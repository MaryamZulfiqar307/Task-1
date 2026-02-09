Lab: Intro to Continuous Integration (CI)
🏁 Step 1: Setup
Click the Actions tab in your GitHub repository. You should see a workflow run listed (triggered by your initial fork/push).
Click on the workflow run to see the steps. Ensure all steps have a green checkmark ✅.
🧪 Step 2: The “Happy Path”
Open src/calculator.py.
Add a small comment to the file (e.g., # This is a change).
Commit and push the change to GitHub.
Go to the Actions tab immediately. Watch the pipeline start automatically.
Observe how it sets up Python, installs dependencies, and runs the tests. It should pass.
💥 Step 3: Break the Build!
Now, let’s see what happens when we make a mistake.

Open src/calculator.py.
Change the add function so it is incorrect:
def add(x, y):
    return x - y  # This is a bug!
Commit and push this change.
Go to the Actions tab.
Observe: The pipeline will fail (Red X ❌).
Click into the failure details and find the specific test that failed (test_add). This demonstrates how CI catches bugs before they reach production.
🚑 Step 4: Fix the Build
Revert the change in src/calculator.py to fix the bug:
def add(x, y):
    return x + y
Commit and push.
Verify in the Actions tab that the build is Green ✅ again.
