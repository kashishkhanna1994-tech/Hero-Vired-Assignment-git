# Hero-Vired-Assignment-git

## Git LFS (Large File Storage) -- Task2

## Step 1: Verify Git LFS Installation
git lfs version

## Step 2: Initialize Git LFS
git lfs install

## Step 3: Create and Switch to New Branch
git checkout -b lfs

## Step 4: Track Large Files Using Git LFS
git lfs track "*.zip"

Verify tracking: cat .gitattributes

## Step 5: Create a Large File (>200MB)
truncate -s 250M largefile.zip

Verify file:
ls -lh

## Step 6: Add Files to Staging
git add .gitattributes git add largefile.zip

## Step 7: Commit Changes
git commit -m "Added large file using Git LFS"

## Step 8: Push to Remote Repository
git push origin lfs

## Step 9: Verify File is Tracked by LFS
git lfs ls-files
