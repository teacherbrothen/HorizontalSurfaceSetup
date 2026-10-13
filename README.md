# Horizontal Surface Projectile Setup

An interactive, web-based scaffolding tool designed for high school physics students learning 2D kinematics with angled launches over level ground.

Like its horizontal-launch counterpart, this tool isolates **conceptual modeling, vector decomposition, and interval selection** from arithmetic computation. Before students reach for a calculator or memorize rigid range formulas, this activity trains them to break down initial velocity vectors, define the appropriate flight interval, populate a two-dimensional T-Chart, and identify scalar time ($t$) as the bridging variable.

---

## 🎯 Pedagogical Rationale

Physics Education Research (PER) shows that angled projectile motion introduces two major cognitive hurdles that cause novice problem-solving to break down:

### 1. Vector Decomposition Without Calculator Distraction
Novice students frequently plug the resultant launch speed ($v_0$) directly into their kinematic equations or swap sine and cosine due to calculator errors (such as being in radian mode). 
* **The Solution:** This tool provides a dedicated **Velocity Resolution Workspace** featuring a right triangle with vector arrowheads. The exact trigonometric substitutions—e.g., $(v_0\text{ m/s})(\cos\theta)$—are evaluated visually on screen, producing unsigned component tiles. Students must inspect the geometry (adjacent vs. opposite) to decide which component belongs on which axis.

### 2. Eliminating the "Frankenstein Table" (Apex vs. Range)
Students frequently mix incompatible points in time into the same table—for example, setting final vertical velocity to $\vec{v}_{V2} = 0\text{ m/s}$ (true only at the **apex**) while simultaneously writing horizontal displacement as full $\text{Range}$ (true only at **landing**).
* **The Solution:** Students must explicitly declare their **Interval of Interest** before the Knowledge Bank unlocks:
  * **Launch to Peak (Apex):** Models the half-trip to find maximum elevation ($h_{\text{max}}$) or time-to-peak. Implied vertical condition: $\vec{v}_{V2} = 0\text{ m/s}$.
  * **Launch to Ground (Full Range):** Models the full flight to find horizontal range or total hang time. Implied vertical conditions: $\vec{d}_V = 0\text{ m}$ and $\vec{v}_{V2} = -v_{0y}$ (via physical symmetry).

### 3. The Power of Symmetry (4 Known Vertical Variables)
In the full-flight scenario, recognizing that $\vec{v}_{V2} = -v_{0y}$ and $\vec{d}_V = 0\text{ m}$ provides **four known vertical quantities** ($\vec{v}_{V1}, \vec{v}_{V2}, \vec{a}_V, \vec{d}_V$). This visually proves to students that total hang time can be calculated easily using:
$$t = \frac{\vec{v}_{V2} - \vec{v}_{V1}}{\vec{a}_V}$$
bypassing the need for the quadratic formula.

---

## 🔄 Student Workflow

Each randomized scenario follows a seamless 5-step progression without artificial button gates:

1. **Velocity Resolution:** Students inspect the launch triangle and use trigonometry to drag the horizontal and vertical velocity components into the T-chart.
2. **Interval Selection:** Students choose whether the target question requires modeling **Launch to Peak (Apex)** or **Launch to Ground (Landing)**.
3. **Implied Constants (Knowledge Bank):** Students drag the physical constants appropriate for their chosen interval into the chart (including $\vec{a}_V = -9.81\text{ m/s}^2$, $\vec{v}_{V2} = 0\text{ m/s}$, or landing symmetry values).
4. **Target Identification:** Students click the chart slot representing what the problem asks them to find ($d_V$ for max height, or $d_H$ for range).
5. **Locate the Bridge Variable ($t$):** Students identify time ($t$) as the single-step variable needed to cross columns and solve the problem.

---

## ✨ Features

- **Zero-Math Scaffolding:** Trig substitutions and arithmetic are calculated on screen so students focus 100% on conceptual schemas.
- **Isotropically Scaled Motion Diagram:** Features an SVG ground-to-ground parabolic trajectory that scales proportionally to the problem values, displaying the target unknown as `$?$`.
- **Cross-Platform Math Typography:** Clean sans-serif mathematical rendering via KaTeX with vector arrows anchored strictly over variable letters across Windows (`Segoe UI`), ChromeOS (`Roboto`), and macOS.
- **SCORM 1.2 Built-In (Brightspace / Canvas / Moodle):** Reports a 100% completion grade once 5 scenarios are completed. Built-in re-entry protection prevents subsequent practice runs from ever overwriting a student's grade.
- **Clipboard Verification Proof:** Features an `html2canvas` proof generator that captures a timestamped summary card with a unique session ID for easy LMS verification.

---

## 🚀 Deployment Options

### Option A: Host on GitHub Pages (Web Link / Embed)
1. Fork or push this repository to GitHub.
2. Go to **Settings** $\rightarrow$ **Pages**.
3. Under **Branch**, select `main` (or `master`) and `/root`, then click **Save**.
4. Share the generated URL or embed it into your LMS with an `<iframe>`:
   ```html
   <iframe src="https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/" width="1020" height="920" frameborder="0"></iframe>
