<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NileGazer00</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; background: #0d1117; color: #c9d1d9; line-height: 1.6; overflow-x: hidden; }
        .container { max-width: 900px; margin: 0 auto; padding: 40px 20px; }
        .header { text-align: center; padding: 60px 0 50px; position: relative; }
        .header::before { content: ''; position: absolute; top: -100px; left: 50%; transform: translateX(-50%); width: 500px; height: 500px; background: radial-gradient(circle, rgba(88,166,255,0.08) 0%, transparent 70%); pointer-events: none; }
        .avatar-wrapper { position: relative; display: inline-block; margin-bottom: 25px; }
        .avatar { width: 160px; height: 160px; border-radius: 50%; border: 3px solid transparent; background: linear-gradient(#0d1117, #0d1117) padding-box, linear-gradient(135deg, #58a6ff, #bc8cff, #f778ba) border-box; position: relative; z-index: 1; }
        .status-dot { position: absolute; bottom: 10px; right: 10px; width: 20px; height: 20px; background: #3fb950; border: 3px solid #0d1117; border-radius: 50%; z-index: 2; }
        h1 { font-size: 2.8em; color: #f0f6fc; letter-spacing: -0.5px; }
        .tagline { font-size: 1.2em; color: #8b949e; margin-top: 8px; }
        .typing { border-right: 2px solid #58a6ff; padding-right: 5px; animation: blink 1s infinite; }
        @keyframes blink { 0%,50% { border-color: #58a6ff; } 51%,100% { border-color: transparent; } }
        .roles { display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-top: 25px; }
        .role { background: linear-gradient(135deg, rgba(88,166,255,0.1), rgba(188,140,255,0.1)); border: 1px solid rgba(88,166,255,0.2); padding: 8px 18px; border-radius: 25px; font-size: 0.85em; color: #79c0ff; font-weight: 500; transition: all 0.3s; }
        .role:hover { border-color: #58a6ff; transform: translateY(-2px); box-shadow: 0 4px 15px rgba(88,166,255,0.15); }
        .socials { display: flex; justify-content: center; gap: 20px; margin-top: 30px; }
        .social { color: #8b949e; text-decoration: none; font-size: 0.95em; display: flex; align-items: center; gap: 6px; transition: color 0.3s; }
        .social:hover { color: #58a6ff; }
        .stats-row { display: flex; justify-content: center; gap: 30px; margin: 40px 0; flex-wrap: wrap; }
        .stat-card { background: #161b22; border: 1px solid #21262d; border-radius: 12px; padding: 20px 30px; text-align: center; min-width: 140px; transition: all 0.3s; }
        .stat-card:hover { border-color: #30363d; transform: translateY(-3px); box-shadow: 0 8px 25px rgba(0,0,0,0.3); }
        .stat-num { font-size: 2em; font-weight: 700; background: linear-gradient(135deg, #58a6ff, #bc8cff); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
        .stat-label { color: #8b949e; font-size: 0.85em; margin-top: 5px; }
        .section { margin: 60px 0; }
        .section-header { display: flex; align-items: center; gap: 12px; margin-bottom: 25px; }
        .section-icon { font-size: 1.3em; }
        h2 { font-size: 1.5em; color: #f0f6fc; }
        .section-line { flex: 1; height: 1px; background: linear-gradient(90deg, #21262d, transparent); }
        .projects { display: grid; grid-template-columns: 1fr 1fr; gap: 20px; }
        .project { background: #161b22; border: 1px solid #21262d; border-radius: 16px; padding: 28px; transition: all 0.3s; position: relative; overflow: hidden; }
        .project::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, #58a6ff, #bc8cff); opacity: 0; transition: opacity 0.3s; }
        .project:hover { border-color: #30363d; transform: translateY(-4px); box-shadow: 0 12px 35px rgba(0,0,0,0.4); }
        .project:hover::before { opacity: 1; }
        .project-header { display: flex; align-items: center; gap: 12px; margin-bottom: 12px; }
        .project-icon { width: 40px; height: 40px; background: linear-gradient(135deg, #58a6ff, #bc8cff); border-radius: 10px; display: flex; align-items: center; justify-content: center; font-size: 1.2em; }
        .project h3 { color: #f0f6fc; font-size: 1.1em; }
        .project p { color: #8b949e; font-size: 0.92em; margin-bottom: 18px; line-height: 1.7; }
        .tags { display: flex; flex-wrap: wrap; gap: 6px; margin-bottom: 18px; }
        .tag { background: rgba(88,166,255,0.08); color: #79c0ff; padding: 4px 12px; border-radius: 20px; font-size: 0.78em; border: 1px solid rgba(88,166,255,0.12); }
        .project-link { color: #58a6ff; text-decoration: none; font-size: 0.9em; font-weight: 500; display: inline-flex; align-items: center; gap: 6px; transition: gap 0.3s; }
        .project-link:hover { gap: 10px; }
        .skills-grid { display: flex; flex-wrap: wrap; gap: 12px; }
        .skill { background: #161b22; border: 1px solid #21262d; padding: 12px 22px; border-radius: 10px; color: #c9d1d9; font-size: 0.92em; transition: all 0.3s; display: flex; align-items: center; gap: 8px; }
        .skill:hover { border-color: #58a6ff; color: #f0f6fc; transform: translateY(-2px); box-shadow: 0 4px 15px rgba(88,166,255,0.1); }
        .skill-dot { width: 8px; height: 8px; border-radius: 50%; }
        .skill-cat { width: 100%; margin-top: 15px; margin-bottom: 5px; font-size: 0.8em; color: #58a6ff; text-transform: uppercase; letter-spacing: 1px; font-weight: 600; }
        .currently { background: linear-gradient(135deg, rgba(63,185,80,0.05), rgba(88,166,255,0.05)); border: 1px solid rgba(63,185,80,0.15); border-radius: 16px; padding: 28px; display: flex; gap: 20px; align-items: flex-start; }
        .currently-icon { font-size: 2em; flex-shrink: 0; }
        .currently h3 { color: #3fb950; margin-bottom: 8px; font-size: 1.1em; }
        .currently p { color: #8b949e; line-height: 1.7; }
        .github-stats { display: flex; justify-content: center; gap: 15px; margin-top: 20px; flex-wrap: wrap; }
        .github-stats img { border-radius: 8px; border: 1px solid #21262d; }
        .footer { text-align: center; padding: 40px 0; margin-top: 40px; border-top: 1px solid #21262d; }
        .footer p { color: #484f58; font-size: 0.85em; }
        .footer a { color: #8b949e; text-decoration: none; }
        .footer a:hover { color: #58a6ff; }
        @keyframes fadeInUp { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
        .fade-in { animation: fadeInUp 0.6s ease-out forwards; }
        .fade-in-delay-1 { animation-delay: 0.1s; opacity: 0; }
        .fade-in-delay-2 { animation-delay: 0.2s; opacity: 0; }
        .fade-in-delay-3 { animation-delay: 0.3s; opacity: 0; }
        .fade-in-delay-4 { animation-delay: 0.4s; opacity: 0; }
        @media (max-width: 600px) { .projects { grid-template-columns: 1fr; } .stats-row { flex-direction: column; align-items: center; } h1 { font-size: 2em; } .avatar { width: 130px; height: 130px; } }
    </style>
</head>
<body>
    <div class="container">
        <div class="header fade-in">
            <div class="avatar-wrapper">
                <img class="avatar" src="https://avatars.githubusercontent.com/u/185620920?v=4" alt="NileGazer00">
                <div class="status-dot"></div>
            </div>
            <h1>Hey, I'm NileGazer00<span class="typing"></span></h1>
            <p class="tagline">Full Stack Developer · Open Source Contributor</p>
            <div class="roles">
                <span class="role">JavaScript</span>
                <span class="role">TypeScript</span>
                <span class="role">React</span>
                <span class="role">Node.js</span>
                <span class="role">Python</span>
                <span class="role">UI/UX</span>
            </div>
            <div class="socials">
                <a class="social" href="https://github.com/NileGazer00">GitHub</a>
                <a class="social" href="https://nilegazer00.github.io/NileGazer00-js-leadmachine">Website</a>
                <a class="social" href="https://paypal.me/LeadGenLabs">Support</a>
            </div>
        </div>

        <div class="stats-row fade-in fade-in-delay-1">
            <div class="stat-card">
                <div class="stat-num">27+</div>
                <div class="stat-label">Contributions</div>
            </div>
            <div class="stat-card">
                <div class="stat-num">3</div>
                <div class="stat-label">Repositories</div>
            </div>
            <div class="stat-card">
                <div class="stat-num">🟢</div>
                <div class="stat-label">Open to Collabs</div>
            </div>
        </div>

        <div class="section fade-in fade-in-delay-2">
            <div class="section-header">
                <span class="section-icon">🚀</span>
                <h2>Featured Projects</h2>
                <div class="section-line"></div>
            </div>
            <div class="projects">
                <div class="project">
                    <div class="project-header">
                        <div class="project-icon">📜</div>
                        <h3>LeadGen.js</h3>
                    </div>
                    <p>Zero-dependency JavaScript library for capturing leads directly to Google Sheets. No backend required.</p>
                    <div class="tags">
                        <span class="tag">JavaScript</span>
                        <span class="tag">Open Source</span>
                        <span class="tag">MIT</span>
                        <span class="tag">Zero Deps</span>
                    </div>
                    <a class="project-link" href="https://github.com/NileGazer00/leadgen.js">View Repository →</a>
                </div>
                <div class="project">
                    <div class="project-header">
                        <div class="project-icon">📖</div>
                        <h3>LeadGen.js Docs</h3>
                    </div>
                    <p>Comprehensive documentation with API reference, code examples, troubleshooting, and integration guides.</p>
                    <div class="tags">
                        <span class="tag">HTML</span>
                        <span class="tag">CSS</span>
                        <span class="tag">Documentation</span>
                        <span class="tag">js.org</span>
                    </div>
                    <a class="project-link" href="https://github.com/NileGazer00/NileGazer00-js-leadmachine">View Repository →</a>
                </div>
            </div>
        </div>

        <div class="section fade-in fade-in-delay-3">
            <div class="section-header">
                <span class="section-icon">⚡</span>
                <h2>Tech Stack</h2>
                <div class="section-line"></div>
            </div>
            <div class="skills-grid">
                <div class="skill-cat">Frontend</div>
                <span class="skill"><span class="skill-dot" style="background:#f7df1e"></span>JavaScript</span>
                <span class="skill"><span class="skill-dot" style="background:#3178c6"></span>TypeScript</span>
                <span class="skill"><span class="skill-dot" style="background:#61dafb"></span>React</span>
                <span class="skill"><span class="skill-dot" style="background:#42b883"></span>Vue.js</span>
                <span class="skill"><span class="skill-dot" style="background:#e34f26"></span>HTML5</span>
                <span class="skill"><span class="skill-dot" style="background:#264de4"></span>CSS3</span>
                <span class="skill"><span class="skill-dot" style="background:#06b6d4"></span>Tailwind</span>
                <span class="skill-cat">Backend</span>
                <span class="skill"><span class="skill-dot" style="background:#68a063"></span>Node.js</span>
                <span class="skill"><span class="skill-dot" style="background:#ffffff"></span>Express</span>
                <span class="skill"><span class="skill-dot" style="background:#47a248"></span>MongoDB</span>
                <span class="skill"><span class="skill-dot" style="background:#336791"></span>PostgreSQL</span>
                <span class="skill-cat">Tools</span>
                <span class="skill"><span class="skill-dot" style="background:#f05032"></span>Git</span>
                <span class="skill"><span class="skill-dot" style="background:#a259ff"></span>Figma</span>
                <span class="skill"><span class="skill-dot" style="background:#3776ab"></span>Python</span>
                <span class="skill"><span class="skill-dot" style="background:#58a6ff"></span>REST APIs</span>
            </div>
        </div>

        <div class="section fade-in fade-in-delay-4">
            <div class="currently">
                <div class="currently-icon">🔨</div>
                <div>
                    <h3>Currently working on</h3>
                    <p>Building open-source JavaScript tools for the developer community. Exploring new technologies and contributing to projects that make developers' lives easier.</p>
                </div>
            </div>
        </div>

        <div class="github-stats fade-in">
            <img src="https://github-readme-stats.vercel.app/api?username=NileGazer00&show_icons=true&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9" alt="GitHub Stats">
            <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=NileGazer00&layout=compact&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9" alt="Top Languages">
        </div>

        <div class="footer">
            <p>Built with ❤️ by <a href="https://github.com/NileGazer00">NileGazer00</a></p>
        </div>
    </div>
</body>
</html>
