# Hero-Vired-Assignment-git

## Step-by-Step Implementation --- Task1

## 1. Repository Setup
cd /C/Users/nicsi/Desktop/Hero-Vired-Assignment-git git init

echo "# Hero-Vired-Assignment-git" >> README.md git add README.md git commit -m "first commit"

git branch -M main git remote add origin https://github.com/kashishkhanna1994-tech/Hero-Vired-Assignment-git.git git push -u origin main

## 2. Create Development Branch
git checkout -b dev

## 3. Add Calculator Code
touch calculator.py Add the following code:

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

def square_root(self, x):
    return math.sqrt(x)
if name == "main": calculator = Calculator()

num1 = 16
num2 = 4

print(f"{num1} + {num2} = {calculator.add(num1, num2)}")
print(f"{num1} - {num2} = {calculator.subtract(num1, num2)}")
print(f"{num1} * {num2} = {calculator.multiply(num1, num2)}")
print(f"{num1} / {num2} = {calculator.divide(num1, num2)}")

num3 = 25
print(f"The square root of {num3} = {calculator.square_root(num3)}")

## 4. Commit & Push to Dev Branch
git add . git commit -m "Added calculator with sqrt feature" git push origin dev

## 5. Merge Dev → Main (Version 1 Release)
git checkout main git pull origin main git merge dev

git tag v1.0 git push origin main --tags

## 6. Create Feature Branch
git checkout dev git checkout -b feature/sqrt

git add . git commit -m "Working on sqrt feature" git push origin feature/sqrt

## 7. Bug Fix in Dev Branch
git checkout dev

Update divide function: def divide(self, a, b): if b == 0: raise ValueError("Cannot divide by zero.") return a / b git add . git commit -m "Fixed division by zero bug" git push origin dev

## 8. Update Feature Branch
git checkout feature/sqrt git merge dev

## 9. Create Pull Request
Go to GitHub repository

Click Compare & Pull Request

Base branch: main

Compare branch: feature/sqrt

## 10. Code Review & Changes
git add . git commit -m "Updated after code review" git push origin feature/sqrt

## 11. Merge Feature → Dev
git checkout dev git merge feature/sqrt git push origin dev

## 12. Final Merge & Version 2 Release
git checkout main git merge dev

git tag v2.0 git push origin main --tags

✅ Final Output Test

python calculator.py Expected Output: 16 + 4 = 20 16 - 4 = 12 16 * 4 = 64
