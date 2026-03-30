<style>
  /* Custom UI Tweaks */
  details {
    background: #111;
    border: 1px solid #222;
    padding: 15px;
    border-radius: 8px;
    margin-bottom: 20px;
    cursor: pointer;
    transition: border-color 0.2s;
  }
	details:hover { border-color: #333; }
  summary {
    font-size: 1.2em;
    font-weight: bold;
    color: #eee;
    outline: none;
    display: list-item;
  }
  details[open] summary { color: #b5e853; /* Green when open */ }
  .project-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-top: 15px;
  }
  .project-card {
    flex: 1 1 calc(50% - 20px);
    background: #151515;
    border: 1px solid #333;
    padding: 20px;
    border-radius: 8px;
    transition: transform 0.2s, border-color 0.2s;
  }
  .project-card:hover { transform: translateY(-3px); border-color: #b5e853; }
  
  /* Specialty tags within cards */
  .tech-tag {
    display: inline-block;
    background: #222;
    color: #eee;
    padding: 2px 8px;
    border-radius: 4px;
    font-size: 0.8em;
    margin-right: 5px;
    margin-top: 10px;
    border: 1px solid #444;
  }

  /* --- FIGURE & IMAGE HOVER EFFECTS (Crucial Update) --- */
  .figure-container {
    display: flex;
    gap: 10px;
    justify-content: center;
    margin-top: 20px;
    position: relative;
    z-index: 1; /* Ensures they layer correctly when magnified */
  }
  
  /* Magnification effect on Figs 1-3 */
  .magnify-figure {
    text-align: center;
    transition: transform 0.3s ease-in-out, z-index 0s;
  }
  .magnify-figure:hover {
    transform: scale(2.0); /* Enlarge by 100% */
    z-index: 99; /* Pop above other figures */
  }
  .magnify-figure img { border-radius: 4px; border: 1px solid #222; }

  /* Magnification effect on the main Fig 4 */
  .magnify-large {
    transition: transform 0.3s ease-in-out;
    cursor: zoom-in;
  }
  .magnify-large:hover { transform: scale(1.3); }

</style>

# Ryan Barrage, PhD
### Systems Architect • Gameplay Programmer • Computational Researcher

A researcher-turned-developer with a background in **Mathematical Physics** and **Computational Mechanics**. I specialize in building robust, high-consequence systems - from deriving 6-DOF constitutive material models to architecting authoritative multiplayer backends.

---

## Featured Game Projects

<div class="project-grid">
  <div class="project-card">
    <h3>Celestica | Full-Stack TCG</h3>
    <p>Globally networked 1v1 TCG with a server-side logic engine in Unity.</p>
    <span class="tech-tag">Unity/C#</span>
    <span class="tech-tag">DigitalOcean</span>
    <span class="tech-tag">MongoDB</span>
    <br><br>
    <a href="https://celesticatcg.com/">Visit Project Site →</a>
  </div>
  
  <div class="project-card">
    <h3>Express Checkout | Infrastructure</h3>
    <p>4-player online co-op featuring dynamic server orchestration.</p>
    <span class="tech-tag">Network Architecture</span>
	<span class="tech-tag">Game Server Spawner</span>
    <span class="tech-tag">Instance Scaling</span>
    <span class="tech-tag">Procedural Generation</span>
  </div>
</div>

---

## Computational Research

<details>
  <summary>PhD Framework: Cosserat Elasticity in Functionally Graded Composites</summary>
  <p>Developed a non-classical Finite Element framework to simulate size-dependent behavior in exponentially graded isotropic materials.</p>
  <ul>
    <li><strong>6-DOF Constitutive Logic:</strong> Derived and implemented a material model for exponentially graded materials within the framework of <strong>Cosserat (Micropolar) Elasticity</strong>.</li>
    <li><strong>Numerical Implementation:</strong> Authored a custom <strong>User Element (UEL)</strong> in Fortran for Abaqus, capturing 3 translational and 3 rotational degrees of freedom per node to model microstructural influence.</li>
	<li><strong>Data Engineering:</strong> Engineered a Python utility to bridge raw solver output with <strong>Paraview (VTK)</strong> for advanced volumetric field analysis.</li>
  </ul>
  
  <strong> Numerical Analysis: Torsional Size Effects</strong>
  
  <div class="figure-container">
    <figure class="magnify-figure">
      <img src="/assets/images/fig1.png" width="275">
      <figcaption><small>Fig 1: Classical</small></figcaption>
    </figure>
    <figure class="magnify-figure">
      <img src="/assets/images/fig2.png" width="275">
      <figcaption><small>Fig 2: l=0.1mm</small></figcaption>
    </figure>
    <figure class="magnify-figure">
      <img src="/assets/images/fig3.png" width="275">
      <figcaption><small>Fig 3: l=1.0mm</small></figcaption>
    </figure>
  </div>
  
  <p align="center">
    <img src="/assets/images/fig4.png" width="600" class="magnify-large"><br>
    <em>Fig 4: Numerical confirmation of the "Size Effect" phenomenon.</em>
  </p>
</details>

<details>
  <summary> Master's Research: GFRP Reinforced Concrete Beams</summary>
  <p>Conducted non-linear FEA to evaluate the performance of glass-fiber-reinforced polymer (GFRP) beams.</p>
  <ul>
    <li><strong>Large-Scale Automation:</strong> Orchestrated <strong>300+ unique Abaqus simulations</strong> investigating a wide range of slenderness ratios.</li>
    <li><strong>Pipeline:</strong> Developed a Python-driven parametric pipeline for job submission, and result extraction (Python-XLSX).</li>
  </ul>
</details>

<details>
  <summary>📚 Selected Publications & Theses</summary>
	<div class="project-grid">
	  <div class="project-card publication-card">
	    <h4>Methods in Modelling of Composite Materials with Microstructure</h4>
	    <p><small>Doctoral Thesis | University of Waterloo</small></p>
	    <span class="tech-tag">Cosserat Elasticity</span>
	    <span class="tech-tag">Fortran UEL</span>
	    <br><br>
	    <a href="https://uwspace.uwaterloo.ca/items/01c7c395-2718-400e-94e0-c069cdeb2498">View Thesis →</a>
	  </div>
	
	  <div class="project-card publication-card">
	    <h4>Finite Element Modelling of FRP Reinforced Concrete Beams and Comparative Analysis of Current Strength Prediction Methods</h4>
	    <p><small>Master's Thesis | University of Waterloo</small></p>
	    <span class="tech-tag">Nonlinear FEA</span>
	    <span class="tech-tag">Python Automation</span>
	    <br><br>
	    <a href="https://uwspace.uwaterloo.ca/items/8454788e-533b-4c1c-9b26-ea31f7ba23b1">View Thesis →</a>
	  </div>
	
	  <div class="project-card publication-card">
	    <h4>Finite Element Modelling of Exponentially Graded Composites with Microstructure</h4>
	    <p><small>Mathematics and Mechanics of Solids</small></p>
	    <span class="tech-tag">Constitutive Modelling</span>
	    <br><br>
	    <a href="https://journals.sagepub.com/doi/full/10.1177/10812865221147858">Read Journal Article →</a>
	  </div>
	
	  <div class="project-card publication-card">
	    <h4>Influence of Microstructural Characteristic Torsion Length on Exponentially Graded Cylinders in Torsion</h4>
	    <p><small>Acta Mechanica (Springer)</small></p>
	    <span class="tech-tag">Torsional Size Effect</span>
	    <br><br>
	    <a href="https://link.springer.com/article/10.1007/s00707-022-03436-8">Read Journal Article →</a>
	  </div>
	  
	  <div class="project-card publication-card">
	    <h4>Flexural and Shear Behaviours of GFRP-Reinforced Concrete Beams Based on Nonlinear Finite Element Studies</h4>
	    <p><small>Canadian Journal of Civil Engineering</small></p>
	    <span class="tech-tag">Parametric Studies</span>
	    <br><br>
	    <a href="https://cdnsciencepub.com/doi/abs/10.1139/cjce-2022-0179">Read Journal Article →</a>
	  </div>
  </div>
  </details>
</div>



---

## Technical Repertoire & Contact

* **Languages:** C#, Python, SQL, Fortran.
* **Tools:** Unity, MongoDB, DigitalOcean, Abaqus, Paraview.
* **GitHub:** [RyanBarrage](https://github.com/RyanBarrage)
* **Email:** [ryan.barrage@gmail.com](mailto:ryan.barrage@gmail.com)
