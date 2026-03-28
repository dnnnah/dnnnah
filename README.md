# [username]'s GitHub Profile

```go
package main

import (
	"fmt"
	"time"
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
			"Languages":      {"Go", "Python", "JavaScript"},
			"Frameworks/Libs": {"React"},
			"Databases":      {"SQL"},
			"Tools":          {"VS Code", "AI Integration"},
			"Environments":   {"Mac", "Linux"},
		},
	}

	// My digital presence
	myLinkedIn = ContactInfo{
		Platform: "LinkedIn",
		URL:      "https://www.linkedin.com/in/donnovan-tc/", // <-- REEMPLAZA ESTO
	}
)

func main() {
	// Let's start with the classic (Go-style)
	fmt.Println("Gola Mundo!") // [Spanish: ¡Hola Mundo!]

	// Current Goal
	fmt.Printf("\nCurrently learning: How to effectively use AI tools, master Go, and become a better developer.\n")

	// Dostoevsky joke
	fmt.Println("\n-- Dostoevsky's Dev Philosophy --")
	fmt.Println("\"We sometimes encounter people, even perfect strangers, who begin to interested us at first sight, before we have said a single word. Especially if they have clean git history.\"\n")

	// Off-screen Activities
	fmt.Printf("When I'm not coding, I enjoy watching series/movies and playing casual video games.\n")
}
