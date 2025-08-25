---
layout: default
title: Home
---

<div class="hero">
  <div class="wrapper">
    <h1 class="hero-title">{{ site.title }}</h1>
    <p class="hero-tagline">{{ site.description }}</p>
    
    <div class="hero-buttons">
      <a href="#features" class="btn btn-primary">Explore Features</a>
      <a href="mailto:{{ site.contact_email }}" class="btn btn-secondary">Get Updates</a>
    </div>
  </div>
</div>

<div class="features" id="features">
  <div class="wrapper">
    <h2 style="text-align: center; margin-bottom: 3rem; color: var(--budsy-h2);">Manage Your Cannabis Journey with budsyapp</h2>
    
    <div class="feature-grid">
      <div class="feature-card">
        <h3>🔢 Manage Your Units</h3>
        <p>Log MMJ units by day, time, and quantity. See expected return of units in real time with a smart 30-day rolling algorithm. Easily edit previous logs for complete accuracy.</p>
      </div>
      
      <div class="feature-card">
        <h3>📅 Unit History View</h3>
        <p>Visual calendar with color-coded unit usage (e.g., blue = 1 unit, pink = 4+). List view for quick browsing and edits of your consumption patterns.</p>
      </div>
      
      <div class="feature-card">
        <h3>🧪 Strain Journal</h3>
        <p>Record strain name, THC %, terpene profile. Rate experiences and note methods, doses, reactions (e.g., euphoric, anxious). Filter entries by terpene, THC, rating, or alphabetically.</p>
      </div>
      
      <div class="feature-card">
        <h3>⚙️ Personalize Settings</h3>
        <p>Rename "units" to your own terminology. Customize your allotment and rolling period to match your specific medical needs and preferences.</p>
      </div>
      
      <div class="feature-card">
        <h3>📊 Smart Analytics</h3>
        <p>Get insights into your usage patterns with beautiful charts and graphs. Monitor trends over time to optimize your medical marijuana experience.</p>
      </div>
      
      <div class="feature-card">
        <h3>🔒 Privacy First</h3>
        <p>Your sensitive medical data stays secure and private. We believe in patient confidentiality and data protection as core principles.</p>
      </div>
    </div>
  </div>
</div>

<div style="background: linear-gradient(135deg, #F5F1E8 0%, #EFE9E0 100%); padding: 4rem 0; margin-top: 4rem; border-radius: 20px; border: 1px solid rgba(137, 177, 83, 0.3);">
  <div class="wrapper" style="text-align: center;">
    <h2 style="color: var(--budsy-h2); text-shadow: 0 0 15px rgba(214, 102, 130, 0.5);">About budsyapp</h2>
    <p style="font-size: 1.1rem; max-width: 600px; margin: 0 auto; line-height: 1.6; color: var(--budsy-text);">
      budsyapp is designed for medical marijuana patients who want to record and optimize their cannabis usage. 
      Built with a focus on simplicity, privacy, and helpful insights to support your wellness journey.
    </p>
    
    <div style="margin-top: 2rem;">
      <a href="https://github.com/{{ site.github_org }}" class="btn btn-secondary" target="_blank" rel="noopener noreferrer">Follow Development</a>
    </div>
    
    <h3 style="margin-top: 3rem; color: var(--budsy-h2); text-shadow: 0 0 10px rgba(214, 102, 130, 0.4);">Support the Project</h3>
    <p style="color: var(--budsy-text);">Help us build budsyapp:</p>
    <div style="display: flex; justify-content: center; margin-top: 1rem;">
      <ul style="list-style: none; padding: 0; color: var(--budsy-text); text-align: left; max-width: 400px; margin: 0 0 0 2rem;">
        <li style="margin-bottom: 0.5rem;">🐛 Report bugs or suggest features</li>
        <li style="margin-bottom: 0.5rem;">🔄 Share budsyapp with others</li>
        <li style="margin-bottom: 0.5rem;">💚 Spread awareness about responsible usage</li>
      </ul>
    </div>
  </div>
</div>

<div style="text-align: center; padding: 3rem 0; background: linear-gradient(135deg, #FFF8E7 0%, #F5F1E8 100%); color: var(--budsy-text); margin: 4rem -15px 0 -15px; border-top: 1px solid rgba(137, 177, 83, 0.2);">
  <div class="wrapper">
    <h2 style="color: var(--budsy-h2); text-shadow: 0 0 15px rgba(214, 102, 130, 0.5);">Ready to Get Started?</h2>
    <p style="font-size: 1.1rem; margin-bottom: 2rem;">Join the budsyapp community and take control of your cannabis journey.</p>
    <a href="#features" class="btn btn-primary">Coming Soon</a>
  </div>
</div>
