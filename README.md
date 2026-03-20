## Hero-Vired-Assignment-git
## Git Workflow – Geometry Calculator Project --- Task 3

## Step 1: Clone Repository and Switch to Dev
git checkout dev git pull origin dev

## Step 2: Create Geometry Calculator Branch
git checkout -b geometry-calculator

## Step 3: Add Initial Python File
vim geometry_calculator.py

import math

class GeometryCalculator:

def calculate_circle_area(self, radius):
    return math.pi * radius ** 2

def calculate_rectangle_area(self, length, width):
    return length * width
if name == "main": calculator = GeometryCalculator()

## Step 4: Commit Base Code
git add . git commit -m "Initial geometry calculator structure" git push origin geometry-calculator

## Step 5: Create Circle Feature Branch
git checkout -b feature/circle-area

## Step 6: Work on Circle Feature (Incomplete)
radius = 5
print(calculator.calculate_circle_area(radius))

## Step 7: Stash Circle Feature
git stash

## Step 8: Create Rectangle Feature Branch
git checkout -b feature/rectangle-area

## Step 9: Work on Rectangle Feature (Incomplete)
length = 10
width = 6
print(calculator.calculate_rectangle_area(length, width))

## Step 10: Stash Rectangle Feature
git stash

## Step 11: Switch Back to Circle Feature
git checkout feature/circle-area git stash list git stash apply stash@{1}

## Step 12: Complete Circle Feature
radius = 5 print(f"Circle Area = {calculator.calculate_circle_area(radius)}")

## Step 13: Commit Circle Feature
git add . git commit -m "Completed circle area feature" git push origin feature/circle-area

## Step 14: Switch Back to Rectangle Feature
git checkout feature/rectangle-area git stash apply stash@{0}

## Step 15: Complete Rectangle Feature
length = 10 width = 6 print(f"Rectangle Area = {calculator.calculate_rectangle_area(length, width)}")

## Step 16: Commit Rectangle Feature
git add . git commit -m "Completed rectangle area feature" git push origin feature/rectangle-area

## Step 17: Create Pull Requests

## Step 18: Merge After Review
git checkout main git merge dev git push origin main

## Step 19: Final Output Circle Area = 78.53981633974483 Rectangle Area = 60
