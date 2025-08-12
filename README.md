# psychic-funicular
Nothing much..
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Next Level Deo - Premium Services</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f0c29, #1a1a2e, #16213e);
            color: white;
            min-height: 100vh;
            padding: 20px;
            position: relative;
            overflow-x: hidden;
            background-attachment: fixed;
        }
        
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle, rgba(255,255,255,0.05) 1px, transparent 1px);
            background-size: 30px 30px;
            z-index: -1;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            position: relative;
            z-index: 2;
        }
        
        /* Header Styles */
        header {
            text-align: center;
            padding: 30px 0;
            position: relative;
            overflow: hidden;
            margin-bottom: 30px;
        }
        
        .title {
            font-size: 4.5rem;
            font-weight: 800;
            margin: 20px 0;
            background: linear-gradient(45deg, #ff4e8d, #8b00ff, #00c9ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            text-shadow: 0 0 20px rgba(255, 78, 141, 0.5);
            position: relative;
            display: inline-block;
            animation: shine 3s infinite alternate;
        }
        
        @keyframes shine {
            0% {
                text-shadow: 0 0 10px rgba(255, 78, 141, 0.5);
            }
            100% {
                text-shadow: 0 0 30px rgba(255, 78, 141, 0.8), 0 0 60px rgba(139, 0, 255, 0.6);
            }
        }
        
        .subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            color: #a3d5ff;
            font-weight: 300;
        }
        
        .info-bar {
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            border-radius: 50px;
            padding: 15px 30px;
            display: inline-flex;
            gap: 30px;
            margin: 20px 0;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .info-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 1.1rem;
        }
        
        /* Services Section */
        .services-container {
            margin: 40px 0;
        }
        
        .section-title {
            text-align: center;
            font-size: 2.2rem;
            margin-bottom: 30px;
            color: #8b00ff;
            text-shadow: 0 0 10px rgba(139, 0, 255, 0.5);
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }
        
        .service-card {
            background: rgba(255, 255, 255, 0.08);
            backdrop-filter: blur(10px);
            border-radius: 15px;
            padding: 25px;
            text-align: center;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
            min-height: 250px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
        }
        
        .service-card::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 70%);
            transform: rotate(30deg);
            pointer-events: none;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.3);
            background: rgba(255, 255, 255, 0.12);
            border-color: rgba(255, 78, 141, 0.3);
        }
        
        .service-icon {
            font-size: 3rem;
            margin-bottom: 20px;
            background: linear-gradient(45deg, #ff4e8d, #8b00ff);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        .service-name {
            font-size: 1.5rem;
            margin-bottom: 15px;
            color: #00c9ff;
        }
        
        .service-btn {
            background: linear-gradient(45deg, #ff4e8d, #8b00ff);
            color: white;
            border: none;
            padding: 12px 25px;
            border-radius: 50px;
            cursor: pointer;
            font-size: 1rem;
            font-weight: 600;
            transition: all 0.3s ease;
            margin-top: 10px;
            width: 100%;
            display: block;
            text-decoration: none;
        }
        
        .service-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(255, 78, 141, 0.4);
        }
        
        /* Business Hours */
        .hours-container {
            background: rgba(0, 0, 0, 0.3);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 25px;
            text-align: center;
            margin: 40px auto;
            max-width: 600px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.2);
        }
        
        .hours-title {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #00c9ff;
        }
        
        .hours-list {
            list-style: none;
            font-size: 1.2rem;
        }
        
        .hours-list li {
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .hours-list li:last-child {
            border-bottom: none;
        }
        
        .highlight {
            color: #ff4e8d;
            font-weight: bold;
        }
        
        /* Social Media Section */
        .social-container {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin: 40px 0;
            flex-wrap: wrap;
        }
        
        .social-btn {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 15px 30px;
            border-radius: 50px;
            font-size: 1.2rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            min-width: 250px;
            justify-content: center;
        }
        
        .whatsapp {
            background: linear-gradient(45deg, #25D366, #128C7E);
        }
        
        .instagram {
            background: linear-gradient(45deg, #833AB4, #FD1D1D, #FCB045);
        }
        
        .social-btn:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.3);
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 30px;
            font-size: 1.1rem;
            color: rgba(255, 255, 255, 0.7);
            margin-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        /* Battery Indicator */
        .battery-level {
            width: 60px;
            height: 30px;
            border: 2px solid white;
            border-radius: 5px;
            position: relative;
            display: inline-block;
            margin-left: 5px;
        }
        
        .battery-level::after {
            content: '';
            position: absolute;
            top: 7px;
            right: -6px;
            width: 4px;
            height: 14px;
            background: white;
            border-radius: 0 2px 2px 0;
        }
        
        .battery-fill {
            height: 100%;
            background: linear-gradient(90deg, #ff4e8d, #8b00ff);
            border-radius: 3px;
            transition: width 0.5s ease;
        }
        
        /* Music Player */
        .music-player {
            position: fixed;
            bottom: 20px;
            right: 20px;
            background: rgba(0, 0, 0, 0.6);
            backdrop-filter: blur(10px);
            border-radius: 50px;
            padding: 15px 25px;
            display: flex;
            align-items: center;
            gap: 15px;
            z-index: 100;
            border: 1px solid rgba(255, 255, 255, 0.1);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
        }
        
        .music-controls {
            display: flex;
            gap: 15px;
        }
        
        .music-btn {
            background: transparent;
            border: none;
            color: white;
            font-size: 1.2rem;
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: background 0.3s;
        }
        
        .music-btn:hover {
            background: rgba(255, 255, 255, 0.1);
        }
        
        .volume-container {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .volume-slider {
            width: 80px;
        }
        
        .music-title {
            margin-right: 15px;
            font-size: 0.9rem;
            color: #a3d5ff;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .title {
                font-size: 3rem;
            }
            
            .info-bar {
                flex-direction: column;
                gap: 15px;
                border-radius: 20px;
                padding: 15px;
            }
            
            .social-container {
                flex-direction: column;
                align-items: center;
            }
            
            .music-player {
                left: 20px;
                right: auto;
                width: calc(100% - 40px);
                justify-content: center;
            }
        }
        
        /* Animation for new service */
        @keyframes pop-in {
            0% {
                transform: scale(0.5);
                opacity: 0;
            }
            100% {
                transform: scale(1);
                opacity: 1;
            }
        }
        
        .new-service {
            animation: pop-in 0.5s ease-out;
        }
        
        /* Floating animation */
        @keyframes float {
            0% {
                transform: translateY(0px);
            }
            50% {
                transform: translateY(-10px);
            }
            100% {
                transform: translateY(0px);
            }
        }
        
        .floating {
            animation: float 3s ease-in-out infinite;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 class="title floating">Next_Level_deo</h1>
            <p class="subtitle">Premium Services at Lightning Speed</p>
            
            <div class="info-bar">
                <div class="info-item">
                    <i class="fas fa-battery-three-quarters"></i>
                    <span>Battery: </span>
                    <div class="battery-level">
                        <div class="battery-fill" id="battery-fill"></div>
                    </div>
                    <span id="battery-percent">95%</span>
                </div>
                <div class="info-item">
                    <i class="fas fa-clock"></i>
                    <span>Time: </span>
                    <span id="current-time">Loading...</span>
                </div>
            </div>
        </header>
        
        <div class="services-container">
            <h2 class="section-title">Our Premium Services</h2>
            <div class="services-grid" id="services-grid">
                <!-- Services will be added here dynamically -->
            </div>
            
            <div class="hours-container">
                <h3 class="hours-title">Opening Hours</h3>
                <ul class="hours-list">
                    <li>Monday - Friday: <span class="highlight">10:00 AM - 6:00 PM</span></li>
                    <li>Monday - Friday: <span class="highlight">9:10 PM - 12:00 AM</span></li>
                    <li>Saturday - Sunday: <span class="highlight">By Appointment Only</span></li>
                </ul>
            </div>
        </div>
        
        <div class="social-container">
            <a href="https://wa.me/254110550356" target="_blank" class="social-btn whatsapp">
                <i class="fab fa-whatsapp"></i>
                WhatsApp Us
            </a>
            <a href="https://instagram.com/next_level_mark" target="_blank" class="social-btn instagram">
                <i class="fab fa-instagram"></i>
                Follow on Instagram
            </a>
        </div>
        
        <footer>
            <p>© Mark <span id="current-year"></span> | Premium Services at Lightning Speed</p>
        </footer>
    </div>
    
    <!-- Music Player -->
    <div class="music-player">
        <span class="music-title">Background Music</span>
        <div class="music-controls">
            <button id="prev-btn" class="music-btn"><i class="fas fa-step-backward"></i></button>
            <button id="play-btn" class="music-btn"><i class="fas fa-play"></i></button>
            <button id="next-btn" class="music-btn"><i class="fas fa-step-forward"></i></button>
        </div>
        <div class="volume-container">
            <i class="fas fa-volume-up"></i>
            <input type="range" min="0" max="100" value="50" class="volume-slider" id="volume-slider">
        </div>
        <audio id="background-music" loop>
            <source src="https://files.catbox.moe/d1gplm.mp3">
        </audio>
    </div>
    
    <script>
        // Update current time
        function updateTime() {
            const now = new Date();
            const timeString = now.toLocaleTimeString([], {hour: '2-digit', minute:'2-digit'});
            document.getElementById('current-time').textContent = timeString;
        }
        
        // Update battery status (simulated for demonstration)
        function updateBattery() {
            // In a real implementation, you would use the Battery Status API
            // This is a simulation for demo purposes
            const batteryLevel = Math.floor(Math.random() * 30) + 70; // Random between 70-100%
            document.getElementById('battery-percent').textContent = `${batteryLevel}%`;
            document.getElementById('battery-fill').style.width = `${batteryLevel}%`;
        }
        
        // Set current year
        document.getElementById('current-year').textContent = new Date().getFullYear();
        
        // Services data with links
        const services = [
            { 
                name: "Instagram Unban", 
                icon: "fa-instagram",
                link: "https://instagram-unban.vercel.app/",
                description: "Restore your Instagram account quickly"
            },
            { 
                name: "WhatsApp Unban", 
                icon: "fa-whatsapp",
                link: "https://whatsapp-unban-mocha.vercel.app/",
                description: "Get your WhatsApp account back in minutes"
            },
            { 
                name: "My Website", 
                icon: "fa-globe",
                link: "https://nextlevelmark.vercel.app/",
                description: "Visit our main website for all services"
            },
            { 
                name: "Content Creation", 
                icon: "fa-pen-fancy",
                link: "https://chat.openai.com/",
                description: "AI-powered content creation tools"
            },
            { 
                name: "Video Downloader", 
                icon: "fa-download",
                link: "https://yt1s.com",
                description: "Download videos from popular platforms"
            }
        ];
        
        // Render services
        function renderServices() {
            const servicesGrid = document.getElementById('services-grid');
            servicesGrid.innerHTML = '';
            
            services.forEach(service => {
                const serviceCard = document.createElement('div');
                serviceCard.className = 'service-card';
                serviceCard.innerHTML = `
                    <div>
                        <div class="service-icon">
                            <i class="fab ${service.icon}"></i>
                        </div>
                        <h3 class="service-name">${service.name}</h3>
                        <p>${service.description}</p>
                    </div>
                    <a href="${service.link}" target="_blank" class="service-btn">Access Service</a>
                `;
                servicesGrid.appendChild(serviceCard);
            });
        }
        
        // Add new service (simulating adding a new service)
        function addNewService(name, icon, link, description) {
            services.push({ name, icon, link, description });
            
            // Re-render services with animation for the new one
            renderServices();
            
            // Animate the last card (the new one)
            const cards = document.querySelectorAll('.service-card');
            if (cards.length > 0) {
                cards[cards.length - 1].classList.add('new-service');
            }
        }
        
        // Music player functionality
        const music = document.getElementById('background-music');
        const playBtn = document.getElementById('play-btn');
        const volumeSlider = document.getElementById('volume-slider');
        let isPlaying = false;
        
        // Play/Pause toggle
        playBtn.addEventListener('click', () => {
            if (isPlaying) {
                music.pause();
                playBtn.innerHTML = '<i class="fas fa-play"></i>';
            } else {
                music.play().catch(e => console.log("Autoplay prevented: ", e));
                playBtn.innerHTML = '<i class="fas fa-pause"></i>';
            }
            isPlaying = !isPlaying;
        });
        
        // Volume control
        volumeSlider.addEventListener('input', () => {
            music.volume = volumeSlider.value / 100;
        });
        
        // Next button
        document.getElementById('next-btn').addEventListener('click', () => {
            // In a real implementation, this would switch to next track
            alert("Next track feature would be implemented here");
        });
        
        // Previous button
        document.getElementById('prev-btn').addEventListener('click', () => {
            // In a real implementation, this would switch to previous track
            alert("Previous track feature would be implemented here");
        });
        
        // Initialize the page
        function init() {
            updateTime();
            updateBattery();
            renderServices();
            
            // Set music volume to 50%
            music.volume = 0.5;
            
            // Update time every minute
            setInterval(updateTime, 60000);
            
            // Update battery every 30 seconds (simulation)
            setInterval(updateBattery, 30000);
            
            // Simulate adding a new service after 3 seconds (for demo)
            setTimeout(() => {
                addNewService(
                    "Social Media Growth", 
                    "fa-chart-line", 
                    "https://example.com/growth", 
                    "Boost your followers organically"
                );
            }, 3000);
        }
        
        // Start the application
        window.onload = init;
    </script>
</body>
</html>
