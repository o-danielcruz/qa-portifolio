# Test Case: Password Recovery - Forgot Password Flow

**Test Case ID:** TC003  
**Module:** Authentication  
**Priority:** Medium  
**Created by:** Daniel Cruz  
**Date:** November 2024

---

## Objective
Verify that users can successfully recover their password through the "Forgot Password" functionality.

## Preconditions
- User has a registered account
- User has access to registered email address
- User is on the login page

## Test Data
| Field | Value |
|-------|-------|
| Registered Email | testuser@example.com |

## Test Steps

| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Navigate to login page | Login page loads successfully |
| 2 | Click "Forgot Password?" link | User is redirected to password recovery page |
| 3 | Enter registered email address | Email field accepts valid email format |
| 4 | Click "Send Reset Link" button | Success message confirms email was sent |
| 5 | Check email inbox | Password reset email is received within 2-5 minutes |
| 6 | Verify email content | Email contains reset link and clear instructions |
| 7 | Click password reset link in email | User is redirected to "Create New Password" page |
| 8 | Enter new password | Password field accepts input and validates requirements |
| 9 | Confirm new password | Confirmation field matches new password |
| 10 | Click "Reset Password" button | Success message confirms password was updated |
| 11 | Attempt login with old password | Login fails with error message |
| 12 | Attempt login with new password | Login succeeds and user is redirected to dashboard |

## Expected Results
- Password reset email is sent successfully
- Reset link is valid and works only once
- Reset link expires after specified time (usually 24 hours)
- New password meets security requirements
- Old password no longer works
- User can log in immediately with new password

## Security Considerations
- Reset link should be single-use (invalid after password is changed)
- Reset link should expire after 24 hours
- Email should not reveal whether account exists (security best practice)
- Password requirements are enforced

## Post-conditions
- User's password is updated in the database (hashed)
- Old password is invalidated
- Reset token is marked as used/expired

---

**Status:** ✅ Passed  
**Executed on:** [Date]  
**Environment:** Staging
