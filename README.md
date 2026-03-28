# dnnah's GitHub Profile

```go
package main

import (
	"fmt"
)

// DevProfile defines who I am
type DevProfile struct {
	Name       string
	Role       string
	Philosophy string
	Stack      map[string][]string
}

// ContactInfo defines how to reach me
type ContactInfo struct {
	Platform string
	URL      string
}

var (
	// My current focus and tools
	currentProfile = DevProfile{
		Name:       "dnnah",
		Role:       "Constant Learner of New Technologies",
		Philosophy: "Write once, do it right, and automate everything. Aim for scalability.",
		Stack: map[string][]string{
			"Languages":       {"Go", "Python", "JavaScript"},
			"Frameworks/Libs": {"React"},
			"Databases":       {"SQL"},
			"Tools":           {"VS Code", "AI Integration"},
			"Environments":    {"Mac", "Linux"},
		},
	}

	// My digital presence
	myLinkedIn = ContactInfo{
		Platform: "LinkedIn",
		URL:      "[https://www.linkedin.com/in/donnovan-tc/](https://www.linkedin.com/in/donnovan-tc/)",
	}
)

func main() {
	// Let's start
	fmt.Println("GOla Mundo!")

	// Current Goal
	fmt.Printf("\nCurrently learning: How to effectively use AI tools, master Go, and become a better developer.\n")

	// Off-screen Activities
	fmt.Printf("When I'm not coding, I enjoy watching series/movies and playing casual video games.\n\n")

	// Philosophical Debugging
	fmt.Println(ExistentialCheck())
}

/*
 * Based on Fiodor Dostoyevsky:
 * "If God does not exist, everything is permitted;
 * and if everything is permitted, life is impossible."
 *
 * [ES]: "Si Dios no existe, todo está permitido;
 * y si todo está permitido, la vida es imposible...
 * y si la vida es imposible, la gente programa en PHP."
 */
func ExistentialCheck() string {
	lifeIsPossible := false

	if !lifeIsPossible {
		return "panic: life is impossible, switching to PHP... (sudo apt install php)"
	}
	return "go run main.go"
}
