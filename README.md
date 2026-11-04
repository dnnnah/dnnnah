# Donnovan Trejo

```ts
type Role = `Frontend Developer + AI-Assisted Engineering`;

interface DevProfile<T Record<string, extends readonly string[]>> {
  readonly name: string;
  readonly role: Role;
  readonly stack: T;
  readonly url: `https://${string}`;
}

export const profile = {
  name: "Donnovan Trejo",
  role: "Frontend Developer + AI-Assisted Engineering",
  stack: {
    core: ["TypeScript", "React 19", "JavaScript (ESNext)", "HTML5/CSS3"],
    styling: ["Tailwind CSS", "Design Systems", "Space Grotesk", "Fluid Typography"],
    ecosystem: ["Vite", "Zustand / Redux", "Vitest", "Vercel Functions"],
    tooling: ["VS Code", "Git / GitHub", "macOS", "AI Agents Workflow"],
  },
  url: "[https://dnnnah.netlify.app/](https://dnnnah.netlify.app/)",
} as const satisfies DevProfile<{
  readonly [K in "core" | "styling" | "ecosystem" | "tooling"]: readonly string[];
}>;

export type StackSnapshot = {
  [K in keyof typeof profile.stack]: (typeof profile.stack)[K][number];
};
```
