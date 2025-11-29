# Test Case: User Registration - New Account Creation

**Test Case ID:** TC002  
**Module:** User Management  
**Priority:** High  
**Created by:** Daniel Cruz  
**Date:** November 2024

---

## Objective
Verify that new users can successfully create an account with valid information.

## Preconditions
- User is on the registration page
- Email address is not already registered in the system

## Test Data
| Field | Value |
|-------|-------|
| First Name | John |
| Last Name | Doe |
| Email | newuser@example.com |
| Password | SecurePass123! |
| Confirm Password | SecurePass123! |

## Test Steps

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to registration page | Registration form displays with all required fields |
| 2 | Enter first name | Field accepts alphabetic characters |
| 3 | Enter last name | Field accepts alphabetic characters |
| 4 | Enter valid email address | Field accepts email in correct format |
| 5 | Enter password meeting requirements | Password field accepts input and masks characters |
| 6 | Re-enter password in confirmation field | Confirm password field matches password |
| 7 | Accept Terms & Conditions checkbox | Checkbox is checked |
| 8 | Click "Register" or "Sign Up" button | Form is submitted successfully |
| 9 | Check for confirmation message | Success message appears confirming registration |
| 10 | Check email inbox | Verification email is received |
| 11 | Click verification link in email | Email is verified and account is activated |

## Expected Results
- Account is created successfully in the database
- User receives confirmation message on screen
- Verification email is sent within 1-2 minutes
- User can log in after email verification
- User data is stored securely (password is hashed)

## Negative Test Scenarios to Consider
- Email already exists
- Password doesn't meet requirements
- Passwords don't match
- Required fields left empty
- Invalid email format
- Terms & Conditions not accepted

## Post-conditions
- User account exists in the system
- User can log in with registered credentials
- User profile is created with provided information

---

**Status:** ✅ Passed  
**Executed on:** [Date]  
**Environment:** Staging
