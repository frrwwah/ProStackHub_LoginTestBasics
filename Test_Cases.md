# Task 1: LoginTestBasics - Farwa Asad - PSH/INT/2026/706
App Tested: https://www.saucedemo.com (Real App)
Environment: Windows 11, Chrome 128, standard_user / secret_sauce

| ID | Scenario | Precondition | Steps | Expected | Actual | Status |
| TC01 | Valid login | On login page | Enter valid user+pass -> Login | Redirect to Products | Products shown | Pass |
| TC02 | Invalid pass | On login page | Valid user + wrong pass | Error: Username and password do not match | Same error | Pass |
| TC03 | Invalid user | On login page | Invalid user + valid pass | Error | Same | Pass |
| TC04 | Empty both | On login page | Leave blank -> Login | Error: Username is required | Same | Pass |
| TC05 | Empty password | On login page | User only | Error: Password is required | Same | Pass |
| TC06 | Empty username | On login page | Pass only | Error: Username is required | Same | Pass |
| TC07 | Case upper user | On login page | STANDARD_USER | Fail - case sensitive | Fail as expected | Pass |
| TC08 | Case upper pass | On login page | SECRET_SAUCE | Fail - case sensitive | Fail as expected | Pass |
| TC09 | Boundary min 1 char | On login page | User + a | Error, no crash | Handled | Pass |
| TC10 | Boundary max 100 char | On login page | User + a*100 | No crash | Handled | Pass |
| TC11 | SQL Injection | On login page | ' OR '1'='1 | Should block | Blocked | Pass |
| TC12 | Locked user | On login page | locked_out_user | Error: locked out | Same | Pass |

Execution: 12 Pass, 0 Fail - 100% Pass Rate
Boundary cases: TC09 (min), TC10 (max) included as required.
