# dnnnah's GitHub Profile

```tsx
import React from "react";

// Tipos & Datos
interface DevProfile {
  name: string;
  role: string;
  stack: {
    core: readonly string[];
    styling: readonly string[];
    ecosystem: readonly string[];
    tooling: readonly string[];
  };
}

const profile: DevProfile = {
  name: "Donnovan Trejo",
  role: "Frontend Developer + AI-Assisted Engineering",
  stack: {
    core: ["TypeScript", "React 19", "JavaScript (ESNext)", "HTML5/CSS3"],
    styling: ["Tailwind CSS", "Design Systems", "Space Grotesk", "Fluid Typography"],
    ecosystem: ["Vite", "Zustand / Redux", "Vitest", "Vercel Functions"],
    tooling: ["VS Code", "Git / GitHub", "macOS", "AI Agents Workflow"],
  },
} as const;

export const Profile: React.FC = () => {
  return (
    <main className="w-full max-w-lg rounded-lg border-2 border-[#171717] bg-[#F6F5F0] p-6 font-mono text-[#171717] shadow-[6px_6px_0px_0px_#171717]">
      {/* Header: Monograma, Nombre y Badge */}
      <header className="flex items-center justify-between border-b border-[#D8D6CF] pb-4">
        <div className="flex items-center gap-3">
          <div className="flex h-10 w-10 shrink-0 items-center justify-center rounded-lg bg-[#171717] font-display text-xl font-bold text-white shadow-sm">
            D.
          </div>
          <div>
            <h1 className="font-display text-2xl font-bold tracking-tight text-[#171717] leading-none">
              {profile.name}
            </h1>
            <p className="mt-1 text-xs font-sans font-medium text-zinc-600">
              {profile.role}
            </p>
          </div>
        </div>

        <a
          href="[https://dnnnah.netlify.app/](https://dnnnah.netlify.app/)"
          className="rotate-[-3deg] rounded-sm border border-[#171717] bg-[#B8FF65] px-2.5 py-1 font-display text-[11px] font-semibold text-[#171717] shadow-[2px_2px_0px_0px_#171717] transition hover:rotate-0"
        >
          dnnnah.dev ↗
        </a>
      </header>

      {/* Stack Snapshot */}
      <section className="mt-4 space-y-1.5 rounded-md border border-[#171717] bg-white p-3.5 text-xs shadow-[3px_3px_0px_0px_#171717]">
        <p className="text-[11px] font-bold text-zinc-500">// Stack Snapshot</p>
        <p><span className="font-semibold text-zinc-600">Core:</span> {profile.stack.core.join(" · ")}</p>
        <p><span className="font-semibold text-zinc-600">Styling:</span> {profile.stack.styling.join(" · ")}</p>
        <p><span className="font-semibold text-zinc-600">Ecosystem:</span> {profile.stack.ecosystem.join(" · ")}</p>
        <p><span className="font-semibold text-zinc-600">Tooling:</span> {profile.stack.tooling.join(" · ")}</p>
      </section>
    </main>
  );
};

export default Profile;
```
