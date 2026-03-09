/* Custom Font */
@font-face {
    font-family: 'Lucy Said Ok';
    src: url('LucySaidOkPersonalUse.ttf') format('truetype'); 
}

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
    font-family: 'Lucy Said Ok', cursive, sans-serif;
    background-color: #fff0f3; 
    color: #333;
    overflow-x: hidden;
}

/* Lovely Color Headings */
h1, h2, h3 {
    color: #ff3366; 
    font-size: 3.5rem;
    margin-bottom: 20px;
    text-shadow: 2px 2px 5px rgba(255, 51, 102, 0.2);
    font-weight: normal; 
    text-align: center;
}

/* Background Animation */
.floating-bg {
    position: fixed; top: 0; left: 0; width: 100vw; height: 100vh;
    z-index: -1; pointer-events: none; overflow: hidden;
}
.emoji {
    position: absolute; font-size: 2rem; opacity: 0.3;
    animation: floatUp 10s linear infinite;
}
.emoji:nth-child(1) { left: 10%; animation-duration: 8s; }
.emoji:nth-child(2) { left: 30%; animation-duration: 12s; animation-delay: 2s; }
.emoji:nth-child(3) { left: 50%; animation-duration: 9s; animation-delay: 1s; }
.emoji:nth-child(4) { left: 70%; animation-duration: 11s; animation-delay: 4s; }
.emoji:nth-child(5) { left: 85%; animation-duration: 10s; }
.emoji:nth-child(6) { left: 20%; animation-duration: 13s; animation-delay: 3s; }

@keyframes floatUp {
    0% { transform: translateY(100vh) rotate(0deg); }
    100% { transform: translateY(-10vh) rotate(360deg); }
}

/* Slide Layout */
.slide {
    display: none; 
    min-height: 100vh; 
    width: 100vw;
    flex-direction: column;
    justify-content: space-between; 
    align-items: center;
    padding: 40px 20px 20px 20px;
    animation: fadeIn 0.8s ease-in-out;
}
.slide.active { display: flex; }

@keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
}

.content {
    flex-grow: 1; display: flex; flex-direction: column;
    justify-content: center; align-items: center;
    max-width: 900px; width: 100%;
}

/* Specific Slide Styles */
.hero-gif { max-width: 350px; border-radius: 15px; margin-bottom: 30px; }
.sweetie-text { font-size: 3rem; color: #ff3366; text-align: center;}
.body-text { font-size: 2.2rem; color: #444; line-height: 1.5; text-align: center; margin-bottom: 20px;}

.left-align-content { align-items: flex-start; text-align: left; }
.left-align-content .small-heading { font-size: 2.8rem; text-align: left; margin-bottom: 20px; }
.left-align-content .body-text { text-align: left; }

/* Timeline */
.timeline { border-left: 3px solid #ff3366; padding: 10px 0; margin: 20px auto; max-width: 700px;}
.timeline-item { position: relative; padding-left: 30px; margin-bottom: 25px; text-align: left; }
.timeline-item::before { content: "♥"; position: absolute; left: -12px; top: 0; color: #ff3366; font-size: 1.5rem; background: #fff0f3; }
.date { display: block; color: #ff3366; font-size: 1.6rem; margin-bottom: 5px; }
.timeline-item p { font-size: 1.6rem; color: #555; }
.journey-continues { font-size: 2.8rem; margin-top: 30px; text-align: center;}

/* Slide 4: Password Lock */
.pink-bg { background-color: #ffb3c6; }
.lock-text { font-size: 2.5rem; color: #fff; margin-bottom: 20px; text-align: center;}
.password-box { padding: 15px; font-size: 1.5rem; border-radius: 10px; border: none; text-align: center; font-family: 'Lucy Said Ok'; margin-bottom: 20px;}
.unlock-btn { background-color: white; color: #ff3366; }

/* Slide 4: Unlocked Collage */
.collage-container { position: relative; width: 100%; height: 60vh; display: flex; justify-content: center; align-items: center; }
.center-white-box { background: white; padding: 30px; border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.2); z-index: 100; text-align: center; }
.center-white-box h3 { margin: 0; font-size: 3rem; }

.scatter { position: absolute; width: 120px; height: 120px; object-fit: cover; border: 5px solid white; box-shadow: 0 5px 15px rgba(0,0,0,0.2); border-radius: 10px; z-index: 1;}
.pic1 { top: 5%; left: 5%; transform: rotate(-15deg); }
.pic2 { top: 10%; right: 10%; transform: rotate(10deg); }
.pic3 { bottom: 10%; left: 10%; transform: rotate(-5deg); }
.pic4 { bottom: 5%; right: 5%; transform: rotate(20deg); }
.pic5 { top: 40%; left: 0%; transform: rotate(-25deg); }
.pic6 { top: 30%; right: 0%; transform: rotate(15deg); }
.pic7 { top: -5%; left: 40%; transform: rotate(5deg); }
.pic8 { bottom: -10%; left: 45%; transform: rotate(-10deg); }
.pic9 { top: 20%; left: 20%; transform: rotate(12deg); }
.pic10 { top: 25%; right: 25%; transform: rotate(-8deg); }
.pic11 { bottom: 20%; left: 25%; transform: rotate(18deg); }
.pic12 { bottom: 25%; right: 25%; transform: rotate(-12deg); }

/* Navigation Buttons */
.nav-buttons { width: 100%; display: flex; justify-content: center; gap: 20px; padding-bottom: 30px; margin-top: 20px;}
.btn {
    font-family: 'Lucy Said Ok', cursive, sans-serif; padding: 12px 30px;
    background-color: #ff3366; color: white; border: none; border-radius: 30px;
    font-size: 1.8rem; cursor: pointer; transition: 0.3s; box-shadow: 0 4px 10px rgba(255, 51, 102, 0.3);
}
.btn:hover { background-color: #ff1a53; transform: scale(1.05); }
