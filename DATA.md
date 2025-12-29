# Healthcare Patient Portal - QA Testing Project

## 📚 Table of Contents
- [Project Overview](#project-overview)
- [Test Objectives](#test-objectives)
- [Test Cases](#test-cases)
- [Bug Reports](#bug-reports)
- [Tools Used](#tools-used)
- [Contact](#contact)

[Rest of your content...]
# BUG-HR-001: No Account Lockout After Multiple Failed Login Attempts

**Severity**: Critical
**Priority**: Critical
**Status**: Open
**Reported Date**: [Current Date]
**Reported By**: [Your Name]

## Environment
- Browser: Chrome 120.0
- OS: Windows 11
- URL: https://healthconnect.example.com/login

## Description
The system allows unlimited login attempts without locking the account, creating a security vulnerability for brute force attacks.

## Steps to Reproduce
1. Navigate to login page
2. Enter valid email address
3. Enter incorrect password
4. Click "Login"
5. Repeat steps 3-4 more than 10 times
6. Observe that login attempts continue

## Expected Result
After 5 failed attempts, account should be temporarily locked for 30 minutes

## Actual Result
System continues to allow login attempts indefinitely

## Impact
High security risk - accounts vulnerable to brute force attacks

## Recommendation
Implement account lockout after 5 failed attempts with 30-minute cooldown period
