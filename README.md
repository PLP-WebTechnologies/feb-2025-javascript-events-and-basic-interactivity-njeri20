# 🎯 JavaScript Event Handling & Interactive Elements Assignment

Welcome to the **ultimate JavaScript playground**! 🎉 This assignment is where we turn boring web pages into dynamic, responsive, *alive* experiences. Get ready to master **event handling**, build **interactive components**, and validate forms like a pro! 💪

## 📁 Assignment Structure

```
📂 js-event-assignment/
├── index.html         # Your playground – where it all comes together
├── style.css          # Keep it cute (optional but encouraged)
└── script.js          # The JavaScript wizardry happens here
```

---

## 🧪 What to Build

Here’s what your interactive bundle of joy should include:

### 1. Event Handling 🎈  
- Button click ✅  
- Hover effects ✅  
- Keypress detection ✅  
- Bonus: A secret action for a *double-click* or *long press* 🤫

### 2. Interactive Elements 🎮  
- A button that changes text or color  
- An image gallery or slideshow  
- Tabs or accordion-style content  
- Bonus: Add some animation using JS or CSS ✨

### 3. Form Validation 📋✅  
- Required field checks  
- Email format validation  
- Password rules (e.g., min 8 characters)  
- Bonus: Real-time feedback while typing

---

## 🧙‍♂️ Pro Tips

- Keep your code clean and commented – your future self will thank you!
- Think about **user experience** – what makes your site more *fun* to use?
- Don’t be afraid to **Google and experiment** – that’s how real developers roll!

---

## 🎉 Now Go Make It Fun!

Remember – this isn't just code. It's your **first step toward creating magical user experiences**. So play around, break stuff (then fix it), and most of all, have FUN! 😄

Happy Coding! 💻✨  



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Event Handling & Interaction</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header>
        <h1>Interactive Web Page</h1>
    </header>

    <main>
        <section id="event-handling-section">
            <h2>1. Event Handling Demos</h2>
            <div class="event-demos">
                <button id="click-me-btn">Click Me!</button>
                <p id="click-output">Button not clicked yet.</p>

                <div id="hover-area">Hover Over Me</div>

                <label for="keypress-input">Press a key here:</label>
                <input type="text" id="keypress-input" placeholder="Type something...">
                <p id="keypress-output">Last key pressed: None</p>

                <button id="double-click-btn">Double Click Me!</button>
                <p id="double-click-output">Double-click button not double-clicked yet.</p>
            </div>
        </section>

        <hr> <section id="interactive-elements-section">
            <h2>2. Interactive Elements</h2>

            <div class="interactive-item">
                <h3>Changing Button</h3>
                <button id="toggle-button">Toggle State (Off)</button>
            </div>

            <div class="interactive-item">
                <h3>Simple Image Slideshow</h3>
                <div id="slideshow-container">
                    <img id="slideshow-img" src="https://via.placeholder.com/600x300/FF5733/FFFFFF?text=Image+1" alt="Slideshow Image">
                    <div class="slideshow-controls">
                        <button id="prev-slide-btn">Previous</button>
                        <button id="next-slide-btn">Next</button>
                    </div>
                    <p class="slideshow-status"></p>
                </div>
            </div>

            <div class="interactive-item">
                 <h3>Basic Tabs</h3>
                 <div class="tabs-container">
                     <div class="tabs-buttons">
                         <button class="tab-button active" data-tab="tab1">Tab 1</button>
                         <button class="tab-button" data-tab="tab2">Tab 2</button>
                         <button class="tab-button" data-tab="tab3">Tab 3</button>
                     </div>
                     <div class="tabs-content">
                         <div id="tab1" class="tab-pane active">
                             <h4>Content for Tab 1</h4>
                             <p>This is the content area for the first tab. Click on the other tabs to see their content.</p>
                         </div>
                         <div id="tab2" class="tab-pane">
                            <h4>Content for Tab 2</h4>
                            <p>This is the content for the second tab. Different content appears based on which tab is active.</p>
                         </div>
                         <div id="tab3" class="tab-pane">
                             <h4>Content for Tab 3</h4>
                             <p>And here is the content for the third tab. This demonstrates switching content sections.</p>
                         </div>
                     </div>
                 </div>
            </div>

        </section>

        <hr> <section id="form-validation-section">
            <h2>3. Form Validation</h2>
            <form id="registration-form" novalidate>
                <div class="form-group">
                    <label for="username">Username:</label>
                    <input type="text" id="username" name="username" required>
                    <span class="error-message"></span>
                </div>

                <div class="form-group">
                    <label for="email">Email:</label>
                    <input type="email" id="email" name="email" required>
                     <span class="error-message"></span>
                </div>

                <div class="form-group">
                    <label for="password">Password:</label>
                    <input type="password" id="password" name="password" required minlength="8">
                    <span class="error-message"></span>
                </div>

                <button type="submit">Register</button>
                 <p id="form-status"></p>
            </form>
        </section>
    </main>

    <footer>
        <p>&copy; 2023 JS Assignment Example</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>



/* Basic Styling and Layout */
body {
    font-family: sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 20px;
    background-color: #f8f8f8;
    color: #333;
}

main {
    max-width: 900px;
    margin: 20px auto;
    background-color: #fff;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

section {
    margin-bottom: 30px;
    padding: 15px;
    border: 1px solid #eee;
    border-radius: 5px;
}

h1, h2, h3 {
    color: #555;
    margin-bottom: 15px;
}

hr {
    margin: 30px 0;
    border: none;
    border-top: 1px solid #ddd;
}

button {
    padding: 10px 15px;
    margin-right: 10px;
    cursor: pointer;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: white;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #0056b3;
}

/* Event Handling Demos Specific Styles */
#hover-area {
    width: 150px;
    height: 50px;
    line-height: 50px; /* Vertically center text */
    text-align: center;
    border: 1px solid #007bff;
    margin-top: 15px;
    background-color: #e9f5ff;
    transition: background-color 0.3s ease;
}

#hover-area.hovered {
    background-color: yellow;
    border-color: orange;
}

#keypress-input {
    padding: 8px;
    margin-left: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

/* Interactive Elements Specific Styles */
.interactive-item {
    margin-bottom: 20px;
    padding: 15px;
    border: 1px dashed #ccc;
    border-radius: 5px;
}

/* Changing Button Style */
#toggle-button.on {
    background-color: green;
}
#toggle-button.off {
     background-color: red;
}


/* Slideshow Styles */
#slideshow-container {
    text-align: center;
    margin-top: 15px;
    border: 1px solid #ddd;
    padding: 10px;
    background-color: #f9f9f9;
    border-radius: 5px;
}

#slideshow-img {
    max-width: 100%;
    height: auto;
    display: block; /* Remove extra space below image */
    margin: 0 auto 15px auto; /* Center image and add space below */
    border-radius: 4px;
     /* Optional: Add a subtle animation for image transition */
    /* transition: opacity 0.5s ease-in-out; */
}

.slideshow-controls button {
    margin-top: 5px;
}

.slideshow-status {
    margin-top: 10px;
    font-size: 0.9em;
    color: #666;
}


/* Tabs Styles */
.tabs-container {
    margin-top: 15px;
}

.tabs-buttons {
    border-bottom: 1px solid #ddd;
    margin-bottom: 15px;
}

.tab-button {
    background-color: #f0f0f0;
    border: 1px solid #ddd;
    border-bottom: none;
    margin-bottom: -1px; /* Overlap border */
    padding: 10px 20px;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
}

.tab-button.active {
    background-color: #fff;
    border-color: #ddd;
    font-weight: bold;
    /* Bonus: Simple animation */
    animation: tab-fade-in 0.3s ease-in-out;
}

@keyframes tab-fade-in {
    from { opacity: 0.7; }
    to { opacity: 1; }
}


.tabs-content .tab-pane {
    display: none; /* Hide all tab content by default */
    padding: 15px;
    border: 1px solid #ddd;
    border-top: none;
    border-radius: 0 0 5px 5px;
    background-color: #fff;
}

.tabs-content .tab-pane.active {
    display: block; /* Show active tab content */
}

/* Form Validation Styles */
.form-group {
    margin-bottom: 15px;
}

.form-group label {
    display: block; /* Label on its own line */
    margin-bottom: 5px;
    font-weight: bold;
}

.form-group input[type="text"],
.form-group input[type="email"],
.form-group input[type="password"] {
    width: calc(100% - 22px); /* Adjust for padding and border */
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    font-size: 1em;
     transition: border-color 0.3s ease; /* Bonus: Animation for border change */
}

/* Validation Feedback Styles */
.form-group input:focus {
     outline: none;
     border-color: #007bff; /* Highlight on focus */
}

.form-group input.invalid {
    border-color: red;
}

.form-group input.valid {
    border-color: green;
}

.form-group .error-message {
    display: block; /* Show error message on a new line */
    color: red;
    font-size: 0.85em;
    margin-top: 5px;
    min-height: 1em; /* Reserve space to prevent layout shifts */
}

#form-status {
    margin-top: 15px;
    font-weight: bold;
    color: green;
}

#form-status.error {
    color: red;
}


// Wait for the DOM to be fully loaded before running the script
document.addEventListener('DOMContentLoaded', function() {

    // ======================================================
    // 1. Event Handling
    // ======================================================

    // Button Click
    const clickMeBtn = document.getElementById('click-me-btn');
    const clickOutput = document.getElementById('click-output');

    clickMeBtn.addEventListener('click', function() {
        clickOutput.textContent = 'Button was clicked!';
        console.log('Click button clicked!');
    });

    // Hover Effects (using mouseenter and mouseleave)
    const hoverArea = document.getElementById('hover-area');

    hoverArea.addEventListener('mouseenter', function() {
        hoverArea.textContent = 'You are hovering!';
        hoverArea.classList.add('hovered'); // Add class for styling
    });

    hoverArea.addEventListener('mouseleave', function() {
        hoverArea.textContent = 'Hover Over Me';
        hoverArea.classList.remove('hovered'); // Remove class
    });

    // Keypress Detection
    const keypressInput = document.getElementById('keypress-input');
    const keypressOutput = document.getElementById('keypress-output');

    // Using 'input' event for real-time feedback on input change
    keypressInput.addEventListener('input', function(event) {
        keypressOutput.textContent = `You are typing. Current value: "${event.target.value}"`;
        // You could use keydown/keyup if you specifically needed the key code
        // keypressInput.addEventListener('keydown', function(event) {
        //     keypressOutput.textContent = `Key pressed: ${event.key} (Code: ${event.code})`;
        // });
    });


    // Double-click
    const doubleClickBtn = document.getElementById('double-click-btn');
    const doubleClickOutput = document.getElementById('double-click-output');

    doubleClickBtn.addEventListener('dblclick', function() {
        doubleClickOutput.textContent = 'Button was double-clicked!';
        console.log('Double click button double-clicked!');
    });


    // ======================================================
    // 2. Interactive Elements
    // ======================================================

    // Button that changes text or color
    const toggleButton = document.getElementById('toggle-button');

    toggleButton.addEventListener('click', function() {
        if (toggleButton.classList.contains('on')) {
            toggleButton.textContent = 'Toggle State (Off)';
            toggleButton.classList.remove('on');
            toggleButton.classList.add('off');
        } else {
            toggleButton.textContent = 'Toggle State (On)';
            toggleButton.classList.remove('off');
            toggleButton.classList.add('on');
        }
        // Set initial state
         if (!toggleButton.classList.contains('on') && !toggleButton.classList.contains('off')) {
             toggleButton.classList.add('off');
         }
    });
    // Set initial state visually
    toggleButton.classList.add('off');


    // Simple Image Slideshow
    const slideshowImg = document.getElementById('slideshow-img');
    const prevSlideBtn = document.getElementById('prev-slide-btn');
    const nextSlideBtn = document.getElementById('next-slide-btn');
    const slideshowStatus = document.querySelector('.slideshow-status');
    const slideshowContainer = document.getElementById('slideshow-container');


    const images = [
        'https://via.placeholder.com/600x300/FF5733/FFFFFF?text=Image+1',
        'https://via.placeholder.com/600x300/33FF57/FFFFFF?text=Image+2',
        'https://via.placeholder.com/600x300/3357FF/FFFFFF?text=Image+3',
        'https://via.placeholder.com/600x300/F0FF33/000000?text=Image+4'
    ];
    let currentImageIndex = 0;
    let slideshowInterval;

    function updateSlide() {
        slideshowImg.src = images[currentImageIndex];
        slideshowStatus.textContent = `Image ${currentImageIndex + 1} of ${images.length}`;
    }

    function nextSlide() {
        currentImageIndex = (currentImageIndex + 1) % images.length; // Loop back to start
        updateSlide();
    }

    function prevSlide() {
        currentImageIndex = (currentImageIndex - 1 + images.length) % images.length; // Loop back to end
        updateSlide();
    }

    // Add event listeners for controls
    nextSlideBtn.addEventListener('click', function() {
        nextSlide();
        resetSlideshowInterval(); // Reset timer on manual navigation
    });

    prevSlideBtn.addEventListener('click', function() {
        prevSlide();
         resetSlideshowInterval(); // Reset timer on manual navigation
    });

    // Bonus: Automatic Slideshow
    function startSlideshow() {
        // Clear any existing interval
        clearInterval(slideshowInterval);
        slideshowInterval = setInterval(nextSlide, 3000); // Change image every 3 seconds
    }

    function stopSlideshow() {
        clearInterval(slideshowInterval);
    }

    function resetSlideshowInterval() {
         stopSlideshow();
         startSlideshow();
    }


    // Bonus: Pause slideshow on hover
    slideshowContainer.addEventListener('mouseenter', stopSlideshow);
    slideshowContainer.addEventListener('mouseleave', startSlideshow);


    // Initialize the slideshow
    updateSlide(); // Display the first image
    startSlideshow(); // Start automatic play


    // Basic Tabs
    const tabButtons = document.querySelectorAll('.tab-button');
    const tabPanes = document.querySelectorAll('.tab-pane');

    tabButtons.forEach(button => {
        button.addEventListener('click', function() {
            const targetTabId = this.dataset.tab; // Get the data-tab attribute value

            // Remove 'active' class from all buttons and panes
            tabButtons.forEach(btn => btn.classList.remove('active'));
            tabPanes.forEach(pane => pane.classList.remove('active'));

            // Add 'active' class to the clicked button and its corresponding pane
            this.classList.add('active');
            document.getElementById(targetTabId).classList.add('active');
        });
    });


    // ======================================================
    // 3. Form Validation
    // ======================================================

    const registrationForm = document.getElementById('registration-form');
    const usernameInput = document.getElementById('username');
    const emailInput = document.getElementById('email');
    const passwordInput = document.getElementById('password');
    const formStatus = document.getElementById('form-status');

    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/; // Simple email regex

    // Function to display validation feedback for a field
    function validateField(inputElement, validationFunction, errorMessage) {
        const value = inputElement.value.trim();
        const errorSpan = inputElement.nextElementSibling; // Get the error span

        if (validationFunction(value)) {
            // Valid
            inputElement.classList.remove('invalid');
            inputElement.classList.add('valid');
            errorSpan.textContent = ''; // Clear error message
            return true;
        } else {
            // Invalid
            inputElement.classList.remove('valid');
            inputElement.classList.add('invalid');
            errorSpan.textContent = errorMessage; // Display error message
            return false;
        }
    }

    // Validation functions
    function isRequired(value) {
        return value !== '';
    }

    function isValidEmail(value) {
        return emailRegex.test(value);
    }

    function isMinLength(value, minLen) {
        return value.length >= minLen;
    }


    // Bonus: Real-time validation feedback while typing
    usernameInput.addEventListener('input', function() {
        validateField(usernameInput, isRequired, 'Username is required.');
    });

    emailInput.addEventListener('input', function() {
        // Check required first, then email format if not empty
        if (!validateField(emailInput, isRequired, 'Email is required.')) {
            // If required check fails, stop here
            return;
        }
        validateField(emailInput, isValidEmail, 'Please enter a valid email format.');
    });

    passwordInput.addEventListener('input', function() {
         // Check required first, then length if not empty
         if (!validateField(passwordInput, isRequired, 'Password is required.')) {
            // If required check fails, stop here
            return;
        }
        validateField(passwordInput, (val) => isMinLength(val, 8), 'Password must be at least 8 characters.');
    });


    // Form Submission Validation
    registrationForm.addEventListener('submit', function(event) {
        event.preventDefault(); // Prevent the default form submission

        // Perform validation for all fields on submit
        const isUsernameValid = validateField(usernameInput, isRequired, 'Username is required.');

        const isEmailRequiredValid = validateField(emailInput, isRequired, 'Email is required.');
        const isEmailFormatValid = isEmailRequiredValid ? validateField(emailInput, isValidEmail, 'Please enter a valid email format.') : false; // Only check format if required field is filled

        const isPasswordRequiredValid = validateField(passwordInput, isRequired, 'Password is required.');
        const isPasswordLengthValid = isPasswordRequiredValid ? validateField(passwordInput, (val) => isMinLength(val, 8), 'Password must be at least 8 characters.') : false; // Only check length if required field is filled


        // Check if all fields are valid
        if (isUsernameValid && isEmailRequiredValid && isEmailFormatValid && isPasswordRequiredValid && isPasswordLengthValid) {
            // Form is valid!
            formStatus.textContent = 'Registration successful!';
            formStatus.classList.remove('error');
            console.log('Form submitted successfully!');
            // Here you would typically send the data to a server (e.g., using fetch API)

            // Optional: Reset the form after successful submission
            // registrationForm.reset();

        } else {
            // Form is invalid
            formStatus.textContent = 'Please fix the errors in the form.';
            formStatus.classList.add('error');
            console.log('Form validation failed.');
        }
    });

}); // End of DOMContentLoaded listener
