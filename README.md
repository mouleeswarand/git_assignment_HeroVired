# git_assignment_HeroVired

https://github.com/mouleeswarand/git_assignment_HeroVired

Assignment 1 -  CalculatorPlus - GitHub Commands

Step 1: GitHub repository: git clone https://github.com/mouleeswarand/git_assignment_HeroVired.git

Step 2: Create a “Dev” Branch

git checkout -b dev	#create and switch to dev branch

CalculatorPlus.py	#create a new file using the VI editor and add the code

import math

class Calculator:

    def add(self, a, b):
        return a + b

    def subtract(self, a, b):
        return a - b

    def multiply(self, a, b):
        return a * b

    def divide(self, a, b):
        return a / b

git add .
git commit -m "Added calculator base code"
git push origin dev


Step 3: Merge the branch Dev - > Main 
git checkout main
git merge dev
git tag v1.0
git push origin main --tags

Step 4: classmates as collaborators

Step 5: Create a new branch “feature/sqrt”
Get checkout -b feature/sqrt

Step 6: Add the Sqrt code

def square_root(self, x):
return math.sqrt(x)


if __name__ == "__main__":
calculator = Calculator()

num1 = 16
num2 = 4

print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")

num3 = 25
print(f"The square root of {num3} = {calculator.square_root(num3)}")


Step 7 : switch back to the ‘dev’ branch and fix the divide formula

def divide(self, a, b):
    if b == 0:
        raise ValueError("Cannot divide by zero.")
    return a / b

#commit the changes
git add .
git commit -m "Fixed divide by zero bug"
git push origin dev

Step 8: Switch back to feature/sqrt and merge with dev for current changes
git checkout feature/sqrt
git merge dev
git add .
git commit -m "feature/sqrt - updated"
git push origin feature/sqrt

Step 9: Pull Request Workflow
Create PR (feature/sqrt -> Dev)
Request review
Make changes if needed

Step 10: Final Merge
Create PR (Dev - > main)
git checkout main
git merge dev


Assignment 2 -  LFS(200 MB) - GitHub Commands

Download and Install the https://git-lfs.github.com/
git lfs install
git init
git lfs track "*.zip"
It create .gitattributes folder
Now add the binary folder (200 mb) in the folder
git add .gitattributes
git add large-file.zip
git commit -m "Add large binary file using Git LFS"
git push --set-upstream origin lfs
git lfs ls-files	#16e122e099 * herovired_lfs.zip
git clone https://github.com/mouleeswarand/git_assignment_HeroVired.git
git lfs pull


git tag v2.0
git push origin main --tags
