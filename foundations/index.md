---
layout: default
title: Foundation Modules
---

<style>
/* Enhanced styles for foundations page */
.hero-section {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 4rem 2rem;
    border-radius: 24px;
    margin-bottom: 3rem;
    text-align: center;
    position: relative;
    overflow: hidden;
}

.hero-section::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
    animation: float 8s ease-in-out infinite;
}

.page-title {
    font-size: 3rem;
    font-weight: 800;
    margin-bottom: 1rem;
    background: linear-gradient(45deg, #fff, #e3f2fd);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    position: relative;
    z-index: 2;
}

.page-subtitle {
    font-size: 1.3rem;
    opacity: 0.9;
    margin-bottom: 2rem;
    position: relative;
    z-index: 2;
}

.module-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem;
    margin: 2rem 0;
    position: relative;
    z-index: 2;
}

.module-card {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(10px);
    border-radius: 16px;
    padding: 2rem;
    border: 1px solid rgba(255, 255, 255, 0.2);
    transition: all 0.3s ease;
    cursor: pointer;
}

.module-card:hover {
    transform: translateY(-8px);
    background: rgba(255, 255, 255, 0.25);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
}

.module-number {
    font-size: 2rem;
    font-weight: 900;
    color: #fff;
    margin-bottom: 0.5rem;
}

.module-title {
    font-size: 1.2rem;
    font-weight: 600;
    color: rgba(255, 255, 255, 0.95);
    margin-bottom: 1rem;
}

.module-description {
    color: rgba(255, 255, 255, 0.8);
    font-size: 0.9rem;
    line-height: 1.5;
}

.content-wrapper {
    background: white;
    border-radius: 24px;
    padding: 3rem;
    margin: 2rem 0;
    box-shadow: 0 10px 40px rgba(0, 0, 0, 0.08);
    position: relative;
}

.content-wrapper::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 5px;
    background: linear-gradient(90deg, #667eea, #764ba2);
    border-radius: 24px 24px 0 0;
}

.section {
    margin: 4rem 0;
    padding: 3rem;
    background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
    border-radius: 20px;
    border-left: 6px solid #667eea;
    position: relative;
}

.section-title {
    font-size: 2.2rem;
    color: #1e293b;
    margin-bottom: 1rem;
    font-weight: 800;
    display: flex;
    align-items: center;
    gap: 1rem;
}

.section-subtitle {
    font-size: 1.1rem;
    color: #64748b;
    margin-bottom: 2rem;
    font-weight: 500;
}

.subsection {
    margin: 2.5rem 0;
    padding: 2rem;
    background: white;
    border-radius: 16px;
    border-left: 4px solid #3b82f6;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
}

.subsection h4 {
    font-size: 1.6rem;
    color: #1e293b;
    margin-bottom: 1.5rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 0.8rem;
}

.subsection h5 {
    font-size: 1.3rem;
    color: #334155;
    margin: 1.5rem 0 1rem 0;
    font-weight: 600;
}

.subsection p {
    font-size: 1.05rem;
    line-height: 1.7;
    color: #475569;
    margin-bottom: 1.2rem;
}

.concept-box {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 2rem;
    border-radius: 16px;
    margin: 2rem 0;
    position: relative;
    overflow: hidden;
}

.concept-box::before {
    content: '';
    position: absolute;
    top: -2px;
    left: -2px;
    right: -2px;
    bottom: -2px;
    background: linear-gradient(45deg, #667eea, #764ba2, #667eea);
    border-radius: 18px;
    z-index: -1;
    animation: borderGlow 3s linear infinite;
}

.concept-box h5 {
    margin-bottom: 1rem;
    font-size: 1.3rem;
    font-weight: 700;
}

.concept-box p {
    margin: 0;
    line-height: 1.6;
}

.formula-box {
    background: #1e293b;
    color: #e2e8f0;
    padding: 1.5rem;
    border-radius: 12px;
    margin: 1rem 0;
    font-family: 'Courier New', monospace;
    border-left: 4px solid #3b82f6;
}

.examples-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 1rem;
    margin: 1.5rem 0;
}

.example-card {
    background: rgba(59, 130, 246, 0.1);
    border: 1px solid rgba(59, 130, 246, 0.2);
    padding: 1.5rem;
    border-radius: 12px;
    transition: all 0.3s ease;
}

.example-card:hover {
    background: rgba(59, 130, 246, 0.15);
    transform: translateY(-2px);
}

.example-card strong {
    display: block;
    color: #1e293b;
    margin-bottom: 0.5rem;
    font-weight: 600;
}

.example-card span {
    color: #64748b;
    font-size: 0.95rem;
}

.interactive-box {
    background: linear-gradient(135deg, #10b981 0%, #059669 100%);
    color: white;
    padding: 2rem;
    border-radius: 16px;
    margin: 2rem 0;
}

.interactive-box h5 {
    font-size: 1.4rem;
    margin-bottom: 1rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.interactive-box h5::before {
    content: '🔗';
    font-size: 1.2rem;
}

.resource-list {
    list-style: none;
    padding: 0;
}

.resource-list li {
    padding: 0.8rem 0;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);
    display: flex;
    align-items: flex-start;
    gap: 1rem;
}

.resource-list li:last-child {
    border-bottom: none;
}

.resource-list li::before {
    content: '🌐';
    font-size: 1rem;
    margin-top: 0.2rem;
    flex-shrink: 0;
}

.resource-list a {
    color: white;
    text-decoration: none;
    font-weight: 600;
    border-bottom: 1px solid rgba(255, 255, 255, 0.3);
    transition: all 0.3s ease;
}

.resource-list a:hover {
    border-bottom-color: white;
}

.key-points {
    background: linear-gradient(135deg, #f59e0b 0%, #d97706 100%);
    color: white;
    padding: 2rem;
    border-radius: 16px;
    margin: 2rem 0;
}

.key-points h5 {
    font-size: 1.4rem;
    margin-bottom: 1rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 0.5rem;
}

.key-points h5::before {
    content: '💡';
    font-size: 1.2rem;
}

.points-list {
    list-style: none;
    padding: 0;
}

.points-list li {
    padding: 0.8rem 0;
    padding-left: 2rem;
    position: relative;
    line-height: 1.6;
}

.points-list li::before {
    content: '→';
    position: absolute;
    left: 0;
    color: rgba(255, 255, 255, 0.8);
    font-weight: bold;
    font-size: 1.2rem;
}

.case-study {
    background: linear-gradient(135deg, #8b5cf6 0%, #7c3aed 100%);
    color: white;
    padding: 2.5rem;
    border-radius: 20px;
    margin: 3rem 0;
    position: relative;
    overflow: hidden;
}

.case-study::before {
    content: '';
    position: absolute;
    top: -50%;
    right: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
    animation: float 6s ease-in-out infinite;
}

.case-study-title {
    font-size: 1.8rem;
    font-weight: 800;
    margin-bottom: 1rem;
    position: relative;
    z-index: 2;
}

.case-study-content {
    position: relative;
    z-index: 2;
}

.stats-highlight {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
    margin: 1.5rem 0;
}

.stat-item {
    background: rgba(255, 255, 255, 0.15);
    padding: 1.5rem;
    border-radius: 12px;
    text-align: center;
    backdrop-filter: blur(10px);
}

.stat-value {
    font-size: 1.8rem;
    font-weight: 900;
    margin-bottom: 0.5rem;
}

.stat-label {
    font-size: 0.9rem;
    opacity: 0.9;
}

.timeline {
    position: relative;
    margin: 2rem 0;
    padding-left: 3rem;
}

.timeline::before {
    content: '';
    position: absolute;
    left: 1rem;
    top: 0;
    bottom: 0;
    width: 3px;
    background: linear-gradient(to bottom, #667eea, #764ba2);
}

.timeline-item {
    position: relative;
    margin-bottom: 2rem;
    background: rgba(255, 255, 255, 0.1);
    padding: 1.5rem;
    border-radius: 12px;
    backdrop-filter: blur(10px);
}

.timeline-item::before {
    content: '';
    position: absolute;
    left: -2.5rem;
    top: 1.5rem;
    width: 12px;
    height: 12px;
    background: white;
    border-radius: 50%;
    border: 3px solid #667eea;
}

.timeline-year {
    font-size: 1.2rem;
    font-weight: 700;
    color: #fff;
    margin-bottom: 0.5rem;
}

.timeline-content {
    color: rgba(255, 255, 255, 0.9);
    line-height: 1.6;
}

@keyframes float {
    0%, 100% { transform: translateY(0) rotate(0deg); }
    50% { transform: translateY(-20px) rotate(180deg); }
}

@keyframes borderGlow {
    0%, 100% { background-position: 0% 50%; }
    50% { background-position: 100% 50%; }
}

/* Responsive design */
@media (max-width: 768px) {
    .hero-section {
        padding: 3rem 1.5rem;
    }

    .page-title {
        font-size: 2.2rem;
    }

    .content-wrapper {
        padding: 2rem;
        margin: 1rem 0;
    }

    .module-grid {
        grid-template-columns: 1fr;
    }

    .examples-grid {
        grid-template-columns: 1fr;
    }

    .stats-highlight {
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
    }

    .timeline {
        padding-left: 2rem;
    }

    .timeline::before {
        left: 0.5rem;
    }

    .timeline-item::before {
        left: -1.5rem;
    }
}

/* Dark mode support */
@media (prefers-color-scheme: dark) {
    .content-wrapper {
        background: #1a1a1a;
        color: #e2e8f0;
    }

    .section {
        background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
    }

    .subsection {
        background: #2d3748;
        color: #e2e8f0;
    }

    .example-card {
        background: rgba(59, 130, 246, 0.2);
        color: #e2e8f0;
    }
}
</style>

<!-- Hero Section -->
<section class="hero-section">
    <h1 class="page-title">🧬 Foundation Modules</h1>
    <p class="page-subtitle">Essential concepts and tools for understanding pandemic science</p>

    <div class="module-grid">
        <div class="module-card">
            <div class="module-number">2.1</div>
            <div class="module-title">Essential Epidemiological Terminology</div>
            <div class="module-description">Master the fundamental concepts that drive pandemic analysis</div>
        </div>
        <div class="module-card">
            <div class="module-number">2.2</div>
            <div class="module-title">Natural History & Progression</div>
            <div class="module-description">Understand how diseases evolve from isolated cases to pandemics</div>
        </div>
        <div class="module-card">
            <div class="module-number">2.3</div>
            <div class="module-title">Classical Epidemic Models</div>
            <div class="module-description">Mathematical frameworks for predicting disease spread</div>
        </div>
        <div class="module-card">
            <div class="module-number">2.4</div>
            <div class="module-title">Historical Case Studies</div>
            <div class="module-description">Multidisciplinary lessons from past pandemics</div>
        </div>
        <div class="module-card">
            <div class="module-number">2.5</div>
            <div class="module-title">Surveillance & Early Warning</div>
            <div class="module-description">Modern systems for detecting emerging threats</div>
        </div>
        <div class="module-card">
            <div class="module-number">2.6</div>
            <div class="module-title">Environmental & Social Drivers</div>
            <div class="module-description">The broader context that shapes pandemic risk</div>
        </div>
    </div>
</section>

<div class="content-wrapper">

    ## Part 2: Foundational Science Modules

    <div class="section">
        <h3 class="section-title">📊 2.1 Essential Epidemiological Terminology</h3>
        <p class="section-subtitle">Master the fundamental concepts that drive pandemic analysis</p>

        <div class="subsection">
            <h4>🎯 Understanding Basic Reproduction Number (R₀)</h4>

            <p>The basic reproduction number is perhaps the most important concept in epidemic science. It answers the question: <strong>"In a completely susceptible population, how many people will one infected person infect on average?"</strong></p>

            <div class="formula-box">
                <strong>Mathematical Definition:</strong><br>
                R₀ = (probability of transmission per contact) × (number of contacts per unit time) × (duration of infectiousness)
            </div>

            <div class="key-points">
                <h5>Practical Interpretation</h5>
                <ul class="points-list">
                    <li><strong>R₀ < 1:</strong> Each infected person infects less than one other person → Disease dies out</li>
                    <li><strong>R₀ = 1:</strong> Each infected person infects exactly one other person → Endemic equilibrium</li>
                    <li><strong>R₀ > 1:</strong> Each infected person infects more than one other person → Epidemic growth</li>
                </ul>
            </div>

            <h5>Real-World Examples</h5>
            <div class="examples-grid">
                <div class="example-card">
                    <strong>Measles</strong>
                    <span>R₀ = 12-18 (highly contagious, airborne)</span>
                </div>
                <div class="example-card">
                    <strong>COVID-19 (original)</strong>
                    <span>R₀ = 2.5-3.0 (respiratory droplets)</span>
                </div>
                <div class="example-card">
                    <strong>COVID-19 (Delta)</strong>
                    <span>R₀ = 5-9 (increased transmissibility)</span>
                </div>
                <div class="example-card">
                    <strong>Seasonal flu</strong>
                    <span>R₀ = 1.3 (lower transmission rate)</span>
                </div>
                <div class="example-card">
                    <strong>SARS</strong>
                    <span>R₀ = 2-3 (similar to COVID but contained)</span>
                </div>
            </div>

            <div class="interactive-box">
                <h5>Interactive Learning</h5>
                <ul class="resource-list">
                    <li><a href="https://gabgoh.github.io/COVID/index.html">R₀ Calculator by Gabriel Goh</a> - Adjust parameters and see epidemic curves</li>
                    <li><a href="https://www.cdc.gov/csels/dsepd/ss1978/lesson1/section11.html">CDC's R₀ Explanation</a> - Detailed epidemiological perspective</li>
                    <li><a href="https://ourworldindata.org/covid-reproduction-rate">Our World in Data: R₀ Estimates</a> - Current R₀ tracking for COVID-19</li>
                </ul>
            </div>

            <h5>Effective Reproduction Number (Rt)</h5>
            <p>While R₀ assumes everyone is susceptible, Rt reflects reality:</p>

            <div class="formula-box">
                Rt = R₀ × (fraction of population still susceptible)
            </div>

            <p>As immunity builds through infection or vaccination, Rt decreases. When Rt < 1, the epidemic declines.</p>

            <div class="concept-box">
                <h5>Key Factors Affecting Rt</h5>
                <p>Population immunity levels (natural infection + vaccination), behavioral changes (social distancing, mask wearing), seasonal effects (indoor vs. outdoor activities), new variants with different transmissibility, and public health interventions (contact tracing, isolation).</p>
            </div>
        </div>

        <div class="subsection">
            <h4>📈 Attack Rate and Population Impact</h4>

            <div class="formula-box">
                Attack rate = (Number of people who became ill) / (Number of people at risk) × 100
            </div>

            <h5>Examples from Recent Pandemics</h5>
            <div class="examples-grid">
                <div class="example-card">
                    <strong>1918 Flu</strong>
                    <span>~25% global attack rate</span>
                </div>
                <div class="example-card">
                    <strong>2009 H1N1</strong>
                    <span>~11-21% attack rate in first year</span>
                </div>
                <div class="example-card">
                    <strong>COVID-19</strong>
                    <span>Varies by location (5-70% depending on interventions)</span>
                </div>
            </div>

            <div class="key-points">
                <h5>Attack rates vary by</h5>
                <ul class="points-list">
                    <li>Age groups (children often higher for respiratory diseases)</li>
                    <li>Occupation (healthcare workers, essential workers)</li>
                    <li>Geographic location (urban vs. rural)</li>
                    <li>Socioeconomic status (housing density, job flexibility)</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>💀 Case Fatality Rate (CFR) vs. Infection Fatality Rate (IFR)</h4>

            <p>This distinction became crucial during COVID-19:</p>

            <div class="concept-box">
                <h5>CFR = Deaths among confirmed cases / Total confirmed cases × 100</h5>
                <p>Depends on testing capacity and strategy. Often overestimates true mortality early in pandemics. Useful for hospital planning and clinical management.</p>
            </div>

            <div class="concept-box">
                <h5>IFR = Deaths among all infected / Total infected (including undetected) × 100</h5>
                <p>Requires serological surveys or modeling. Better estimate of true disease severity. Important for policy decisions about interventions.</p>
            </div>

            <h5>COVID-19 Example</h5>
            <div class="examples-grid">
                <div class="example-card">
                    <strong>Early CFR</strong>
                    <span>3-4% (limited testing)</span>
                </div>
                <div class="example-card">
                    <strong>Estimated IFR</strong>
                    <span>0.5-1.0% (including asymptomatic cases)</span>
                </div>
                <div class="example-card">
                    <strong>Age-stratified IFR</strong>
                    <span><0.1% (under 50) to >5% (over 70)</span>
                </div>
            </div>
        </div>

        <div class="subsection">
            <h4>🛡️ Herd Immunity Threshold</h4>

            <div class="formula-box">
                <strong>Formula:</strong> HIT = 1 - (1/R₀)
            </div>

            <h5>Disease Examples</h5>
            <div class="examples-grid">
                <div class="example-card">
                    <strong>Measles (R₀=15)</strong>
                    <span>HIT = 93% - Explains why measles outbreaks occur when vaccination drops below ~95%</span>
                </div>
                <div class="example-card">
                    <strong>COVID-19 (R₀=3)</strong>
                    <span>HIT = 67% - But variants with higher R₀ increase this threshold</span>
                </div>
                <div class="example-card">
                    <strong>Influenza (R₀=1.3)</strong>
                    <span>HIT = 23% - Seasonal patterns affect this calculation</span>
                </div>
            </div>

            <div class="interactive-box">
                <h5>Learning Resources</h5>
                <ul class="resource-list">
                    <li><a href="https://www.vaccineconfidence.org/">Vaccine Confidence Project</a> - Monitoring global attitudes toward vaccines</li>
                    <li><a href="https://www.omnicalculator.com/health/herd-immunity">Herd Immunity Calculator</a> - Interactive threshold calculator</li>
                    <li><a href="https://ourworldindata.org/covid-vaccinations">Our World in Data: Vaccination Progress</a> - Real-time vaccination tracking</li>
                </ul>
            </div>
        </div>
    </div>

    <div class="section">
        <h3 class="section-title">📈 2.2 Natural History and Progression of Epidemics</h3>
        <p class="section-subtitle">Understanding how diseases evolve from isolated cases to pandemics</p>

        <div class="subsection">
            <h4>🔄 Epidemic Progression Framework: From Infection to Pandemic</h4>

            <p>Understanding how diseases escalate helps us know when and how to respond:</p>

            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-year">Stage 1: Sporadic Cases</div>
                    <div class="timeline-content">
                        Individual infections with no clear pattern. May be imported cases from other regions. No evidence of local transmission.
                        <br><strong>Example:</strong> First COVID-19 cases in Wuhan (December 2019)
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-year">Stage 2: Outbreak</div>
                    <div class="timeline-content">
                        Cases exceed expected baseline for the population, time, and place. Clear epidemiological links between cases. Geographic clustering evident.
                        <br><strong>Example:</strong> SARS outbreak in Amoy Gardens, Hong Kong (2003)
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-year">Stage 3: Epidemic</div>
                    <div class="timeline-content">
                        Widespread occurrence within a community or region. Sustained person-to-person transmission. Cases not directly linked to index case or common source.
                        <br><strong>Example:</strong> MERS-CoV outbreak in South Korea (2015)
                    </div>
                </div>

                <div class="timeline-item">
                    <div class="timeline-year">Stage 4: Pandemic</div>
                    <div class="timeline-content">
                        Worldwide spread across multiple countries/continents. Sustained transmission in multiple regions. WHO may declare Public Health Emergency of International Concern (PHEIC).
                        <br><strong>Example:</strong> COVID-19 declared pandemic March 11, 2020
                    </div>
                </div>
            </div>

            <div class="interactive-box">
                <h5>Real-Time Tracking</h5>
                <ul class="resource-list">
                    <li><a href="https://www.who.int/emergencies/disease-outbreak-news">WHO Disease Outbreak News</a> - Current global outbreaks</li>
                    <li><a href="https://promedmail.org/">ProMED-mail</a> - Program for Monitoring Emerging Diseases</li>
                    <li><a href="https://www.healthmap.org/en/">HealthMap</a> - Real-time disease surveillance</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>📊 Epidemic Curve Analysis: Reading the Story of an Outbreak</h4>

            <p>Epidemic curves (epi curves) show the number of cases over time and reveal the outbreak's source and transmission pattern.</p>

            <div class="concept-box">
                <h5>Point Source Outbreak</h5>
                <p><strong>Shape:</strong> Rapid rise to peak, then gradual decline<br>
                <strong>Timeframe:</strong> Cases occur within one incubation period<br>
                <strong>Cause:</strong> Single exposure event<br>
                <strong>Example:</strong> Food poisoning at wedding reception</p>
            </div>

            <div class="concept-box">
                <h5>Continuous Common Source Outbreak</h5>
                <p><strong>Shape:</strong> Plateau or fluctuating pattern<br>
                <strong>Timeframe:</strong> Cases continue as long as exposure continues<br>
                <strong>Cause:</strong> Ongoing exposure to contaminated source<br>
                <strong>Example:</strong> Contaminated water supply</p>
            </div>

            <div class="concept-box">
                <h5>Propagated (Progressive) Source Outbreak</h5>
                <p><strong>Shape:</strong> Series of progressively larger peaks<br>
                <strong>Timeframe:</strong> Peaks separated by incubation period<br>
                <strong>Cause:</strong> Person-to-person transmission<br>
                <strong>Example:</strong> Respiratory virus outbreak</p>
            </div>

            <div class="interactive-box">
                <h5>Interactive Tools</h5>
                <ul class="resource-list">
                    <li><a href="https://www.cdc.gov/training/quicklearns/epiconf/">CDC Epi Curve Tutorial</a> - Interactive learning module</li>
                    <li><a href="https://www.cdc.gov/foodsafety/outbreaks/investigating-outbreaks/epi-curves.html">Epi Curve Analysis Tool</a> - CDC's practical guide</li>
                    <li><a href="https://www.openepi.com/EpiCalc/EpiCalc.htm">OpenEpi Epidemic Calculator</a> - Statistical analysis tools</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>🌍 Seasonal Patterns and Disease Emergence</h4>

            <div class="examples-grid">
                <div class="example-card">
                    <strong>Respiratory Disease Seasonality</strong>
                    <span>Winter peaks: Influenza, RSV, common cold viruses. Factors: Indoor crowding, lower humidity, vitamin D deficiency</span>
                </div>
                <div class="example-card">
                    <strong>Vector-Borne Disease Seasonality</strong>
                    <span>Summer peaks: Malaria, dengue, Zika, West Nile virus. Factors: Vector breeding cycles, temperature effects</span>
                </div>
                <div class="example-card">
                    <strong>Foodborne Disease Patterns</strong>
                    <span>Summer peaks: Bacterial foodborne illness. Holiday clusters: Gathering-associated outbreaks</span>
                </div>
            </div>
        </div>
    </div>

    <div class="section">
        <h3 class="section-title">🧮 2.3 Classical Epidemic Models and Modern Applications</h3>
        <p class="section-subtitle">Mathematical frameworks for predicting disease spread</p>

        <div class="subsection">
            <h4>📐 The SIR Model: Foundation of Epidemic Modeling</h4>

            <p>Developed by Kermack and McKendrick in 1927, the SIR model remains the foundation of epidemic modeling.</p>

            <div class="concept-box">
                <h5>Population Compartments</h5>
                <p><strong>S:</strong> Susceptible individuals who can become infected<br>
                <strong>I:</strong> Infected individuals who can transmit the disease<br>
                <strong>R:</strong> Recovered (or removed) individuals who are immune or deceased</p>
            </div>

            <div class="formula-box">
                <strong>Mathematical Framework:</strong><br>
                dS/dt = -βSI/N<br>
                dI/dt = βSI/N - γI<br>
                dR/dt = γI
            </div>

            <div class="key-points">
                <h5>Parameter Definitions</h5>
                <ul class="points-list">
                    <li><strong>β (beta):</strong> Transmission rate - contacts per time × probability of transmission per contact</li>
                    <li><strong>γ (gamma):</strong> Recovery rate = 1/(infectious period)</li>
                    <li><strong>N:</strong> Total population size</li>
                    <li><strong>R₀ = β/γ:</strong> Basic reproduction number</li>
                </ul>
            </div>

            <div class="concept-box">
                <h5>Key Insights from SIR Model</h5>
                <p>1. <strong>Epidemic threshold:</strong> Epidemic occurs when S₀ > γ/β (or R₀ > 1)<br>
                2. <strong>Final epidemic size:</strong> Not everyone gets infected, even without intervention<br>
                3. <strong>Peak timing:</strong> Depends on R₀ and initial conditions<br>
                4. <strong>Herd immunity:</strong> Epidemic ends when S < γ/β</p>
            </div>

            <div class="interactive-box">
                <h5>Interactive SIR Models</h5>
                <ul class="resource-list">
                    <li><a href="https://www.washingtonpost.com/graphics/2020/world/corona-simulator/">Washington Post: Epidemic Simulator</a> - Visual explanation</li>
                    <li><a href="https://www.youtube.com/watch?v=Kas0tIxDvrg">3Blue1Brown: Exponential Growth</a> - Mathematical intuition</li>
                    <li><a href="http://www.epimodel.org/">EpiModel R Package</a> - Professional modeling tools</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>🔄 SEIR Model: Adding Realism with Incubation Period</h4>

            <p>Many diseases have an incubation period where individuals are infected but not yet infectious.</p>

            <div class="concept-box">
                <h5>Additional Compartment</h5>
                <p><strong>E:</strong> Exposed individuals (infected but not yet infectious)</p>
            </div>

            <div class="formula-box">
                <strong>Mathematical Framework:</strong><br>
                dS/dt = -βSI/N<br>
                dE/dt = βSI/N - σE<br>
                dI/dt = σE - γI<br>
                dR/dt = γI
            </div>

            <div class="key-points">
                <h5>When to Use SEIR</h5>
                <ul class="points-list">
                    <li>Diseases with significant incubation periods (COVID-19, influenza, measles)</li>
                    <li>Policy modeling (latent period affects intervention timing)</li>
                    <li>Contact tracing analysis (exposed individuals need monitoring)</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>🚀 Model Extensions and Modern Applications</h4>

            <div class="examples-grid">
                <div class="example-card">
                    <strong>SIRS Model</strong>
                    <span>Waning Immunity - Adds return from R to S compartment for seasonal influenza, common cold coronaviruses</span>
                </div>
                <div class="example-card">
                    <strong>Age-Structured Models</strong>
                    <span>Different contact patterns, disease severity, and vaccination priorities by age group</span>
                </div>
                <div class="example-card">
                    <strong>Network Models</strong>
                    <span>Account for heterogeneous mixing, superspreading events, geographic spread patterns</span>
                </div>
                <div class="example-card">
                    <strong>Stochastic Models</strong>
                    <span>Include randomness in transmission, small outbreak extinction probability, uncertainty quantification</span>
                </div>
                <div class="example-card">
                    <strong>Agent-Based Models</strong>
                    <span>Track individual agents with detailed behaviors, spatial movement, intervention compliance</span>
                </div>
            </div>

            <div class="interactive-box">
                <h5>Advanced Modeling Resources</h5>
                <ul class="resource-list">
                    <li><a href="https://www.imperial.ac.uk/mrc-global-infectious-disease-analysis/covid-19/">Imperial College COVID-19 Reports</a> - Policy-relevant modeling</li>
                    <li><a href="https://www.idmod.org/">Institute for Disease Modeling</a> - Global health modeling</li>
                    <li><a href="https://covid19scenariomodelinghub.org/">COVID-19 Scenario Hub</a> - Collaborative forecasting</li>
                    <li><a href="https://www.repidemicsconsortium.org/">R Epidemics Consortium (RECON)</a> - Open-source epidemic analysis tools</li>
                </ul>
            </div>
        </div>
    </div>

    <div class="section">
        <h3 class="section-title">📚 2.4 Historical Case Studies with Multidisciplinary Lessons</h3>
        <p class="section-subtitle">Learning from past pandemics to inform future preparedness</p>

        <div class="case-study">
            <h4 class="case-study-title">🦠 Spanish Flu (1918-1920): Lessons in Pandemic Response</h4>
            <div class="case-study-content">
                <p>The 1918 influenza pandemic remains the most devastating pandemic in recorded history, offering crucial lessons for modern pandemic preparedness.</p>

                <div class="stats-highlight">
                    <div class="stat-item">
                        <div class="stat-value">500M</div>
                        <div class="stat-label">Infected (1/3 of world population)</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">50-100M</div>
                        <div class="stat-label">Deaths worldwide</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">1.8-3.0</div>
                        <div class="stat-label">R₀ estimate (similar to COVID-19)</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">3</div>
                        <div class="stat-label">Distinct waves over two years</div>
                    </div>
                </div>

                <div class="concept-box">
                    <h5>Multidisciplinary Lessons</h5>
                    <p><strong>St. Louis vs. Philadelphia:</strong> Classic comparison showing intervention timing matters. St. Louis had early school closures and banned gatherings → death rate 2.7 per 1,000. Philadelphia delayed response and held parade → death rate 7.6 per 1,000.</p>
                </div>
            </div>
        </div>

        <div class="case-study">
            <h4 class="case-study-title">🔬 SARS (2003): Success Story in Global Coordination</h4>
            <div class="case-study-content">
                <p>The SARS outbreak demonstrated how international cooperation and modern public health tools could contain a novel pathogen.</p>

                <div class="stats-highlight">
                    <div class="stat-item">
                        <div class="stat-value">8,098</div>
                        <div class="stat-label">Total cases across 17 countries</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">774</div>
                        <div class="stat-label">Deaths (~10% CFR)</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">8</div>
                        <div class="stat-label">Months from first case to containment</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">$40B</div>
                        <div class="stat-label">Lost GDP</div>
                    </div>
                </div>

                <div class="key-points">
                    <h5>Success Factors</h5>
                    <ul class="points-list">
                        <li><strong>Rapid Scientific Response:</strong> Novel coronavirus identified in 2 weeks, complete genome sequenced and shared globally</li>
                        <li><strong>Global Coordination:</strong> WHO leadership, real-time data sharing, targeted travel advisories</li>
                        <li><strong>Public Health Measures:</strong> Extensive contact tracing, large-scale quarantine, improved infection control</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="case-study">
            <h4 class="case-study-title">🌍 COVID-19 (2019-present): The Modern Pandemic</h4>
            <div class="case-study-content">
                <p>The ongoing COVID-19 pandemic has tested every aspect of global pandemic preparedness and response.</p>

                <div class="stats-highlight">
                    <div class="stat-item">
                        <div class="stat-value">700M+</div>
                        <div class="stat-label">Confirmed cases globally</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">7M+</div>
                        <div class="stat-label">Reported deaths</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value">12-15</div>
                        <div class="stat-label">R₀ estimate for Omicron variant</div>
                    </div>
                    <div class="stat-item">
                        <div class="stat-value"><1 Year</div>
                        <div class="stat-label">mRNA vaccine development time</div>
                    </div>
                </div>

                <div class="key-points">
                    <h5>Multidisciplinary Innovations</h5>
                    <ul class="points-list">
                        <li><strong>Scientific Breakthroughs:</strong> mRNA vaccines, real-time genomic surveillance, multiple therapeutic options</li>
                        <li><strong>Digital Health:</strong> Contact tracing apps, telemedicine, vaccine passports, wastewater surveillance</li>
                        <li><strong>Policy Innovations:</strong> Varied lockdown strategies, unprecedented fiscal response, global vaccine equity initiatives</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="interactive-box">
            <h5>Historical Case Study Resources</h5>
            <ul class="resource-list">
                <li><a href="https://www.pbs.org/wgbh/americanexperience/features/influenza-pandemic-1918/">American Experience: The Great Pandemic</a> - PBS documentary and resources</li>
                <li><a href="https://www.who.int/health-topics/severe-acute-respiratory-syndrome">WHO SARS Archive</a> - Complete WHO response documentation</li>
                <li><a href="https://ourworldindata.org/covid-deaths">Our World in Data: COVID-19</a> - Comprehensive data dashboard</li>
                <li><a href="https://www.nature.com/subjects/covid-19">Nature COVID-19 Collection</a> - Latest research</li>
            </ul>
        </div>
    </div>

    <div class="section">
        <h3 class="section-title">🔍 2.5 Modern Surveillance and Early Warning Systems</h3>
        <p class="section-subtitle">Technology and networks for detecting emerging threats</p>

        <div class="subsection">
            <h4>🌐 Global Surveillance Networks</h4>

            <div class="examples-grid">
                <div class="example-card">
                    <strong>WHO GOARN</strong>
                    <span>200+ technical institutions worldwide. Rapid verification, risk assessment, and expert deployment. Deployed to 63 countries.</span>
                </div>
                <div class="example-card">
                    <strong>GPHIN</strong>
                    <span>AI-powered monitoring of online news in 9 languages. 7,000+ sources worldwide. First detected SARS, H7N9 influenza.</span>
                </div>
                <div class="example-card">
                    <strong>ProMED-mail</strong>
                    <span>Email-based reporting system with expert moderation. 80,000+ subscribers in 185 countries. Often first to report emerging events.</span>
                </div>
                <div class="example-card">
                    <strong>HealthMap</strong>
                    <span>Automated web-scraping and machine learning. Real-time global disease mapping. Mobile app available.</span>
                </div>
            </div>

            <div class="interactive-box">
                <h5>Global Surveillance Resources</h5>
                <ul class="resource-list">
                    <li><a href="https://extranet.who.int/goarn/">GOARN Portal</a> - WHO Global Outbreak Alert and Response Network</li>
                    <li><a href="https://www.who.int/emergencies/disease-outbreak-news">WHO Disease Outbreak News</a> - Weekly outbreak updates</li>
                    <li><a href="https://promedmail.org/">ProMED-mail</a> - Expert-moderated disease surveillance</li>
                    <li><a href="https://www.healthmap.org/en/">HealthMap.org</a> - Real-time disease mapping</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>📱 Digital Epidemiology Revolution</h4>

            <div class="concept-box">
                <h5>Syndromic Surveillance</h5>
                <p>Real-time monitoring of health indicators before laboratory confirmation. Examples include hospital emergency department surveillance, influenza-like illness tracking, and analysis of drug sales patterns.</p>
            </div>

            <div class="concept-box">
                <h5>Social Media Monitoring</h5>
                <p>Natural language processing and sentiment analysis of platforms like Twitter, Facebook, WeChat, and WhatsApp for early outbreak detection and misinformation tracking.</p>
            </div>

            <div class="concept-box">
                <h5>Genomic Surveillance</h5>
                <p>Real-time pathogen evolution tracking through platforms like GISAID (millions of viral genomes from 180+ countries) and Nextstrain (real-time phylogenetic analysis and visualization).</p>
            </div>

            <div class="interactive-box">
                <h5>Digital Surveillance Tools</h5>
                <ul class="resource-list">
                    <li><a href="https://www.cdc.gov/nssp/">CDC NSSP</a> - National Syndromic Surveillance Program</li>
                    <li><a href="https://www.gisaid.org/">GISAID.org</a> - Global sharing of viral sequences</li>
                    <li><a href="https://nextstrain.org/">Nextstrain.org</a> - Real-time phylogenetic analysis</li>
                    <li><a href="https://covid.joinzoe.com/">COVID Symptom Study</a> - Citizen science approach</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>📲 Mobile Health Technologies</h4>

            <div class="examples-grid">
                <div class="example-card">
                    <strong>Contact Tracing Apps</strong>
                    <span>Bluetooth Low Energy proximity detection. Privacy approaches: centralized vs. decentralized models.</span>
                </div>
                <div class="example-card">
                    <strong>Symptom Tracking Apps</strong>
                    <span>Daily symptom reporting by millions of users. Large-scale epidemiological studies on disease progression.</span>
                </div>
                <div class="example-card">
                    <strong>Wastewater Surveillance</strong>
                    <span>Community-level monitoring through sewage analysis. Early warning system for population-level infections.</span>
                </div>
            </div>
        </div>
    </div>

    <div class="section">
        <h3 class="section-title">🌍 2.6 Environmental and Social Drivers</h3>
        <p class="section-subtitle">The broader context that shapes pandemic risk</p>

        <div class="subsection">
            <h4>🌳 Environmental Drivers of Pandemic Risk</h4>

            <div class="concept-box">
                <h5>Deforestation and Habitat Destruction</h5>
                <p><strong>The Spillover Connection:</strong> 75% of emerging infectious diseases are zoonotic. Habitat destruction forces wildlife into human contact, with tropical regions being hotspots due to high biodiversity and deforestation rates.</p>
            </div>

            <div class="stats-highlight">
                <div class="stat-item">
                    <div class="stat-value">10M</div>
                    <div class="stat-label">Hectares of forest lost annually</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value">1000x</div>
                    <div class="stat-label">Current extinction rate vs. natural background</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value">$1T</div>
                    <div class="stat-label">Annual ecosystem service losses</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value">75%</div>
                    <div class="stat-label">Emerging diseases that are zoonotic</div>
                </div>
            </div>

            <div class="interactive-box">
                <h5>Forest Monitoring Resources</h5>
                <ul class="resource-list">
                    <li><a href="https://www.globalforestwatch.org/">Global Forest Watch</a> - Real-time deforestation tracking</li>
                    <li><a href="https://earthenginepartners.appspot.com/science-2013-global-forest">Hansen Global Forest Change</a> - University of Maryland dataset</li>
                    <li><a href="http://www.obt.inpe.br/OBT/assuntos/programas/amazonia/prodes">PRODES Amazon</a> - Brazilian Amazon monitoring</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>🏙️ Urbanization and Megacity Challenges</h4>

            <div class="concept-box">
                <h5>Urban Disease Transmission</h5>
                <p>Population density facilitates respiratory disease spread. Transportation hubs serve as mixing points. Informal settlements have poor sanitation and crowded conditions. Air pollution increases respiratory disease susceptibility.</p>
            </div>

            <div class="stats-highlight">
                <div class="stat-item">
                    <div class="stat-value">55%</div>
                    <div class="stat-label">Current world population in cities</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value">68%</div>
                    <div class="stat-label">Projected urban population by 2050</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value">33</div>
                    <div class="stat-label">Cities with >10 million people</div>
                </div>
                <div class="stat-item">
                    <div class="stat-value">1B</div>
                    <div class="stat-label">People in informal settlements</div>
                </div>
            </div>

            <div class="key-points">
                <h5>Urban Health Vulnerabilities</h5>
                <ul class="points-list">
                    <li>2 billion people lack safely managed drinking water</li>
                    <li>3.6 billion lack safely managed sanitation</li>
                    <li>90% of urban dwellers breathe polluted air</li>
                    <li>1 billion people live in informal settlements</li>
                </ul>
            </div>
        </div>

        <div class="subsection">
            <h4>🌐 Globalization and Connectivity</h4>

            <div class="examples-grid">
                <div class="example-card">
                    <strong>Transportation Networks</strong>
                    <span>4.5 billion passengers annually pre-COVID. Disease can reach anywhere within 24-36 hours. Major airports as epidemic amplifiers.</span>
                </div>
                <div class="example-card">
                    <strong>Digital Connectivity</strong>
                    <span>Information spreads faster than pathogens. Enables global coordination and data sharing. Misinformation can undermine response.</span>
                </div>
                <div class="example-card">
                    <strong>Economic Integration</strong>
                    <span>11 billion tons of maritime cargo annually. Supply chain vulnerabilities revealed during COVID-19. Economic concerns can delay response.</span>
                </div>
            </div>

            <div class="interactive-box">
                <h5>Global Connectivity Resources</h5>
                <ul class="resource-list">
                    <li><a href="https://www.iata.org/en/pressroom/pr/2023-03-07-01/">IATA Travel Statistics</a> - Aviation data and trends</li>
                    <li><a href="https://ourworldindata.org/trade-and-globalization">Our World in Data: Trade</a> - Global trade patterns</li>
                    <li><a href="https://unhabitat.org/">UN-Habitat</a> - Urban development and health</li>
                    <li><a href="https://www.who.int/healthpromotion/healthy-cities/en/">Healthy Cities Network</a> - WHO initiative</li>
                </ul>
            </div>
        </div>
    </div>

</div>

<!-- Add your next sections here -->

## Next Steps

Continue with the [Advanced Topics](/advanced/) section or explore additional [Resources](/resources/).
