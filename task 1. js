
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Palindrome Checker</title>
    <link rel="stylesheet" href="style.css">
    <script src="script.js" defer></script>
</head>
<body>

    <div class="container">
        <h1>Palindrome Checker</h1>
        <p>level</p>

        <div class="checker">
            <label for="wordInput">level:</label>
            <input type="text" id="wordInput" placeholder="e.g. level">

            <button id="checkButton">Check Word</button>

            <p id="result" aria-live="polite"></p>
        </div>

        <div class="history-section">
            <h2>Previous Checks</h2>
            <ul id="historyList">
                <li>No words checked yet.</li>
            </ul>
        </div>
    </div>

</body>
</html
 {
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    background-color: #f1f5f9;
    color: #1e293b;
    margin: 0;
    padding: 30px 15px;
}

.container {
    max-width: 600px;
    margin: 0 auto;
}

h1 {
    text-align: center;
    color: #4338ca;
}

/* Header */
.header {
    text-align: center;
    margin-bottom: 30px;
}

.logo {
    width: 58px;
    height: 58px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 auto 14px;
    background: #5146d8;
    color: white;
    font-size: 30px;
    font-weight: bold;
    border-radius: 16px;
}

.header h1 {
    font-size: clamp(26px, 5vw, 36px);
    margin-bottom: 8px;
}

.header p,
.history-header p {
    color: #707991;
}

/* Main cards */
.checker-card,
.history-card {
    background: white;
background: #5146d8;
    color: white;
    font-size: 30px;
    font-weight: bold;
    border-radius: 16px;
}

.header h1 {
    font-size: clamp(26px, 5vw, 36px);
    margin-bottom: 8px;
}

.header p,
.history-header p {
    color: #70799
    
    
   //  Main cards 
.checker-card,
.history-card {
    background: white;
    border-radius: 16px;
    padding: 28px;
    margin-bottom: 24px;
    box-shadow: 0 8px 28px rgba(35, 45, 80, 0.06);
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 10px;
}
input {
    width: 100%;
    padding: 15px;
    font-size: 16px;
    border: 1px solid #d9deeb;
    border-radius: 9px;
    margin-bottom: 16px;
    outline: none;
}

input:focus {
    border-color: #5146d8;
    box-shadow: 0 0 0 3px rgba(81, 70, 216, 0.12);
}

button {
    width: 100%;
    padding: 14px;
    border: none;
    border-radius: 9px;
    background: #5146d8;
    color: white;
    font-size: 16px;
    font-weight: bold;
    cursor: pointer;
    transition: background 0.2s;
    button:hover {
    background: #4035bd;
}

/* Result message */
.result {
    margin-top: 20px;
    padding: 14px;
    border-radius: 9px;
    background: #f3f5fb;
    color: #707991;
    overflow-wrap: anywhere;
}

.result.success {
    background: #e7f8ee;
    color: #176c3a;
}

.result.failure {
    background: #fff0ed;
     color: #b52f24;
}

.result.error {
    background: #fff5dc;
    color: #875a00;
}

/* History section */
.history-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 12px;
    margin-bottom: 22px;
}

.history-header h2 {
    font-size: 22px;
}
.count {
    white-space: nowrap;
    background: #efedff;
    color: #5146d8;
    padding: 6px 12px;
    border-radius: 20px;
    font-size: 13px;
    font-weight: bold;
}

.table-wrapper {
    overflow-x: auto;
}

table {
    width: 100%;
    border-collapse: collapse;
    text-align: left;
}

th,

td {
    padding: 14px 12px;
    border-bottom: 1px solid #edf0f6;
    overflow-wrap: anywhere;
}

th {
    color: #707991;
    font-size: 13px;
    text-transform: uppercase;
}

td {
    font-size: 14px;
}

.status {
    display: inline-block;
    padding: 4px 9px;
    border-radius: 20px;
    font-size: 12px;
    font-weight: bold;
    white-space: nowrap;.status.yes {
    background: #e7f8ee;
    color: #176c3a;
}

.status.no {
    background: #fff0ed;
    color: #b52f24;
}

.empty-state {
    text-align: center;
    color: #8b93a6;
    padding: 28px 12px;
}

footer {
    text-align: center;
    color: #8b93a6;
    font-size: 13px;
    padding: 10px;
}

/* Mobile layout */
@media (max-width: 520px) {
    body {
        padding: 24px 12px;
 
        
     .checker-card,
    .history-card {
        padding: 20px 16px;
    }

    .history-header {
        align-items: flex-start;
        flex-direction: column;
    }

    th,
    td {
        padding: 12px 8px;
        font-size: 12px;
    }
}
/* Array to store all checked words and their results */
const history = [];

/* Get the HTML elements */
const form = document.getElementById("palindromeForm");
const wordInput = document.getElementById("wordInput)
const result = document.getElementById("result");
const historyList = document.getElementById("historyList");
const totalChecks = document.getElementById("totalChecks");

/* Check whether a word or phrase is a palindrome */
function checkPalindrome(word) {
    // Remove spaces and punctuation, then ignore letter case
    const cleanedWord = word
        .toLowerCase()
        .replace(/[^a-z0-9]/g, "");

    // Reverse the cleaned string
    const reversedWord = cleanedWord
        .split("")
        .reverse()
        .join("");

    // Compare the original cleaned string with its reverse
    const isPalindrome =
        cleanedWord.length > 0 &&
        cleanedWord === reversedWord;

    return {
        isPalindrome: isPalindrome,
        reversed: reversedWord
    };
}/* Handle the form submission */
form.addEventListener("submit", function (event) {
    // Stop the page from refreshing
    event.preventDefault();

    const word = wordInput.value.trim();

    // Validate the input
    if (word === "") {
        result.textContent = "Please enter a word or phrase.";
        result.className = "result error";
        return;
    }

       const answer = checkPalindrome(word);

    // Store the entry and its result in the array
    const entry = {
        word: word,
        reversed: answer.reversed,
        isPalindrome: answer.isPalindrome
    };

    history.unshift(entry);

    // Show the result to the user
    if (answer.isPalindrome) {
        result.textContent =
            `"${word}" is a palindrome!`;
        result.className = "result success";
    } else {
        result.textContent =
            `"${word}" is not a palindrome.`;
        result.className = "result failure";
    }

    // Refresh the history displayed on the page
    displayHistory();

    
    // Clear the input for the next word
    wordInput.value = "";
    wordInput.focus();
});

/* Display the stored entries in the HTML table */
function displayHistory() {
    // Remove the old table contents
    historyList.replaceChildren();

    // Update the number of checks
    totalChecks.textContent =
        `${history.length} ${history.length === 1 ? "check" : "checks"}`;

    // Show a message if the array is empty
    if (history.length === 0) {
        const row = document.createElement("tr");
        const cell = document.createElement("td");

        cell.colSpan = 3;
        cell.className = "empty-state";
        cell.textContent = "No words checked yet.";

        row.appendChild(cell);
        historyList.appendChild(row);
        return;
    }

    // Loop through the history array
    history.forEach(function (entry) {
        const row = document.createElement("tr");

        const wordCell = document.createElement("td");
        wordCell.textContent = entry.word;

        const reversedCell = document.createElement("td");
        reversedCell.textContent = entry.reversed || "(empty)";

        const resultCell = document.createElement("td");
        const status = document.createElement("span");

        if (entry.isPalindrome) {
            status.textContent = "Palindrome";
            status.className = "status yes";
        } else {
            status.textContent = "Not a palindrome";
            status.className = "status no";

        resultCell.appendChild(status);

        row.appendChild(wordCell);
        row.appendChild(reversedCell);
        row.appendChild(resultCell);


