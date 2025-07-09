# Saveetha_Admission_clone
## Date: 09-07-2025

## Objective:
To design a landing page clone of Saveetha Engineering College’s Admission Enquiry form using HTML and CSS. This activity reinforces skills in layout design, form creation, user input handling, responsive structure, and visual styling based on a real-world example.

## Tasks:
#### 1. Analyze the Landing Page Layout:
Observe the split-screen layout with a promotional section on the left and a form on the right.

Note the use of background images, text styling, and branding elements.

#### 2. Create the HTML Structure:
Use semantic tags like ```<section>, <header>, <form>, and <footer>``` to organize content.

Structure the form with input fields such as name, email, phone, password, city, state, course, specialization, captcha, and checkbox.

#### 3. Add Form Functionality:
Include appropriate input types (text, email, tel, password, select, etc.) with placeholders and labels.

Use the <button> element for the "APPLY NOW" action.

#### 4. Apply CSS Styling:
Implement a split layout using flexbox or grid.

Style the form elements with padding, shadows, background colors, and rounded borders.

Include hover effects and button transitions to match the original look.

#### 5. Incorporate Images and Branding:
Add the institution logo and use matching fonts and colors.

Place a background image or blurred overlay behind the form content if needed.

#### 6. Ensure Responsiveness:
Make sure the page adapts to different screen sizes using media queries.

Maintain readability and layout integrity on both desktop and mobile.

## HTML Code:

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Saveetha Engineering College</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="logo-section">
            <img src="logo.png" alt="Saveetha Logo" class="logo-img">
        </div>
        
        <div class="main-content">
            <h1 class="industry-heading">INDUSTRY 5.0</h1>
            <h2 class="curriculum-heading">Ready Curriculum Imparting</h2>
            <h2 class="skills-heading">21st Century Skills</h2>
            
            <button class="apply-btn">Apply Now</button>
        </div>
        
        <div class="sister-image">
            <img src="sister.png" alt="Student" class="student-img">
        </div>
        
        <div class="form-container">
            <h2>Admissions Open 2025</h2>
            
            <form class="admission-form">
                <input type="text" placeholder="Enter Name *" required>
                <input type="email" placeholder="Enter Email Address *" required>
                
                <div class="mobile-container">
                    <select name="country_code" class="country-code" required>
                        <option value="+91">+91 (India)</option>
                        <option value="+1">+1 (USA)</option>
                        <option value="+44">+44 (UK)</option>
                        <option value="+61">+61 (Australia)</option>
                        <option value="+971">+971 (UAE)</option>
                    </select>
                    <input type="tel" name="mobile" placeholder="Enter Mobile Number *" required>
                </div>
                
                <input type="password" placeholder="Any Password of Your Choice *" required>
                
                <div class="form-row">
                    <select name="state" required>
                        <option value="">State *</option>
                        <option value="Tamil Nadu">Tamil Nadu</option>
                        <option value="Karnataka">Karnataka</option>
                        <option value="Kerala">Kerala</option>
                        <option value="Andhra Pradesh">Andhra Pradesh</option>
                        <option value="Telangana">Telangana</option>
                    </select>
                    
                    <select name="city" required>
                        <option value="">City *</option>
                        <option value="Chennai">Chennai</option>
                        <option value="Bangalore">Bangalore</option>
                        <option value="Hyderabad">Hyderabad</option>
                        <option value="Coimbatore">Coimbatore</option>
                    </select>
                </div>
                
                <div class="form-row">
                    <select name="course" required>
                        <option value="">Course *</option>
                        <option value="B.Tech or B.E">B.Tech or B.E</option>
                        <option value="Lateral Entry">Lateral Entry</option>
                        <option value="M.E">M.E</option>
                        <option value="MBA">MBA</option>
                    </select>
                    
                    <select name="specialization" required>
                        <option value="">Specialization *</option>
                        <option value="Computer Science">Computer Science</option>
                        <option value="Information Technology">Information Technology</option>
                        <option value="Mechanical">Mechanical</option>
                        <option value="ECE">ECE</option>
                    </select>
                </div>
                
                <div class="captcha-container">
                    <div class="captcha-display">
                        <span id="captchaText">pQrs2P</span>
                        <button type="button" id="refreshCaptcha">Refresh</button>
                    </div>
                    <input type="text" id="captchaInput" placeholder="Enter Captcha" required>
                </div>
                <div class="checkbox-container">
                    <input type="checkbox" id="consent" required>
                    <label for="consent">I authorise Saveetha Engineering College & its representatives to contact me with updates and notifications via Email/SMS/WhatsApp/Call. This will override DND/NDNC *</label>
                </div>
                
                <button type="submit">APPLY NOW</button>
                
                <div class="form-footer">
                    <p><a href="#" class="footer-link">Already have an Account? Login</a></p>
                    <p><a href="#" class="footer-link">Resend Verification Email</a></p>
                </div>
            </form>
        </div>
    </div>
</body>
</html>
```
## CSS Code:

```
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    height: 100vh;
    overflow: visible;
    position: relative;
}

.container {
    position: relative;
    height: 100vh;
    background: rgba(0, 0, 0, 0.5); 
    overflow:visible
}

.logo-section {
    position: absolute;
    top: 10px; 
    left: 60px;
    z-index: 2;
}

.logo-img {
    width: 500px; 
    height: 280px;
    object-fit: contain;
}

.main-content {
    position: absolute;
    top: 300px; 
    left: 80px;
    color: white;
    text-align: left;
    z-index: 2;
}

.industry-heading {
    font-size: 3.0rem; 
    font-weight: 900;
    color: #FFD700;
    margin-bottom: 15px;
    text-shadow: 3px 3px 6px rgba(0,0,0,0.7);
    letter-spacing: 3px;
}

.curriculum-heading, .skills-heading {
    font-size: 1.5rem; 
    font-weight: 600;
    margin-bottom: 8px;
    text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
    line-height: 1.2;
}

.apply-btn {
    background: #FFD700;
    color: #333;
    border: none;
    padding: 18px 40px;
    font-size: 1.2rem;
    font-weight: bold;
    cursor: pointer;
    margin-top: 30px;
    box-shadow: 0 6px 20px rgba(255, 215, 0, 0.4);
    transition: all 0.3s ease;
    border-radius: 5px;
}

.apply-btn:hover {
    transform: translateY(-3px);
    box-shadow: 0 8px 25px rgba(255, 215, 0, 0.6);
}

.form-container {
    position: absolute;
    top: 15px;
    right: 50px;
    width: 330px;
    background: rgba(0, 0, 0, 0.6);
    padding: 18px;
    border-radius: 12px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
    backdrop-filter: blur(15px);
    border: 1px solid rgba(255, 255, 255, 0.2);
    z-index: 2;
}

.form-container h2 {
    color: white; 
    margin-bottom: 18px;
    text-align: center;
    font-size: 1.4rem;
}

.admission-form {
    display: flex;
    flex-direction: column;
    gap: 10px; 
}

.admission-form input,
.admission-form select {
    padding: 8px; 
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 12px; 
    outline: none;
    background: rgba(255, 255, 255, 0.95);
    color: #333;
    transition: all 0.3s ease;
}

.admission-form input:focus,
.admission-form select:focus {
    border-color: #667eea;
    background: rgba(255, 255, 255, 1);
}

.form-row {
    display: flex;
    gap: 8px; 
}

.mobile-container {
    display: flex;
    gap: 8px; 
}

.country-code {
    width: 80px; 
    padding: 8px 4px;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 11px;
    outline: none;
    background: rgba(255, 255, 255, 0.95);
    color: #333;
    transition: all 0.3s ease;
}

.country-code:focus {
    border-color: #667eea;
    background: rgba(255, 255, 255, 1);
}

.mobile-container input[type="tel"] {
    flex: 1;
    padding: 8px;
    border: 2px solid #ddd;
    border-radius: 5px;
    font-size: 12px;
    outline: none;
    background: rgba(255, 255, 255, 0.95);
    color: #333;
    transition: all 0.3s ease;
}

.mobile-container input[type="tel"]:focus {
    border-color: #667eea;
    background: rgba(255, 255, 255, 1);
}

.admission-form button {
    background: #FFD700;
    color: #333;
    padding: 10px; 
    border: none;
    border-radius: 5px;
    font-size: 13px;
    font-weight: bold;
    cursor: pointer;
    transition: all 0.3s ease;
    box-shadow: 0 4px 15px rgba(255, 215, 0, 0.3);
}

.admission-form button:hover {
    transform: translateY(-2px);
    box-shadow: 0 6px 20px rgba(255, 215, 0, 0.5);
}

.captcha-container {
    display: flex;
    flex-direction: column;
    gap: 5px;
}

.captcha-display {
    display: flex;
    align-items: center;
    gap: 6px;
    padding: 5px;
    background: rgba(255, 255, 255, 0.95);
    border: 1px solid #ddd;
    border-radius: 4px;
}

#captchaText {
    font-weight: bold;
    color: #333;
    font-size: 13px;
    letter-spacing: 1px;
}

#refreshCaptcha {
    background-color: #667eea;
    color: white;
    border: none;
    padding: 3px 6px;
    border-radius: 3px;
    cursor: pointer;
    font-size: 9px;
}

.checkbox-container {
    display: flex;
    align-items: flex-start;
    gap: 5px;
}

.checkbox-container input[type="checkbox"] {
    margin-top: 2px;
    width: 13px;
    height: 13px;
}

.checkbox-container label {
    font-size: 10px;
    color: white; 
    line-height: 1.2;
    cursor: pointer;
}

.form-footer {
    text-align: center;
    margin-top: 10px;
}

.form-footer p {
    margin: 3px 0;
    font-size: 10px;
}

.footer-link {
    color: #FFD700;
    text-decoration: none;
}

.footer-link:hover {
    text-decoration: underline;
}

.sister-image {
    position: absolute;
    left: 40%;
    bottom: 0;
    width: 500px;
    z-index: -0.1;
}

.student-img {
    width: 500px; 
    height: auto; 
    object-fit: contain;
}

@media (max-width: 768px) {
    .logo-section {
        top: 10px;
        left: 30px;
    }
    
    .logo-img {
        width: 300px;
        height: 180px;
    }
    
    .main-content {
        top: 200px;
        left: 30px;
    }
    
    .industry-heading {
        font-size: 2.5rem;
    }
    
    .curriculum-heading, .skills-heading {
        font-size: 1.3rem;
    }
    
    .sister-image {
        right: 35%;
        z-index: 3;
    }
    
    .student-img {
        width: 250px;
        height: 400px;
    }
    
    .form-container {
        top: 30px; 
        right: 15px;
        width: 280px;
    }
    
    .mobile-container {
        flex-direction: column;
        gap: 6px;
    }
    
    .country-code {
        width: 100%;
    }
}
```

## Output:

![image](https://github.com/user-attachments/assets/1cbb19e3-7980-4218-90ce-a97bd1d66c17)


## Result:
A landing page clone of Saveetha Engineering College’s Admission Enquiry form using HTML and CSS is designed successfully.
