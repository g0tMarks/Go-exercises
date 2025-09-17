package main

import "fmt"

func getMonthlyPrice(tier string) int {
	switch tier {
	case "basic":
		return 10000
	case "premium":
		return 15000
	case "enterprise":
		return 50000
	default:
		return 0
	}
}

func main() {
	test("basic", 10000)
	test("premium", 15000)
	test("enterprise", 50000)
}

func test(tier string, expected int) {
	fmt.Println(getMonthlyPrice(tier))
}
