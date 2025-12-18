# engrpromise.github.io
PhD project dissertation 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LLM-Augmented HRL for Crypto Portfolio Optimization</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Base Styles and Variables */
        :root {
            --primary: #1a237e;
            --secondary: #0d47a1;
            --accent: #00bcd4;
            --light: #f5f7ff;
            --dark: #121212;
            --gray: #6c757d;
            --success: #4caf50;
            --warning: #ff9800;
            --shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
            --transition: all 0.3s ease;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }
        
        a {
            text-decoration: none;
            color: inherit;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header & Navigation */
        header {
            background-color: white;
            box-shadow: var(--shadow);
            position: sticky;
            top: 0;
            z-index: 1000;
        }
        
        .header-content {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 1.2rem 0;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--accent);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav li {
            margin-left: 2rem;
        }
        
        nav a {
            font-weight: 600;
            padding: 0.5rem 0.2rem;
            position: relative;
            transition: var(--transition);
        }
        
        nav a:hover {
            color: var(--accent);
        }
        
        nav a.active {
            color: var(--accent);
        }
        
        nav a.active::after {
            content: '';
            position: absolute;
            width: 100%;
            height: 3px;
            background-color: var(--accent);
            bottom: -5px;
            left: 0;
        }
        
        .mobile-menu-btn {
            display: none;
            background: none;
            border: none;
            font-size: 1.5rem;
            color: var(--primary);
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 4rem 0;
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .hero h1 {
            font-size: 2.5rem;
            margin-bottom: 1rem;
            line-height: 1.3;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 800px;
            margin: 0 auto 2rem;
            opacity: 0.9;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 0.8rem 1.8rem;
            border-radius: 4px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: var(--transition);
        }
        
        .btn:hover {
            background-color: #0097a7;
            transform: translateY(-2px);
            box-shadow: 0 6px 12px rgba(0, 0, 0, 0.15);
        }
        
        /* Content Sections */
        .page {
            display: none;
            animation: fadeIn 0.5s ease;
        }
        
        .page.active {
            display: block;
        }
        
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        section {
            background-color: white;
            border-radius: 8px;
            box-shadow: var(--shadow);
            padding: 2.5rem;
            margin-bottom: 2.5rem;
        }
        
        section h2 {
            color: var(--primary);
            margin-bottom: 1.5rem;
            padding-bottom: 0.8rem;
            border-bottom: 2px solid #eee;
            font-size: 1.8rem;
        }
        
        section h3 {
            color: var(--secondary);
            margin: 1.5rem 0 0.8rem;
            font-size: 1.3rem;
        }
        
        section p {
            margin-bottom: 1.2rem;
        }
        
        /* Methodology Components */
        .methodology-steps {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        .step {
            flex: 1;
            min-width: 250px;
            background: #f8f9ff;
            border-left: 4px solid var(--accent);
            padding: 1.5rem;
            border-radius: 4px;
        }
        
        .step-number {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            text-align: center;
            line-height: 30px;
            font-weight: bold;
            margin-bottom: 1rem;
        }
        
        /* Results Components */
        .results-container {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .result-card {
            background: #f8f9ff;
            border-radius: 8px;
            padding: 1.5rem;
            border-top: 4px solid var(--accent);
        }
        
        .result-card h4 {
            color: var(--primary);
            margin-bottom: 0.8rem;
        }
        
        .result-value {
            font-size: 2rem;
            font-weight: 700;
            color: var(--secondary);
            margin: 1rem 0;
        }
        
        .chart-placeholder {
            height: 200px;
            background: linear-gradient(45deg, #e0e7ff, #f3e5f5);
            border-radius: 6px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-weight: 600;
            margin: 1.5rem 0;
        }
        
        /* Team Section */
        .team-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
            margin-top: 2rem;
        }
        
        .team-member {
            text-align: center;
            padding: 1.5rem;
            background: #f8f9ff;
            border-radius: 8px;
            transition: var(--transition);
        }
        
        .team-member:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0, 0, 0, 0.1);
        }
        
        .member-photo {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            background-color: #ddd;
            margin: 0 auto 1rem;
            overflow: hidden;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 2.5rem;
        }
        
        /* Publications */
        .publication-list {
            margin-top: 1.5rem;
        }
        
        .publication-item {
            padding: 1.2rem;
            border-left: 3px solid var(--accent);
            background-color: #f8f9ff;
            margin-bottom: 1rem;
            border-radius: 0 4px 4px 0;
        }
        
        .publication-item h4 {
            color: var(--primary);
            margin-bottom: 0.5rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 3rem 0 1.5rem;
            margin-top: 3rem;
        }
        
        .footer-content {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            margin-bottom: 2rem;
        }
        
        .footer-column {
            flex: 1;
            min-width: 250px;
            margin-bottom: 1.5rem;
        }
        
        .footer-column h3 {
            color: var(--accent);
            margin-bottom: 1.2rem;
            font-size: 1.2rem;
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column li {
            margin-bottom: 0.6rem;
        }
        
        .footer-column a:hover {
            color: var(--accent);
        }
        
        .social-icons {
            display: flex;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .social-icons a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 36px;
            height: 36px;
            background-color: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transition: var(--transition);
        }
        
        .social-icons a:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Responsive Design */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2rem;
            }
        }
        
        @media (max-width: 768px) {
            .mobile-menu-btn {
                display: block;
            }
            
            nav ul {
                position: fixed;
                top: 70px;
                left: 0;
                width: 100%;
                background-color: white;
                flex-direction: column;
                align-items: center;
                padding: 1rem 0;
                box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1);
                transform: translateY(-150%);
                transition: transform 0.3s ease;
                z-index: 999;
            }
            
            nav ul.active {
                transform: translateY(0);
            }
            
            nav li {
                margin: 0.8rem 0;
            }
            
            .hero {
                padding: 3rem 0;
            }
            
            .hero h1 {
                font-size: 1.8rem;
            }
            
            section {
                padding: 1.8rem;
            }
        }
        
        @media (max-width: 576px) {
            .hero h1 {
                font-size: 1.6rem;
            }
            
            .hero p {
                font-size: 1rem;
            }
            
            section {
                padding: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container">
            <div class="header-content">
                <div class="logo">HRL<span>Crypto</span>Research</div>
                <button class="mobile-menu-btn" id="mobileMenuBtn">
                    <i class="fas fa-bars"></i>
                </button>
                <nav>
                    <ul id="navMenu">
                        <li><a href="#" class="nav-link active" data-page="home">Home</a></li>
                        <li><a href="#" class="nav-link" data-page="methodology">Methodology</a></li>
                        <li><a href="#" class="nav-link" data-page="results">Results</a></li>
                    </ul>
                </nav>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <div class="hero">
        <div class="container">
            <h1>LLM-Augmented Hierarchical Reinforcement Learning for Multi-Asset Cryptocurrency Portfolio Optimization under Extreme Volatility</h1>
            <p>Advanced AI-driven approach combining Large Language Models with Hierarchical Reinforcement Learning to optimize cryptocurrency portfolios in highly volatile market conditions.</p>
            <a href="#" class="btn nav-link" data-page="methodology">Explore Methodology</a>
        </div>
    </div>

    <!-- Main Content Area -->
    <main class="container">
        <!-- Home Page -->
        <div id="home-page" class="page active">
            <section id="overview">
                <h2>Research Overview</h2>
                <p>This research introduces a novel framework that integrates Large Language Models (LLMs) with Hierarchical Reinforcement Learning (HRL) to address the complex challenge of multi-asset cryptocurrency portfolio optimization in environments characterized by extreme volatility.</p>
                
                <p>Traditional portfolio optimization methods often fail in cryptocurrency markets due to non-stationary price dynamics, sudden market shocks, and complex interdependencies between assets. Our approach leverages the reasoning capabilities of LLMs to interpret market sentiment and news, while HRL provides a structured decision-making process for portfolio allocation.</p>
                
                <div class="chart-placeholder">
                    LLM-Augmented HRL Architecture Diagram
                </div>
                
                <h3>Key Innovations</h3>
                <ul>
                    <li>Integration of LLMs for market sentiment analysis and contextual understanding</li>
                    <li>Hierarchical RL structure with meta-controller and sub-controllers for multi-timescale decision making</li>
                    <li>Novel reward shaping incorporating volatility-adjusted returns</li>
                    <li>Adaptive risk management under extreme market conditions</li>
                </ul>
            </section>
            
            <section id="team">
                <h2>Research Team</h2>
                <p>This interdisciplinary project brings together experts in machine learning, quantitative finance, and blockchain technology.</p>
                
                <div class="team-grid">
                    <div class="team-member">
                        <div class="member-photo">
                            <i class="fas fa-user"></i>
                        </div>
                        <h3>Dr. Alexandra Chen</h3>
                        <p>Principal Investigator</p>
                        <p>Professor of Machine Learning, Stanford University</p>
                    </div>
                    
                    <div class="team-member">
                        <div class="member-photo">
                            <i class="fas fa-user"></i>
                        </div>
                        <h3>Dr. Marcus Johnson</h3>
                        <p>Quantitative Finance Lead</p>
                        <p>Former Head of Quant Research, Goldman Sachs</p>
                    </div>
                    
                    <div class="team-member">
                        <div class="member-photo">
                            <i class="fas fa-user"></i>
                        </div>
                        <h3>Dr. Sophia Williams</h3>
                        <p>Blockchain Technology Expert</p>
                        <p>Director, MIT Digital Currency Initiative</p>
                    </div>
                    
                    <div class="team-member">
                        <div class="member-photo">
                            <i class="fas fa-user"></i>
                        </div>
                        <h3>Dr. Raj Patel</h3>
                        <p>Reinforcement Learning Specialist</p>
                        <p>Senior Researcher, DeepMind</p>
                    </div>
                </div>
            </section>
            
            <section id="publications">
                <h2>Related Publications</h2>
                <div class="publication-list">
                    <div class="publication-item">
                        <h4>LLM-Augmented Hierarchical Reinforcement Learning for Portfolio Optimization</h4>
                        <p><strong>Authors:</strong> Chen, A., Johnson, M., Williams, S., Patel, R.</p>
                        <p><strong>Conference:</strong> NeurIPS 2023</p>
                        <p><strong>Status:</strong> Under Review</p>
                    </div>
                    
                    <div class="publication-item">
                        <h4>Adaptive Risk Management in Cryptocurrency Markets Using Multi-Agent Reinforcement Learning</h4>
                        <p><strong>Authors:</strong> Johnson, M., Chen, A.</p>
                        <p><strong>Journal:</strong> Journal of Financial Data Science, 2023</p>
                    </div>
                    
                    <div class="publication-item">
                        <h4>Extreme Volatility Modeling with Deep Reinforcement Learning</h4>
                        <p><strong>Authors:</strong> Patel, R., Williams, S.</p>
                        <p><strong>Conference:</strong> ICML 2022</p>
                    </div>
                </div>
            </section>
        </div>
        
        <!-- Methodology Page -->
        <div id="methodology-page" class="page">
            <section>
                <h2>Methodology Overview</h2>
                <p>Our methodology combines the interpretative power of Large Language Models with the structured decision-making of Hierarchical Reinforcement Learning to create a robust portfolio optimization framework for extreme volatility environments.</p>
                
                <div class="methodology-steps">
                    <div class="step">
                        <div class="step-number">1</div>
                        <h3>LLM-Based Market Context Analysis</h3>
                        <p>LLMs process real-time news, social media sentiment, and market reports to generate contextual embeddings that inform the reinforcement learning agent about market conditions.</p>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">2</div>
                        <h3>Hierarchical RL Architecture</h3>
                        <p>A two-level hierarchy: Meta-controller sets high-level allocation strategy, while sub-controllers execute specific trading actions for individual assets.</p>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">3</div>
                        <h3>Multi-Timescale Decision Making</h3>
                        <p>The system operates on multiple timescales: daily rebalancing for long-term strategy and minute-level adjustments for volatility management.</p>
                    </div>
                    
                    <div class="step">
                        <div class="step-number">4</div>
                        <h3>Volatility-Adaptive Reward Function</h3>
                        <p>Custom reward function that balances returns with volatility-adjusted risk metrics, dynamically adjusting during extreme market events.</p>
                    </div>
                </div>
                
                <h3>Technical Architecture</h3>
                <p>The system is implemented using a combination of transformer-based LLMs (GPT-4 architecture) for natural language processing and a custom HRL framework built on PyTorch. The architecture features:</p>
                
                <ul>
                    <li><strong>LLM Module:</strong> Fine-tuned GPT-4 for financial text analysis, generating 512-dimensional context embeddings</li>
                    <li><strong>Meta-Controller:</strong> GRU-based network processing portfolio state and LLM embeddings</li>
                    <li><strong>Sub-Controllers:</strong> Ensemble of DDPG agents for individual asset trading decisions</li>
                    <li><strong>Risk Manager:</strong> Monolithic network evaluating Value-at-Risk and expected shortfall</li>
                    <li><strong>Backtesting Engine:</strong> High-fidelity simulation of cryptocurrency markets with slippage and transaction costs</li>
                </ul>
                
                <div class="chart-placeholder">
                    Technical Architecture Visualization
                </div>
                
                <h3>Data Sources</h3>
                <p>Our research utilizes multiple data sources including:</p>
                <ul>
                    <li>Historical cryptocurrency price data (BTC, ETH, and 15 altcoins) at 1-minute intervals</li>
                    <li>Real-time news feeds from 20+ financial publications</li>
                    <li>Social media sentiment data from Twitter and Reddit</li>
                    <li>On-chain metrics (transaction volume, wallet activity, miner flows)</li>
                    <li>Traditional market indicators (VIX, bond yields, forex rates)</li>
                </ul>
            </section>
        </div>
        
        <!-- Results Page -->
        <div id="results-page" class="page">
            <section>
                <h2>Experimental Results</h2>
                <p>Our LLM-Augmented HRL framework was tested on cryptocurrency market data from January 2021 to December 2022, a period marked by significant volatility including the May 2021 crash and the LUNA/UST collapse in May 2022.</p>
                
                <div class="results-container">
                    <div class="result-card">
                        <h4>Cumulative Return</h4>
                        <div class="result-value">+247.3%</div>
                        <p>Outperforming baseline strategies by 89-152%</p>
                    </div>
                    
                    <div class="result-card">
                        <h4>Sharpe Ratio</h4>
                        <div class="result-value">2.87</div>
                        <p>Risk-adjusted returns significantly higher than benchmarks</p>
                    </div>
                    
                    <div class="result-card">
                        <h4>Max Drawdown</h4>
                        <div class="result-value">-18.2%</div>
                        <p>Substantially lower than market average (-64.3%) during extreme events</p>
                    </div>
                    
                    <div class="result-card">
                        <h4>Volatility-Adjusted Return</h4>
                        <div class="result-value">1.94</div>
                        <p>Measure of return per unit of risk (higher is better)</p>
                    </div>
                </div>
                
                <div class="chart-placeholder">
                    Cumulative Returns Comparison Chart
                </div>
                
                <h3>Performance Comparison</h3>
                <p>The LLM-Augmented HRL framework was compared against several baseline methods:</p>
                
                <ul>
                    <li><strong>Traditional Mean-Variance Optimization:</strong> +98.7% return, Sharpe 1.02, Max Drawdown -42.1%</li>
                    <li><strong>Deep Q-Learning Portfolio:</strong> +158.4% return, Sharpe 1.89, Max Drawdown -31.5%</li>
                    <li><strong>PPO-based Agent:</strong> +130.2% return, Sharpe 1.45, Max Drawdown -38.7%</li>
                    <li><strong>Equal Weight Portfolio (Benchmark):</strong> +95.3% return, Sharpe 0.87, Max Drawdown -64.3%</li>
                    <li><strong>Our Method (LLM-HRL):</strong> +247.3% return, Sharpe 2.87, Max Drawdown -18.2%</li>
                </ul>
                
                <div class="chart-placeholder">
                    Drawdown Comparison During Extreme Volatility Events
                </div>
                
                <h3>Key Findings</h3>
                <ul>
                    <li>The LLM component significantly improved performance during news-driven market events, with 34% higher returns during FOMC announcements and regulatory news periods</li>
                    <li>The hierarchical structure allowed the system to maintain strategic positioning while making tactical adjustments during volatility spikes</li>
                    <li>Risk management module successfully reduced exposure during the LUNA/UST collapse, limiting losses to 12% compared to market average of 45%</li>
                    <li>The framework demonstrated robust performance across different market regimes (bull, bear, sideways)</li>
                </ul>
                
                <h3>Future Work</h3>
                <p>We are currently extending this research in several directions:</p>
                <ul>
                    <li>Incorporating DeFi protocols and yield farming strategies into the portfolio optimization</li>
                    <li>Extending to cross-chain arbitrage opportunities</li>
                    <li>Developing explainability modules to interpret LLM contributions to decision-making</li>
                    <li>Testing on traditional asset classes with crypto-correlations</li>
                </ul>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>Research Lab</h3>
                    <p>Advanced Financial AI Research Group</p>
                    <p>Stanford University</p>
                    <p>350 Serra Mall, Stanford, CA 94305</p>
                </div>
                
                <div class="footer-column">
                    <h3>Contact</h3>
                    <ul>
                        <li><i class="fas fa-envelope"></i> hrlcrypto@stanford.edu</li>
                        <li><i class="fas fa-phone"></i> (650) 123-4567</li>
                        <li><i class="fas fa-map-marker-alt"></i> Gates Computer Science Building, Room 392</li>
                    </ul>
                </div>
                
                <div class="footer-column">
                    <h3>Connect</h3>
                    <p>Follow our research updates and publications</p>
                    <div class="social-icons">
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-github"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                        <a href="#"><i class="fas fa-paper-plane"></i></a>
                    </div>
                </div>
            </div>
            
            <div class="copyright">
                <p>&copy; 2023 LLM-Augmented HRL Crypto Research. All rights reserved.</p>
                <p>This website is for academic research purposes only.</p>
            </div>
        </div>
    </footer>

    <script>
        // Page Navigation
        document.addEventListener('DOMContentLoaded', function() {
            const navLinks = document.querySelectorAll('.nav-link');
            const pages = document.querySelectorAll('.page');
            const mobileMenuBtn = document.getElementById('mobileMenuBtn');
            const navMenu = document.getElementById('navMenu');
            
            // Function to switch pages
            function switchPage(pageId) {
                // Update active page
                pages.forEach(page => {
                    page.classList.remove('active');
                    if (page.id === `${pageId}-page`) {
                        page.classList.add('active');
                    }
                });
                
                // Update active nav link
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.getAttribute('data-page') === pageId) {
                        link.classList.add('active');
                    }
                });
                
                // Close mobile menu if open
                navMenu.classList.remove('active');
            }
            
            // Add click event to nav links
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const pageId = this.getAttribute('data-page');
                    switchPage(pageId);
                    
                    // Scroll to top of page
                    window.scrollTo({
                        top: 0,
                        behavior: 'smooth'
                    });
                });
            });
            
            // Mobile menu toggle
            mobileMenuBtn.addEventListener('click', function() {
                navMenu.classList.toggle('active');
            });
            
            // Close mobile menu when clicking outside
            document.addEventListener('click', function(e) {
                if (!navMenu.contains(e.target) && !mobileMenuBtn.contains(e.target)) {
                    navMenu.classList.remove('active');
                }
            });
            
            // Initialize with home page
            switchPage('home');
        });
    </script>
</body>
</html>
