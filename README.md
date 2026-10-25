# dnnnah's GitHub Profile

```tsx
import React, { useState, useEffect } from "react";

// Types & Contracts
interface DevProfile {
  name: string;
  role: string;
  focus: string;
  stack: {
    core: string[];
    styling: string[];
    ecosystem: string[];
    tooling: string[];
  };
}

const currentProfile: DevProfile = {
  name: "Donnovan Trejo",
  role: "Frontend Developer & UI/UX Craftsman",
  focus: "Component architectures, responsive design & snappy interactions",
  stack: {
    core: ["TypeScript", "JavaScript (ESNext)", "React", "HTML5/CSS3"],
    styling: ["Tailwind CSS", "Flexbox", "Responsive Design", "CSS Modules"],
    ecosystem: ["Vite", "Jest" "Zustand / Redux", "React Router"],
    tooling: ["VS Code", "Git / GitHub", "LLMs", "macOS"],
  },
};

export const DeveloperSpace: React.FC = () => {
  const [chaosMode, setChaosMode] = useState<boolean>(true);
  const [renderStatus, setRenderStatus] = useState<string>("Initializing Virtual DOM...");

  useEffect(() => {
    // Philosophical Logic Check:
    // "Without strict layout constraints, UI collapses into undefined behavior."
    if (chaosMode) {
      console.warn("Fatal: CSS specificity war detected. Everything is permitted.");
      setRenderStatus("Error: Infinite re-render loop triggered. Centering a div with float.");
      return;
    }

    setRenderStatus("Status: Strict constraints applied. Flexbox aligned perfectly.");
  }, [chaosMode]);

  return (
    <main className="flex min-h-screen flex-col items-center justify-center p-8 font-mono">
      <header className="border-b border-zinc-800 pb-4">
        <h1 className="text-2xl font-bold tracking-tight text-zinc-100">
          {currentProfile.name}
        </h1>
        <p className="text-sm text-zinc-400">{currentProfile.role}</p>
      </header>

      <section className="mt-6 max-w-lg space-y-4 text-xs text-zinc-300">
        <div>
          <span className="text-emerald-400">Current Focus:</span> {currentProfile.focus}
        </div>

        <div className="rounded-md bg-zinc-950 p-4 border border-zinc-900">
          <p className="text-zinc-500">// Stack Snapshot</p>
          <p className="mt-1">
            <span className="text-cyan-400">Core:</span> {currentProfile.stack.core.join(" · ")}
          </p>
          <p>
            <span className="text-cyan-400">Styling:</span> {currentProfile.stack.styling.join(" · ")}
          </p>
          <p>
            <span className="text-cyan-400">Tooling:</span> {currentProfile.stack.tooling.join(" · ")}
          </p>
        </div>

        <aside className="border-l-2 border-amber-500 pl-3 italic text-zinc-400">
          {renderStatus}
        </aside>
      </section>
    </main>
  );
};

export default DeveloperSpace;
