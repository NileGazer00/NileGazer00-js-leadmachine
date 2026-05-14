<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NileGazer00</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; background: #0d1117; color: #c9d1d9; line-height: 1.6; }
        .container { max-width: 800px; margin: 0 auto; padding: 40px 20px; }
        .header { text-align: center; padding: 60px 0 40px; }
        .avatar { width: 150px; height: 150px; border-radius: 50%; border: 3px solid #58a6ff; margin-bottom: 20px; }
        h1 { font-size: 2.5em; color: #f0f6fc; }
        .tagline { font-size: 1.3em; color: #8b949e; margin-top: 10px; }
        .roles { display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-top: 25px; }
        .role { background: #161b22; border: 1px solid #30363d; padding: 8px 16px; border-radius: 20px; font-size: 0.9em; color: #58a6ff; }
        .section { margin: 50px 0; }
        h2 { font-size: 1.6em; color: #f0f6fc; margin-bottom: 20px; padding-bottom: 10px; border-bottom: 1px solid #21262d; }
        .projects { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        .project { background: #161b22; border: 1px solid #30363d; border-radius: 12px; padding: 25px; transition: border-color 0.3s; }
        .project:hover { border-color: #58a6ff; }
        .project h3 { color: #f0f6fc; margin-bottom: 8px; }
        .project p { color: #8b949e; font-size: 0.95em; margin-bottom: 15px; }
        .project a { color: #58a6ff; text-decoration: none; font-size: 0.9em; }
        .project a:hover { text-decoration: underline; }
        .tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 15px; }
        .tag { background: #1f2937; color: #8b949e; padding: 3px 10px; border-radius: 12px; font-size: 0.8em; }
        .skills { display: flex; flex-wrap: wrap; gap: 10px; }
        .skill { background: #161b22; border: 1px solid #30363d; padding: 10px 20px; border-radius: 8px; color: #c9d1d9; font-size: 0.95em; }
        .stats { display: flex; justify-content: center; gap: 40px; margin: 30px 0; }
        .stat { text-align: center; }
        .stat-num { font-size: 2em; color: #58a6ff; font-weight: bold; }
        .stat-label { color: #8b949e; font-size: 0.9em; }
        .links { display: flex; justify-content: center; gap: 15px; margin-top: 20px; }
        .link { color: #8b949e; text-decoration: none; font-size: 1.1em; }
        .link:hover { color: #58a6ff; }
        .currently { background: #161b22; border: 1px solid #30363d; border-radius: 12px; padding: 25px; }
        .currently h3 { color: #3fb950; margin-bottom: 10px; }
        .currently p { color: #8b949e; }
        @media (max-width: 600px) { .projects { grid-template-columns: 1fr; } .stats { gap: 20px; } }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <img class="avatar" src="https://avatars.githubusercontent.com/u/185620920?v=4" alt="NileGazer00">
            <h1>NileGazer00</h1>
            <p class="tagline">Full Stack Developer · Open Source Contributor</p>
            <div class="roles">
                <span class="role">JavaScript</span>
                <span class="role">TypeScript</span>
                <span class="role">React</span>
                <span class="role">Node.js</span>
                <span class="role">Python</span>
                <span class="role">UI/UX Design</span>
            </div>
        </div>

        <div class="stats">
            <div class="stat">
                <div class="stat-num">🟢</div>
                <div class="stat-label">Available for collabs</div>
            </div>
        </div>

        <div class="section">
            <h2>Projects</h2>
            <div class="projects">
                <div class="project">
                    <div class="tags">
                        <span class="tag">JavaScript</span>
                        <span class="tag">Open Source</span>
                        <span class="tag">MIT</span>
                    </div>
                    <h3>LeadGen.js</h3>
                    <p>Zero-dependency JavaScript library for capturing leads directly to Google Sheets. No backend required.</p>
                    <a href="https://github.com/NileGazer00/leadgen.js">View Repository →</a>
                </div>
                <div class="project">
                    <div class="tags">
                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">Documentation</span>
                    </div>
                    <h3>LeadGen.js Docs</h3>
                    <p>Comprehensive documentation site with API reference, examples, and troubleshooting guides.</p>
                    <a href="https://github.com/NileGazer00/NileGazer00-js-leadmachine">View Repository →</a>
                </div>
            </div>
        </div>

        <div class="section">
            <h2>Tech Stack</h2>
            <div class="skills">
                <span class="skill">JavaScript</span>
                <span class="skill">TypeScript</span>
                <span class="skill">React</span>
                <span class="skill">Vue.js</span>
                <span class="skill">Node.js</span>
                <span class="skill">Express</span>
                <span class="skill">Python</span>
                <span class="skill">HTML5</span>
                <span class="skill">CSS3</span>
                <span class="skill">Tailwind CSS</span>
                <span class="skill">MongoDB</span>
                <span class="skill">PostgreSQL</span>
                <span class="skill">Git</span>
                <span class="skill">Figma</span>
                <span class="skill">REST APIs</span>
            </div>
        </div>

        <div class="section">
            <div class="currently">
                <h3>Currently working on</h3>
                <p>Building open-source JavaScript tools and contributing to the developer community. Always exploring new technologies and improving existing workflows.</p>
            </div>
        </div>

        <div class="links">
            <a class="link" href="https://github.com/NileGazer00">GitHub</a>
            <a class="link" href="https://paypal.me/LeadGenLabs">Support</a>
        </div>
    </div>
</body>
</html>
