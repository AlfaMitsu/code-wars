Looking for a Benefactor

    export function newAvg(arr: number[], newavg: number): number {
        const totalDonations = arr.reduce((acc, curr) => acc + curr, 0);
        const targetSum = (arr.length + 1) * newavg;
        const additionalDonation = Math.ceil(targetSum - totalDonations);
        if (additionalDonation <= 0) {
            throw new Error('Expected New Average is too low');
        }
        return additionalDonation;
    }
