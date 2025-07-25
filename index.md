---
layout: default
---

<style>
/* Enhanced styles for the pandemic science guide */
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

.section-title {
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

.section-title i {
    margin-right: 1rem;
    color: rgba(255, 255, 255, 0.9);
}

.highlight-box {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(10px);
    border-radius: 20px;
    padding: 2.5rem;
    margin: 2rem auto;
    border: 1px solid rgba(255, 255, 255, 0.2);
    max-width: 800px;
    position: relative;
    z-index: 2;
}

.highlight-box h3 {
    font-size: 1.8rem;
    margin-bottom: 1rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 1rem;
}

.highlight-box h3::before {
    content: '💡';
    font-size: 1.5rem;
}

.highlight-box p {
    font-size: 1.2rem;
    line-height: 1.8;
    margin: 0;
    font-weight: 500;
}

.stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
    margin: 3rem 0;
    position: relative;
    z-index: 2;
}

.stat-card {
    background: rgba(255, 255, 255, 0.15);
    backdrop-filter: blur(10px);
    border-radius: 16px;
    padding: 2rem 1rem;
    text-align: center;
    border: 1px solid rgba(255, 255, 255, 0.2);
    transition: all 0.3s ease;
    cursor: pointer;
}

.stat-card:hover {
    transform: translateY(-8px);
    background: rgba(255, 255, 255, 0.25);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
}

.stat-number {
    font-size: 2.5rem;
    font-weight: 900;
    color: #fff;
    margin-bottom: 0.5rem;
    display: block;
}

.stat-label {
    color: rgba(255, 255, 255, 0.9);
    font-size: 1rem;
    font-weight: 600;
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

.section-intro {
    border-left: 5px solid #667eea;
    padding-left: 2rem;
    margin-bottom: 3rem;
    background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
    padding: 2rem;
    border-radius: 12px;
}

.section-intro h2 {
    font-size: 2.5rem;
    color: #1e293b;
    margin-bottom: 0.5rem;
    font-weight: 800;
}

.section-intro .subtitle {
    font-size: 1.2rem;
    color: #64748b;
    font-weight: 500;
    margin: 0;
}

.subsection {
    margin: 3rem 0;
    padding: 2.5rem;
    background: linear-gradient(135deg, #f8fafc 0%, #f1f5f9 100%);
    border-radius: 20px;
    border-left: 6px solid #667eea;
    position: relative;
}

.subsection h3 {
    font-size: 1.8rem;
    color: #1e293b;
    margin-bottom: 1.5rem;
    font-weight: 700;
    display: flex;
    align-items: center;
    gap: 1rem;
}

.subsection h3::before {
    content: attr(data-icon);
    font-size: 1.5rem;
}

.subsection p {
    font-size: 1.1rem;
    line-height: 1.8;
    color: #475569;
    margin-bottom: 1.5rem;
}

.example-box {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    padding: 2rem;
    border-radius: 16px;
    margin: 2rem 0;
    position: relative;
    overflow: hidden;
}

.example-box::before {
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

.example-box h4 {
    margin-bottom: 1rem;
    font-size: 1.3rem;
    font-weight: 700;
}

.example-list {
    list-style: none;
    padding: 0;
}

.example-list li {
    padding: 1rem 0;
    padding-left: 2.5rem;
    position: relative;
    font-size: 1.05rem;
    line-height: 1.7;
    border-bottom: 1px solid rgba(255, 255, 255, 0.2);
}

.example-list li:last-child {
    border-bottom: none;
}

.example-list li::before {
    content: '🔗';
    position: absolute;
    left: 0;
    top: 1rem;
    font-size: 1.2rem;
}

.guide-components {
    background: linear-gradient(135deg, #1e293b 0%, #334155 100%);
    color: white;
    padding: 3rem;
    border-radius: 20px;
    margin: 3rem 0;
}

.guide-components h4 {
    font-size: 1.6rem;
    margin-bottom: 2rem;
    font-weight: 700;
    text-align: center;
}

.components-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.5rem;
}

.component-card {
    background: rgba(255, 255, 255, 0.1);
    padding: 2rem;
    border-radius: 16px;
    border: 1px solid rgba(255, 255, 255, 0.2);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
}

.component-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 3px;
    background: linear-gradient(90deg, #667eea, #764ba2);
}

.component-card:hover {
    background: rgba(255, 255, 255, 0.2);
    transform: translateY(-5px);
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
}

.component-card strong {
    display: block;
    font-size: 1.2rem;
    margin-bottom: 1rem;
    color: #e2e8f0;
    font-weight: 600;
}

.component-card p {
    color: rgba(255, 255, 255, 0.8);
    line-height: 1.6;
    margin: 0;
}

.fade-in-up {
    animation: fadeInUp 0.8s ease-out;
}

/* Logo section */
.logo-section {
    text-align: center;
    margin: var(--space-2xl) 0;
    padding: var(--space-xl);
    background: var(--bg-primary);
    border-radius: var(--border-radius-lg);
    box-shadow: var(--shadow-md);
    border: 1px solid var(--border-color);
}

.appex-logo {
    max-width: 300px;
    height: auto;
    margin-bottom: var(--space-lg);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-sm);
}

.contact-info {
    font-size: 1.1rem;
    color: var(--primary-blue);
    font-weight: 600;
    margin-bottom: var(--space-md);
}

.contact-info a {
    color: var(--primary-blue);
    text-decoration: none;
    transition: var(--transition);
}

.contact-info a:hover {
    color: var(--secondary-teal);
    text-decoration: underline;
}

/* NSF acknowledgment */
.nsf-acknowledgment {
    background: var(--bg-secondary);
    border-left: 4px solid var(--accent-orange);
    padding: var(--space-lg);
    margin: var(--space-2xl) 0;
    border-radius: 0 var(--border-radius) var(--border-radius) 0;
    font-size: 0.95rem;
    line-height: 1.7;
    color: var(--text-secondary);
}

.nsf-acknowledgment strong {
    color: var(--text-primary);
}

@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
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
    
    .section-title {
        font-size: 2.2rem;
    }
    
    .content-wrapper {
        padding: 2rem;
        margin: 1rem 0;
    }
    
    .stats-grid {
        grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
        gap: 1rem;
    }
    
    .components-grid {
        grid-template-columns: 1fr;
    }
    
    .appex-logo {
        max-width: 250px;
    }
    
    .logo-section {
        padding: var(--space-lg);
        margin: var(--space-lg) 0;
    }
    
    .contact-info {
        font-size: 1rem;
    }
    
    .nsf-acknowledgment {
        font-size: 0.9rem;
        padding: var(--space-md);
    }
}

/* Dark mode support */
@media (prefers-color-scheme: dark) {
    .content-wrapper {
        background: #1a1a1a;
        color: #e2e8f0;
    }
    
    .subsection {
        background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
    }
    
    .section-intro {
        background: linear-gradient(135deg, #2d3748 0%, #4a5568 100%);
    }
}
</style>

<!-- Hero Section -->
<section class="hero-section fade-in-up">
    <h2 class="section-title">
        <i class="fas fa-bullseye"></i>
        Understanding Pandemic Science
    </h2>
    <div class="highlight-box">
        <h3>The Driving Question</h3>
        <p>What allows a few isolated cases of an infectious disease to blossom into an outbreak and further expand into a true pandemic?</p>
    </div>
    
    <div class="stats-grid">
        <div class="stat-card">
            <div class="stat-number">6</div>
            <div class="stat-label">Expert Archetypes</div>
        </div>
        <div class="stat-card">
            <div class="stat-number">50+</div>
            <div class="stat-label">Interactive Resources</div>
        </div>
        <div class="stat-card">
            <div class="stat-number">100+</div>
            <div class="stat-label">Research Papers</div>
        </div>
        <div class="stat-card">
            <div class="stat-number">∞</div>
            <div class="stat-label">Learning Opportunities</div>
        </div>
    </div>
</section>

<div class="content-wrapper">
    <div class="section-intro">
        <h2>Part 1: Introduction to the APPEX Center and Its Mission</h2>
        <p class="subtitle">Bridging disciplines to understand pandemic complexity</p>
    </div>

    <div class="subsection">
        <h3 data-icon="🎯">The Driving Question</h3>
        <p>The Center for Analysis and Prediction of Pandemic Expansion (APPEX) is built around a single, critical question: <strong>What allows a few isolated cases of an infectious disease to blossom into an outbreak and further expand into a true pandemic?</strong></p>
        
        <p>The answer is never simple. It's not just about the biology of a virus; it's a "perfect storm" scenario where numerous factors—biological, environmental, social, and economic—interact in complex and often unpredictable ways. The APPEX Center's core mission is to dismantle the traditional silos that separate scientific disciplines, creating a new, integrated approach to pandemic science.</p>
    </div>

    <div class="subsection">
        <h3 data-icon="🔗">The Failure of Silos</h3>
        <p>Historically, pandemic research has been discipline-specific. Virologists studied viruses, economists studied economic impacts, and sociologists studied human behavior. While valuable, this isolated approach misses the crucial synergies between risk factors.</p>
        
        <div class="example-box">
            <h4>🌟 Real-World Examples of Interconnected Risks:</h4>
            <ul class="example-list">
                <li>A new housing development (Built Environment) pushes into a bat habitat (Ecological), increasing the chance of a zoonotic (animal-to-human) spillover event.</li>
                <li>A highly contagious but low-mortality virus (Biomedical) emerges, but misinformation on social media (Information Access) leads to widespread public distrust in basic health measures (Socio-behavioral).</li>
                <li>A government's initial response is slowed by economic concerns (Economic), allowing the pathogen to become established and spread globally.</li>
            </ul>
        </div>
        
        <p>The APPEX Center operates on the principle that the greatest breakthroughs will be found at the interfaces between disciplines.</p>
    </div>

    <div class="subsection">
        <h3 data-icon="🗺️">How to Use This Guide</h3>
        <p>This guide is designed for college-level students and aspiring researchers. It is structured around six core "Expert Archetypes," representing the key domains of knowledge essential for understanding pandemic risk.</p>
        
        <div class="guide-components">
            <h4>📚 For each archetype, you will find:</h4>
            <div class="components-grid">
                <div class="component-card">
                    <strong>🧠 Core Concepts</strong>
                    <p>The fundamental principles and scope of the discipline</p>
                </div>
                <div class="component-card">
                    <strong>🎯 Learning Objectives</strong>
                    <p>What you should be able to understand and do after studying the section</p>
                </div>
                <div class="component-card">
                    <strong>🔗 Key Challenges & Intersections</strong>
                    <p>How this field interacts with others to create complex pandemic scenarios</p>
                </div>
                <div class="component-card">
                    <strong>🔬 Foundational Research</strong>
                    <p>Summaries of and links to peer-reviewed papers that underpin the concepts</p>
                </div>
                <div class="component-card">
                    <strong>💻 Practical Upskilling</strong>
                    <p>Links to sample Jupyter Notebooks for hands-on data analysis and modeling</p>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- Logo and Contact Section -->
<section class="logo-section fade-in-up">
    <img src="{{ '/assets/images/appex-logo.png' | relative_url }}" alt="APPEX Logo" class="appex-logo">
    <div class="contact-info">
        <a href="mailto:contact@appex.org">contact@appex.org</a>
    </div>
</section>

<!-- NSF Acknowledgment -->
<section class="nsf-acknowledgment">
    <p><strong>Acknowledgment:</strong> This material is based upon work supported by the National Science Foundation under Award No. 2412115. Any opinions, findings and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the National Science Foundation.</p>
</section>