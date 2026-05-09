# 🎂 Age Calculator

A simple web-based Age Calculator built using **HTML, CSS, and JavaScript**.  
It allows users to select their date of birth using a built-in date picker and calculates their exact age in years.

---

## 🚀 Features

- 📅 Built-in JavaScript date picker
- ⚡ Instant age calculation
- 🎯 Clean and minimal UI
- 📱 Responsive design (works on mobile and desktop)

---

## 🛠️ Technologies Used

- HTML5
- CSS3
- JavaScript (Vanilla)

---

## 📸 How It Works

1. The user selects their date of birth using a date input field.
2. JavaScript reads the selected date.
3. The current date is compared with the birth date.
4. The difference in years is calculated and adjusted if the birthday has not yet occurred this year.
5. The result is displayed below the button.

---

## 🧠 Challenge I Faced

At first, I thought calculating age would be as simple as:

age = currentYear - birthYear;

However, I quickly noticed a problem — the result was often incorrect.

❌ The Issue

The calculation ignored whether the user's birthday had already happened in the current year.

For example:

If someone is born in December 2000
And today is May 2026
The simple formula would incorrectly say they are 26, even though they are still 25
💡 The Solution

To fix this, I had to account for the month and day difference, not just the year.

I added a condition:

If the current month is before the birth month → subtract 1 year
If it's the same month but the day hasn't passed → subtract 1 year
if (monthDiff < 0 || (monthDiff === 0 && dayDiff < 0)) {
  age--;
}

✔ Final Result

This made the calculator accurate and reliable, handling real-world edge cases properly.

📌 Learning Outcome

This project helped me understand:

How JavaScript Date objects work
Why time-based calculations need edge-case handling
The importance of validating logic beyond simple formulas
📷 Future Improvements
Show age in months and days
Add animations for result display
Improve UI with modern design styles
Add validation for future dates
👨‍💻 MrM

Project URL https://github.com/CodeWithMrM/Age-Calculator

Built by a developer learning and improving JavaScript fundamentals through hands-on projects.
