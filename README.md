:root {
    --primary-orange: #FF6B35;
    --primary-blue: #2D5B8F;
    --primary-purple: #7E57C2;
    --accent-red: #E63946;
    --light-bg: #F8F9FA;
    --dark-text: #333333;
    --light-text: #FFFFFF;
    --shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    --border-radius: 12px;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

html, body {
    width: 100%;
    height: 100%;
    overflow-x: hidden;
}

body {
    background-color: var(--light-bg);
    color: var(--dark-text);
    line-height: 1.6;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
}

.container {
    width: 100%;
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* Header & Navigation */
header {
    background: linear-gradient(135deg, var(--primary-blue), var(--primary-purple));
    color: var(--light-text);
    padding: 15px 0;
    position: sticky;
    top: 0;
    z-index: 1000;
    box-shadow: var(--shadow);
    width: 100%;
}

.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo {
    display: flex;
    align-items: center;
    gap: 10px;
}

.logo-circle {
    width: 45px;
    height: 45px;
    background: linear-gradient(135deg, var(--primary-orange), var(--accent-red));
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: bold;
    font-size: 1.2rem;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.logo-text {
    font-size: 1.8rem;
    font-weight: 700;
    letter-spacing: 1px;
}

.logo-text span {
    color: var(--primary-orange);
}

.nav-links {
    display: flex;
    gap: 25px;
}

.nav-links a {
    color: var(--light-text);
    text-decoration: none;
    font-weight: 500;
    transition: color 0.3s;
    position: relative;
}

.nav-links a:hover {
    color: var(--primary-orange);
}

.nav-links a::after {
    content: '';
    position: absolute;
    width: 0;
    height: 2px;
    bottom: -5px;
    left: 0;
    background-color: var(--primary-orange);
    transition: width 0.3s;
}

.nav-links a:hover::after {
    width: 100%;
}

.auth-buttons {
    display: flex;
    gap: 15px;
}

.btn {
    padding: 8px 20px;
    border-radius: 30px;
    font-weight: 600;
    cursor: pointer;
    transition: all 0.3s ease;
    border: none;
}

.btn-outline {
    background: transparent;
    border: 2px solid var(--light-text);
    color: var(--light-text);
}

.btn-outline:hover {
    background: var(--light-text);
    color: var(--primary-blue);
}

.btn-primary {
    background: var(--primary-orange);
    color: var(--light-text);
}

.btn-primary:hover {
    background: #e05a2b;
    transform: translateY(-2px);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

/* Hero Section */
.hero {
    background: linear-gradient(rgba(45, 91, 143, 0.85), rgba(126, 87, 194, 0.85)), url('https://images.unsplash.com/photo-1534438327276-14e5300c3a48?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1470&q=80');
    background-size: cover;
    background-position: center;
    color: var(--light-text);
    padding: 100px 0;
    text-align: center;
    width: 100%;
}

.hero h1 {
    font-size: 3rem;
    margin-bottom: 20px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.hero p {
    font-size: 1.2rem;
    max-width: 700px;
    margin: 0 auto 30px;
}

.search-box {
    background: var(--light-text);
    border-radius: 50px;
    padding: 10px;
    max-width: 600px;
    margin: 0 auto;
    display: flex;
    box-shadow: var(--shadow);
}

.search-box input {
    flex: 1;
    border: none;
    padding: 15px 20px;
    border-radius: 50px;
    font-size: 1rem;
    outline: none;
}

.search-box button {
    background: var(--primary-orange);
    color: white;
    border: none;
    border-radius: 50px;
    padding: 15px 30px;
    cursor: pointer;
    font-weight: 600;
    transition: background 0.3s;
}

.search-box button:hover {
    background: #e05a2b;
}

/* Features Section */
.section {
    padding: 80px 0;
    width: 100%;
}

.section-title {
    text-align: center;
    margin-bottom: 50px;
}

.section-title h2 {
    font-size: 2.5rem;
    color: var(--primary-blue);
    margin-bottom: 15px;
}

.section-title p {
    max-width: 700px;
    margin: 0 auto;
    color: #666;
}

.features {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.feature-card {
    background: white;
    border-radius: var(--border-radius);
    padding: 30px;
    box-shadow: var(--shadow);
    transition: transform 0.3s;
    text-align: center;
}

.feature-card:hover {
    transform: translateY(-10px);
}

.feature-icon {
    width: 70px;
    height: 70px;
    background: var(--primary-purple);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    color: white;
    font-size: 1.8rem;
}

.feature-card h3 {
    margin-bottom: 15px;
    color: var(--primary-blue);
}

/* How It Works */
.how-it-works {
    background: linear-gradient(135deg, var(--primary-blue), var(--primary-purple));
    color: var(--light-text);
}

.how-it-works .section-title h2 {
    color: var(--light-text);
}

.steps {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 20px;
}

.step {
    flex: 1;
    min-width: 250px;
    text-align: center;
    padding: 30px 20px;
}

.step-number {
    width: 50px;
    height: 50px;
    background: var(--primary-orange);
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 20px;
    font-size: 1.5rem;
    font-weight: bold;
}

/* Testimonials */
.testimonials {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}

.testimonial-card {
    background: white;
    border-radius: var(--border-radius);
    padding: 30px;
    box-shadow: var(--shadow);
}

.testimonial-text {
    font-style: italic;
    margin-bottom: 20px;
}

.testimonial-author {
    display: flex;
    align-items: center;
    gap: 15px;
}

.author-avatar {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background: var(--primary-blue);
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: bold;
}

/* CTA Section */
.cta {
    background: linear-gradient(135deg, var(--primary-orange), #FF8E53);
    color: var(--light-text);
    text-align: center;
    padding: 80px 0;
    width: 100%;
}

.cta h2 {
    font-size: 2.5rem;
    margin-bottom: 20px;
}

.cta p {
    max-width: 700px;
    margin: 0 auto 30px;
    font-size: 1.2rem;
}

/* Footer */
footer {
    background: var(--primary-blue);
    color: var(--light-text);
    padding: 60px 0 30px;
    width: 100%;
    margin-top: auto;
}

.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
    margin-bottom: 40px;
}

.footer-column h3 {
    margin-bottom: 20px;
    font-size: 1.3rem;
}

.footer-column ul {
    list-style: none;
}

.footer-column ul li {
    margin-bottom: 10px;
}

.footer-column ul li a {
    color: #ddd;
    text-decoration: none;
    transition: color 0.3s;
}

.footer-column ul li a:hover {
    color: var(--primary-orange);
}

.social-links {
    display: flex;
    gap: 15px;
    margin-top: 20px;
}

.social-links a {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    background: rgba(255, 255, 255, 0.1);
    display: flex;
    align-items: center;
    justify-content: center;
    color: white;
    text-decoration: none;
    transition: background 0.3s;
}

.social-links a:hover {
    background: var(--primary-orange);
}

.footer-bottom {
    text-align: center;
    padding-top: 30px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
}

/* Modal Styles */
.modal {
    display: none;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 1001;
    align-items: center;
    justify-content: center;
}

.modal-content {
    background-color: white;
    border-radius: var(--border-radius);
    width: 90%;
    max-width: 450px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
    overflow: hidden;
    animation: modalFadeIn 0.3s;
}

@keyframes modalFadeIn {
    from { opacity: 0; transform: translateY(-50px); }
    to { opacity: 1; transform: translateY(0); }
}

.modal-header {
    background: linear-gradient(135deg, var(--primary-blue), var(--primary-purple));
    color: white;
    padding: 20px;
    text-align: center;
    position: relative;
}

.modal-header h2 {
    margin: 0;
}

.close-modal {
    position: absolute;
    top: 15px;
    right: 15px;
    font-size: 1.5rem;
    cursor: pointer;
    color: white;
}

.modal-body {
    padding: 30px;
}

.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;
    margin-bottom: 8px;
    font-weight: 500;
}

.form-group input {
    width: 100%;
    padding: 12px 15px;
    border: 1px solid #ddd;
    border-radius: 8px;
    font-size: 1rem;
    transition: border-color 0.3s;
}

.form-group input:focus {
    border-color: var(--primary-blue);
    outline: none;
    box-shadow: 0 0 0 2px rgba(45, 91, 143, 0.2);
}

.form-options {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 20px;
}

.remember-me {
    display: flex;
    align-items: center;
    gap: 8px;
}

.forgot-password {
    color: var(--primary-blue);
    text-decoration: none;
    font-size: 0.9rem;
}

.forgot-password:hover {
    text-decoration: underline;
}

.modal-footer {
    text-align: center;
    padding-top: 20px;
    border-top: 1px solid #eee;
}

.modal-footer p {
    margin: 0;
    color: #666;
}

.modal-footer a {
    color: var(--primary-blue);
    text-decoration: none;
    font-weight: 500;
}

.modal-footer a:hover {
    text-decoration: underline;
}

/* Responsive */
@media (max-width: 768px) {
    .navbar {
        flex-direction: column;
        gap: 15px;
    }
    
    .nav-links {
        gap: 15px;
    }
    
    .hero h1 {
        font-size: 2.2rem;
    }
    
    .section {
        padding: 60px 0;
    }
    
    .section-title h2 {
        font-size: 2rem;
    }
    
    .steps {
        flex-direction: column;
    }
    
    .step {
        min-width: 100%;
    }
}
