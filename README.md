# dnnnah's GitHub Profile

```tsx
import React, { useState } from "react";

// Tipado y contratos
interface Channel {
  platform: string;
  handle: string;
  url: string;
}

interface DevProfile {
  brand: string;
  name: string;
  role: string;
  manifesto: string;
  description: string;
  principle: string;
  channels: readonly Channel[];
  stack: {
    core: readonly string[];
    styling: readonly string[];
    ecosystem: readonly string[];
    tooling: readonly string[];
  };
}

const currentProfile: DevProfile = {
  brand: "D.",
  name: "Donnovan Trejo",
  role: "Frontend Developer + AI-Assisted Engineering",
  manifesto: "Diseño la lógica. Dirijo la creación. Respondo por el resultado.",
  description:
    "Dirijo la arquitectura y coordino agentes de IA para convertir ideas en experiencias digitales. Combino desarrollo web sólido con arquitectura de componentes e interfaces con personalidad propia.",
  principle: "Intención en cada decisión.",
  channels: [
    { platform: "Portfolio", handle: "dnnnah.dev", url: "[https://dnnnah.dev](https://dnnnah.dev)" },
    { platform: "LinkedIn", handle: "in/donnovan-tc", url: "[https://linkedin.com/in/donnovan-tc](https://linkedin.com/in/donnovan-tc)" },
    { platform: "Email", handle: "dnnnah@icloud.com", url: "mailto:dnnnah@icloud.com" },
  ],
  stack: {
    core: ["TypeScript", "React 19", "JavaScript (ESNext)", "HTML5 / CSS3"],
    styling: ["Tailwind CSS", "Design Systems", "Space Grotesk", "Fluid Typography"],
    ecosystem: ["Vite", "Zustand / Redux", "Vitest", "Vercel Functions"],
    tooling: ["VS Code", "Git / GitHub", "macOS", "AI Agents Workflow"],
  },
} as const;

export const DnnnahProfile: React.FC = () => {
  const [terminalOpen, setTerminalOpen] = useState<boolean>(false);

  return (
    <main className="w-full max-w-3xl rounded-lg border-2 border-[#171717] bg-[#F6F5F0] p-8 font-sans text-[#171717] shadow-[8px_8px_0px_0px_#171717]">
      {/* Filebar IDE */}
      <div className="flex items-center justify-between border-b border-[#D8D6CF] pb-3 text-xs font-mono text-zinc-500">
        <div className="flex items-center gap-2">
          <span className="h-2 w-2 rounded-full bg-[#171717]" />
          <span className="font-semibold text-[#171717]">profile.tsx</span>
          <span>/</span>
          <span>Creative Workspace</span>
        </div>
        <span className="rounded border border-[#D8D6CF] bg-white px-2 py-0.5 text-[11px] text-zinc-600">
          Interactive Workspace
        </span>
      </div>

      {/* Masthead con Monograma D. y Badges inclinados */}
      <header className="mt-6 flex flex-wrap items-start justify-between gap-4">
        <div className="flex items-start gap-4">
          <div className="flex h-12 w-12 items-center justify-center rounded-xl bg-[#171717] font-display text-2xl font-bold text-white shadow-sm">
            {currentProfile.brand}
          </div>
          <div>
            <span className="font-mono text-xs uppercase tracking-wider text-zinc-500">// Creative Developer</span>
            <h1 className="font-display text-4xl font-bold tracking-tight text-[#171717]">
              {currentProfile.name}
            </h1>
            <p className="font-medium text-zinc-700">{currentProfile.role}</p>
          </div>
        </div>

        {/* Tilted Badges */}
        <div className="flex flex-col gap-2">
          <span className="rotate-[-4deg] rounded-sm border border-[#171717] bg-[#B8FF65] px-3 py-1 font-display text-xs font-semibold shadow-[2px_2px_0px_0px_#171717]">
            Frontend Developer
          </span>
          <span className="rotate-[3deg] rounded-sm border border-[#171717] bg-[#D9CDFF] px-3 py-1 font-display text-xs font-semibold shadow-[2px_2px_0px_0px_#171717]">
            AI-Assisted Engineering
          </span>
        </div>
      </header>

      {/* Manifiesto */}
      <blockquote className="mt-6 border-l-4 border-[#B8FF65] border-y border-r border-[#D8D6CF] bg-white p-4 font-display text-lg font-medium">
        "{currentProfile.manifesto}"
      </blockquote>

      {/* Stack Snapshot */}
      <section className="mt-6 rounded-lg border border-[#171717] bg-white p-5 shadow-[4px_4px_0px_0px_#171717]">
        <div className="flex justify-between border-b border-[#D8D6CF] pb-2 font-mono text-xs text-zinc-500">
          <span className="font-semibold text-[#171717]">// Stack Snapshot</span>
          <span>src/components/skills.ts</span>
        </div>
        <div className="mt-3 grid grid-cols-1 sm:grid-cols-2 gap-3 text-xs font-mono">
          <p className="rounded border border-[#D8D6CF] bg-[#F6F5F0] p-2">
            <span className="font-bold text-zinc-500">Core: </span>
            {currentProfile.stack.core.join(" · ")}
          </p>
          <p className="rounded border border-[#D8D6CF] bg-[#F6F5F0] p-2">
            <span className="font-bold text-zinc-500">Styling: </span>
            {currentProfile.stack.styling.join(" · ")}
          </p>
          <p className="rounded border border-[#D8D6CF] bg-[#F6F5F0] p-2">
            <span className="font-bold text-zinc-500">Ecosystem: </span>
            {currentProfile.stack.ecosystem.join(" · ")}
          </p>
          <p className="rounded border border-[#D8D6CF] bg-[#F6F5F0] p-2">
            <span className="font-bold text-zinc-500">Tooling: </span>
            {currentProfile.stack.tooling.join(" · ")}
          </p>
        </div>
      </section>

      {/* Footer y Canales */}
      <footer className="mt-6 flex flex-wrap items-center justify-between gap-4 border-t border-[#D8D6CF] pt-4 font-mono text-xs">
        <div className="flex flex-wrap gap-2">
          {currentProfile.channels.map((ch) => (
            <a
              key={ch.platform}
              href={ch.url}
              className="rounded border border-[#171717] bg-white px-3 py-1 font-medium transition hover:bg-[#B8FF65] shadow-[2px_2px_0px_0px_#171717]"
            >
              {ch.platform}: <span className="font-semibold">{ch.handle}</span>
            </a>
          ))}
        </div>
        <span className="text-zinc-500">{currentProfile.principle}</span>
      </footer>
    </main>
  );
};

export default DnnnahProfile;
```
