Sure! Here's a clean and formatted `README.md` file based on your instructions:

---

```markdown
# WebdriverIo.master

## 🔧 To Use This Project

### Step 1  
Download the folder or clone the repository:

```bash
git clone <repository-url>
```

### Step 2  
Make sure **Node.js** is installed on your system:

```bash
node -v
```

### Step 3  
Open terminal/cmd → Go to project folder → Run:

```bash
npm install     # Downloads and installs all required libraries from package.json
npx wdio        # Runs the tests
```

---

## 🚀 Project Setup & WebdriverIO Installation

### Step 1  
Create a new folder and open it in an IDE (e.g., VS Code)

### Step 2  
Open terminal in VS Code and run:

```bash
npm init -y
npm init wdio
```

### Step 3  
Follow the prompts to configure your WebdriverIO project.

### Step 4  
Check the installed WebdriverIO version:

```bash
npm ls webdriverio
```

### Step 5  
Ensure `wdio.conf.js` and the required project folders are created.

### Step 6  
To run existing tests:

- **Run all tests** (configured in `wdio.conf.js`):

```bash
npx wdio run wdio.conf.js
```

or

```bash
npm run wdio
```

- **Run specific test**:

```bash
npx wdio run wdio.conf.js --spec test1.js
```

---

## 🧪 How to Create Tests

### Step 1  
Create a new file under the `spec` folder.

### Step 2  
Add your test using Mocha’s `describe` and `it` blocks:

```js
describe('Demo Tests', () => {
   it('My 1st Test', async () => {
       await browser.url('https://google.com/');
       await browser.pause(2000);
       await $('[name="q"]').setValue("WebdriverIO");
       await $('button[type="submit"]').click();
       await browser.keys('Enter');
   });
});
```

### Quick Selector Notes

- `$()` — Single element selector  
- `$$()` — Multiple elements selector

---

## 📊 How to Generate and View Reports (Allure)

### Step 1  
Install Allure reporter:

```bash
npm install @wdio/allure-reporter --save-dev
```

### Step 2  
Add the reporter to your `wdio.conf.js`:

```js
reporters: ['spec', ['allure', {
    outputDir: 'allure-results',
    disableWebdriverStepsReporting: true,
    disableWebdriverScreenshotsReporting: false,
}]],
```

### Step 3  
Run your test and verify the `allure-results` folder is created.

### Step 4  
Install the Allure CLI:

```bash
npm install -g allure-commandline --save-dev
```

### Step 5  
Generate and open report:

```bash
allure generate allure-results --clean
allure open
```

---

Let me know if you'd like this saved as a file or need help pushing it to your repo!
