Bumps in the road

    export function bump(x: string): string{
      const bumps = (x.match(/n/g) || []).length;
      return bumps <= 15 ? 'Woohoo!' : 'Car Dead';
    }
