# A Better Abonded Auto Intake Form
Goal:  Automate the PBOT [Abandoned Auto intake form](https://www.portland.gov/transportation/parking/abandoned-auto) so it is easier to report cars that fit the "abandoned" definition, including: expired license plate tags, no license plates, inoperable vehicles, and more.

## Desired Capabilities
- Predict vehicle info with a single photo: vehicle type, make, color, license plate (state and alphanumeric)
- Automatically populate location (either geotag on photo or direct browser location)
- Pre-populate repeated/standard form elements per user (save per user device)

## Additional Features
- Record all submissions (non-PII fields) to database to collect and do downstream analysis
- Integrate https://safelanes.org/ capabilities
- Capture and Report other traffic violations

# Proposed Flow
![Form submission flow](flow-form-01.png)

# Project Background
**Problem**:  I want to report cars with expired/invalid/no plates, and after a recent call with a Parking Enforcement representative (503-823-5195, option 4). The agent told me to report any expired tags to the abandoned auto form--even if the vehicle is driven daily and not actually "abandoned".  In fact, if the vehicle moves, the agent said to just submit another form to "help them find the car".  Now, there are so many cars in my neighborhood with expired registration, that I cannot spend the 5-10 minutes per car submitting the form, especially as they move (as an example, I walked 2 square blocks and have literally 12 cars to report).

**Opportunity**:  PBOT recently redesigned their Abandoned Auto intake form: it's no longer behind a login and it's slightly shorter.  I want to more-automatically collect, inject, and submit the form with the required information.  I have a server running https://platerecognizer.com/, so we can submit pics and let machine learning predict the Vehicle Info: vehicle type, make, color, and license plate (if exists). Then POST all that info in-lieu of the intake form.

**Request**: I need help designing and then developing the apps/script(s) to either inject the info to the form or take the correct form submission "hand-shake" and submit it more automatically.  If you know of libraries, scripts, or would be willing to help me design this as an open source project, I would be very appreciative.  I am not familiar with tapping into forms to automate this kind of submission, so I could use any guidance you can send my way.  I can build the photo submission and return the payloads, help coordinate the work, etc.
