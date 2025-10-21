<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SkillBuddy Nigeria 🤖 - AI-Powered Learning</title>
    <link rel="stylesheet" href="css/style.css">
</head>
<body>
    <div class="container">
        <!-- WELCOME SCREEN -->
        <div id="welcome-screen" class="screen active">
            <div class="header">
                <div class="ai-badge">🤖 AI Powered</div>
                <div class="logo">🎯</div>
                <div class="title">SkillBuddy Nigeria</div>
                <div class="subtitle">AI-Powered Skill Learning</div>
            </div>
            <div class="content">
                <div class="ai-feature-card">
                    <strong>🚀 AI Features Included:</strong>
                    <div class="feature-list">
                        • Personalized Learning Path<br>
                        • AI Tutor Chat Support<br>
                        • Adaptive Difficulty<br>
                        • Progress Analytics<br>
                        • Smart Recommendations
                    </div>
                </div>
                
                <button class="btn btn-primary" onclick="app.showScreen('signup-screen')">
                    Start AI-Powered Learning
                </button>
                
                <button class="btn btn-secondary" onclick="app.showScreen('login-screen')">
                    I Have an Account
                </button>
                
                <div class="footer-note">
                    🤖 AI Tutor • 📊 Smart Analytics • 🎯 Personalized
                </div>
            </div>
        </div>

        <!-- SIGNUP SCREEN -->
        <div id="signup-screen" class="screen">
            <div class="header">
                <div class="title">AI Learning Profile</div>
                <div class="subtitle">Tell us about your goals</div>
            </div>
            <div class="content">
                <input type="text" id="user-name" class="form-input" placeholder="Your Name" value="Test User">
                <input type="tel" id="user-phone" class="form-input" placeholder="Phone Number" value="09121468809">
                
                <div class="form-section">
                    <strong>Choose Your Skill:</strong>
                    <div class="skill-grid">
                        <div class="skill-btn" onclick="app.selectSkill('piano')">🎹 Piano</div>
                        <div class="skill-btn" onclick="app.selectSkill('design')">🎨 Design</div>
                        <div class="skill-btn" onclick="app.selectSkill('drums')">🥁 Drums</div>
                        <div class="skill-btn" onclick="app.selectSkill('violin')">🎻 Violin</div>
                        <div class="skill-btn" onclick="app.selectSkill('voice')">🎤 Voice Training</div>
                        <div class="skill-btn" onclick="app.selectSkill('karate')">🥋 Karate</div>
                    </div>
                </div>
                
                <div class="form-section">
                    <strong>Learning Goal:</strong>
                    <select id="learning-goal" class="form-select">
                        <option value="hobby">🎯 For Fun & Hobby</option>
                        <option value="career">💼 For Career Development</option>
                        <option value="performance">🎭 For Live Performance</option>
                        <option value="business">💼 For Business Use</option>
                    </select>
                </div>
                
                <div class="form-section">
                    <strong>Available Practice Time:</strong>
                    <select id="practice-time" class="form-select">
                        <option value="15">15 minutes daily</option>
                        <option value="30">30 minutes daily</option>
                        <option value="45">45 minutes daily</option>
                        <option value="60">1 hour daily</option>
                    </select>
                </div>
                
                <button class="btn btn-primary" onclick="app.createAILearningProfile()">
                    🤖 Create AI Learning Plan
                </button>
                
                <button class="btn btn-secondary" onclick="app.showScreen('welcome-screen')">
                    Back
                </button>
            </div>
        </div>

        <!-- DASHBOARD SCREEN -->
        <div id="dashboard-screen" class="screen">
            <div class="header">
                <div class="title" id="greeting">Hello, User!</div>
                <div class="subtitle" id="user-skill">AI Learning Active</div>
            </div>
            <div class="content">
                <!-- AI Recommendations -->
                <div class="ai-recommendation" id="ai-recommendation">
                    <strong>🤖 AI Suggestion:</strong>
                    <div id="recommendation-text">Based on your progress, I recommend focusing on chord transitions today.</div>
                </div>
                
                <!-- Adaptive Difficulty -->
                <div class="adaptive-difficulty">
                    <strong>🎯 Current Level: <span id="difficulty-level">Beginner</span></strong>
                    <div class="difficulty-subtext">
                        AI-adjusted based on your performance
                    </div>
                </div>
                
                <div class="lesson-card">
                    <strong>📚 AI-Personalized Lesson</strong>
                    <div id="lesson-title">Piano Basics - Hand Positioning</div>
                    <div class="lesson-meta">
                        ⏱️ <span id="lesson-duration">15 minutes</span> • 
                        🎯 <span id="lesson-focus">Fundamentals</span>
                    </div>
                    <button class="btn btn-primary" onclick="app.startAILesson()">
                        Start AI Lesson
                    </button>
                </div>
                
                <!-- Progress Analytics -->
                <div class="analytics-card">
                    <strong>📊 AI Progress Analytics</strong>
                    <div class="analytics-grid">
                        <div class="analytics-item">
                            <div class="analytics-value" id="completion-rate">85%</div>
                            <div class="analytics-label">Success Rate</div>
                        </div>
                        <div class="analytics-item">
                            <div class="analytics-value" id="improvement-score">+12%</div>
                            <div class="analytics-label">Weekly Improvement</div>
                        </div>
                        <div class="analytics-item">
                            <div class="analytics-value" id="consistency-score">94%</div>
                            <div class="analytics-label">Consistency</div>
                        </div>
                    </div>
                </div>
                
                <button class="btn btn-ai" onclick="app.showScreen('ai-tutor-screen')">
                    🧠 Talk to AI Tutor
                </button>

                <button class="btn btn-ai" onclick="app.showScreen('voice-training-screen')">
                    🎤 Start Voice Training
                </button>
                
                <button class="btn btn-secondary" onclick="app.showPayment()">
                    💳 Upgrade to Premium
                </button>
            </div>
        </div>

        <!-- AI TUTOR CHAT SCREEN -->
        <div id="ai-tutor-screen" class="screen">
            <div class="header">
                <div class="title">🧠 AI Tutor</div>
                <div class="subtitle">Ask me anything about your skill!</div>
            </div>
            <div class="content">
                <div class="ai-chat" id="chat-messages">
                    <div class="message ai-message">
                        Hello! I'm your AI tutor. I can help you with:
                        • Lesson explanations
                        • Practice techniques  
                        • Problem solving
                        • Progress advice
                        What would you like to know?
                    </div>
                </div>
                
                <div class="typing-indicator" id="typing-indicator">
                    AI Tutor is typing...
                </div>
                
                <div class="chat-input">
                    <input type="text" id="chat-input" placeholder="Ask your question..." onkeypress="app.handleChatInput(event)">
                    <button class="btn btn-primary" onclick="app.sendMessage()">Send</button>
                </div>
                
                <div class="quick-questions">
                    <strong>Quick Questions:</strong>
                    <div class="quick-buttons">
                        <button class="btn quick-btn" onclick="app.askQuickQuestion('How can I improve my rhythm?')">Improve rhythm</button>
                        <button class="btn quick-btn" onclick="app.askQuickQuestion('Explain this lesson again')">Explain lesson</button>
                        <button class="btn quick-btn" onclick="app.askQuickQuestion('Give me practice exercises')">Practice exercises</button>
                    </div>
                </div>
                
                <button class="btn btn-secondary" onclick="app.showScreen('dashboard-screen')">
                    ← Back to Dashboard
                </button>
            </div>
        </div>

        <!-- LESSON SCREEN -->
        <div id="lesson-screen" class="screen">
            <div class="header">
                <div class="title" id="lesson-screen-title">AI Lesson</div>
                <div class="subtitle">Personalized for you</div>
            </div>
            <div class="content">
                <div id="lesson-content">
                    <!-- AI-generated lesson content will go here -->
                </div>
                
                <button class="btn btn-primary" onclick="app.completeAILesson()">
                    ✅ Complete Lesson
                </button>
                
                <button class="btn btn-ai" onclick="app.showScreen('ai-tutor-screen')">
                    🧠 Ask AI Tutor
                </button>
                
                <button class="btn btn-secondary" onclick="app.showScreen('dashboard-screen')">
                    ← Back to Dashboard
                </button>
            </div>
        </div>

        <!-- VOICE TRAINING SCREEN -->
        <div id="voice-training-screen" class="screen">
            <div class="header">
                <div class="title">🎤 Voice Training</div>
                <div class="subtitle">AI-Powered Vocal Development</div>
            </div>
            <div class="content">
                <!-- Voice Level Selection -->
                <div class="level-selection">
                    <strong>Select Your Vocal Level:</strong>
                    <div class="level-grid">
                        <div class="level-btn" onclick="voiceTraining.selectLevel('beginner')">
                            🐣 Beginner
                            <div class="level-desc">Just starting out</div>
                        </div>
                        <div class="level-btn" onclick="voiceTraining.selectLevel('intermediate')">
                            🚀 Intermediate
                            <div class="level-desc">Some experience</div>
                        </div>
                        <div class="level-btn" onclick="voiceTraining.selectLevel('advanced')">
                            ⚡ Advanced
                            <div class="level-desc">Regular performer</div>
                        </div>
                        <div class="level-btn" onclick="voiceTraining.selectLevel('professional')">
                            🏆 Professional
                            <div class="level-desc">Stage experience</div>
                        </div>
                    </div>
                </div>

                <!-- Daily Voice Exercise -->
                <div class="voice-exercise-card" id="voice-exercise-card">
                    <div class="exercise-header">
                        <strong>📅 Today's Vocal Exercise</strong>
                        <div class="exercise-difficulty" id="exercise-difficulty">Beginner</div>
                    </div>
                    <div class="exercise-content">
                        <div id="current-exercise">Lip trills for 2 minutes</div>
                        <div class="exercise-timer">
                            <div class="timer-display" id="timer-display">02:00</div>
                            <button class="btn btn-primary" onclick="voiceTraining.startExercise()" id="start-exercise-btn">
                                Start Exercise
                            </button>
                            <button class="btn btn-secondary" onclick="voiceTraining.stopExercise()" id="stop-exercise-btn" style="display: none;">
                                Stop Exercise
                            </button>
                        </div>
                    </div>
                </div>

                <!-- Posture Guide -->
                <div class="posture-guide">
                    <strong>🧘 Proper Singing Posture</strong>
                    <div class="posture-steps">
                        <div class="posture-step">
                            <span class="step-number">1</span>
                            <span>Feet shoulder-width apart</span>
                        </div>
                        <div class="posture-step">
                            <span class="step-number">2</span>
                            <span>Knees slightly bent</span>
                        </div>
                        <div class="posture-step">
                            <span class="step-number">3</span>
                            <span>Spine straight, shoulders relaxed</span>
                        </div>
                        <div class="posture-step">
                            <span class="step-number">4</span>
                            <span>Chin parallel to floor</span>
                        </div>
                    </div>
                    <button class="btn btn-secondary" onclick="voiceTraining.showPostureDemo()">
                        🎬 View Posture Demo
                    </button>
                </div>

                <!-- Breathing Techniques -->
                <div class="breathing-techniques">
                    <strong>🌬️ Breathing Exercises</strong>
                    <div class="breathing-exercises">
                        <div class="breathing-exercise" onclick="voiceTraining.startBreathingExercise('diaphragmatic')">
                            <strong>Diaphragmatic Breathing</strong>
                            <div>4-7-8 technique for vocal support</div>
                        </div>
                        <div class="breathing-exercise" onclick="voiceTraining.startBreathingExercise('ribcage')">
                            <strong>Ribcage Expansion</strong>
                            <div>Expand ribs without shoulder movement</div>
                        </div>
                        <div class="breathing-exercise" onclick="voiceTraining.startBreathingExercise('panting')">
                            <strong>Panting Exercise</strong>
                            <div>Build diaphragm strength</div>
                        </div>
                    </div>
                </div>

                <!-- AI Voice Analysis -->
                <div class="voice-analysis">
                    <strong>🤖 AI Voice Analysis</strong>
                    <div class="analysis-results">
                        <div class="analysis-item">
                            <div class="analysis-label">Pitch Stability</div>
                            <div class="analysis-bar">
                                <div class="analysis-fill" id="pitch-stability" style="width: 75%"></div>
                            </div>
                            <div class="analysis-value" id="pitch-value">75%</div>
                        </div>
                        <div class="analysis-item">
                            <div class="analysis-label">Breath Control</div>
                            <div class="analysis-bar">
                                <div class="analysis-fill" id="breath-control" style="width: 60%"></div>
                            </div>
                            <div class="analysis-value" id="breath-value">60%</div>
                        </div>
                        <div class="analysis-item">
                            <div class="analysis-label">Tone Quality</div>
                            <div class="analysis-bar">
                                <div class="analysis-fill" id="tone-quality" style="width: 80%"></div>
                            </div>
                            <div class="analysis-value" id="tone-value">80%</div>
                        </div>
                    </div>
                    <button class="btn btn-ai" onclick="voiceTraining.startVoiceAnalysis()">
                        🎤 Start Voice Analysis
                    </button>
                </div>

                <!-- Progress Tracking -->
                <div class="voice-progress">
                    <strong>📈 Vocal Progress</strong>
                    <div class="progress-stats">
                        <div class="progress-stat">
                            <div class="stat-value" id="vocal-range">C3-G4</div>
                            <div class="stat-label">Vocal Range</div>
                        </div>
                        <div class="progress-stat">
                            <div class="stat-value" id="practice-streak">5</div>
                            <div class="stat-label">Day Streak</div>
                        </div>
                        <div class="progress-stat">
                            <div class="stat-value" id="endurance-score">7/10</div>
                            <div class="stat-label">Endurance</div>
                        </div>
                    </div>
                </div>

                <button class="btn btn-secondary" onclick="app.showScreen('dashboard-screen')">
                    ← Back to Dashboard
                </button>
            </div>
        </div>

        <!-- BREATHING EXERCISE SCREEN -->
        <div id="breathing-exercise-screen" class="screen">
            <div class="header">
                <div class="title" id="breathing-title">Breathing Exercise</div>
                <div class="subtitle">Follow the rhythm</div>
            </div>
            <div class="content">
                <div class="breathing-animation">
                    <div class="breathing-circle" id="breathing-circle">
                        <div class="breathing-text" id="breathing-text">Breathe In</div>
                    </div>
                </div>
                <div class="breathing-timer">
                    <div class="breathing-time" id="breathing-time">04s</div>
                    <div class="breathing-phase" id="breathing-phase">Inhale</div>
                </div>
                <div class="breathing-instructions">
                    <div id="breathing-instruction">Inhale deeply through your nose for 4 seconds</div>
                </div>
                <button class="btn btn-primary" onclick="voiceTraining.stopBreathingExercise()">
                    Complete Exercise
                </button>
            </div>
        </div>

        <!-- PAYMENT SCREEN -->
        <div id="payment-screen" class="screen">
            <div class="header">
                <div class="title">Upgrade to AI Premium</div>
                <div class="subtitle">Unlock Advanced AI Features</div>
            </div>
            <div class="content">
                <div class="ai-feature-card">
                    <strong>🚀 AI Premium Includes:</strong>
                    <div class="feature-list">
                        • Advanced Personalization<br>
                        • Voice-based AI Tutor<br>
                        • Real-time Feedback<br>
                        • Detailed Analytics<br>
                        • Priority Support
                    </div>
                </div>
                
                <div class="pricing-display">
                    <div class="price">₦500/week</div>
                    <div class="price-subtext">or ₦1,500/month</div>
                </div>
                
                <div class="payment-instructions">
                    <strong>Payment Instructions:</strong><br>
                    Send ₦500 to OPay: <strong>9121468809</strong><br>
                    Then WhatsApp screenshot to <strong>09121468809</strong>
                </div>
                
                <button class="btn btn-primary" onclick="app.simulatePayment()">
                    💳 Activate AI Premium
                </button>
                
                <button class="btn btn-secondary" onclick="app.showScreen('dashboard-screen')">
                    Maybe Later
                </button>
            </div>
        </div>
    </div>

    <script src="js/app.js"></script>
    <script src="js/voice-training.js"></script>
</body>
</html>
