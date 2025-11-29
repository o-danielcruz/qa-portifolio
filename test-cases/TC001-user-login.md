# Test Case: User Login - Valid Credentials

**Test Case ID:** TC001  
**Module:** Authentication  
**Priority:** High  
**Created by:** Daniel Cruz  
**Date:** November 2024

---

## Objective
Verify that users can successfully log in with valid credentials.

## Preconditions
- User has a registered account
- User is on the login page
- User credentials are valid and active

## Test Data
| Field | Value |
|-------|-------|
| Email | testuser@example.com |
| Password | SecurePass123! |

## Test Steps

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to application login page | Login page loads successfully with email and password fields visible |
| 2 | Enter valid email in the email field | Email is accepted and displayed in the field |
| 3 | Enter valid password in the password field | Password is masked with asterisks or dots |
| 4 | Click "Login" button | User is authenticated and redirected to dashboard |
| 5 | Verify user session | User's name or profile picture appears in header/navigation bar |

## Expected Results
- User successfully logs in without errors
- User is redirected to the dashboard/home page
- Session token is created (visible in cookies/local storage)
- Welcome message displays user's name
- All navigation elements are accessible

## Post-conditions
- User remains logged in until they explicitly log out or session expires
- User activity is tracked in the system logs

## Notes
- Test with different browsers (Chrome, Firefox, Safari, Edge)
- Verify mobile responsiveness
- Check session timeout behavior (typically 30 minutes of inactivity)

---

**Status:** ✅ Passed  
**Executed on:** [Date]  
**Environment:** Production-like staging environment
