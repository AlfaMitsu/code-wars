I love you, a little , a lot, passionately ... not at all

package kata

func HowMuchILoveYou(i int) string {
	phrases := []string{"I love you", "a little", "a lot", "passionately", "madly", "not at all"}
	index := (i - 1) % len(phrases)
	return phrases[index]
}
