# **BUSINESS REQUIREMENTS DOCUMENT** 

### **Travel Planning & Booking Application** 

_Version 1.0  |   9 October 2026_ 

Project Name: SKY Travels (temp name) 

Tam Members   - 
- Shashi Kanth Yadav (Team Leader) 
- Mohammad Arif 
- Jahnavi 
- Govind Maheshwari
- Pradeep 

Course: BCA (Final Year) 

College/University: SMSG Jain Degree College 

Document purpose: Define the business problem, objectives, users, scope, and expected capabilities of a travel application before detailed design and development begin. 

## **1. Project Overview** 

The Travel Planning & Booking Application will help travellers discover destinations, plan trips, organise itineraries, estimate expenses, and access accommodation or transport booking options in one place. The first release is intended as a practical MVP (minimum viable product); actual reservations and payments depend on integration with suitable third-party providers. 

## **2. Business Problem** 

Travellers often use multiple websites and apps to research destinations, compare options, organise daily plans, and track trip expenses. Information can become scattered, making trip preparation time-consuming and difficult to manage. 

## **3. Business Objectives** 

- Provide one convenient place to discover destinations and build trip plans. 

- Allow users to create, edit, and view day-by-day itineraries. 

- Help users estimate and track a trip budget. 

- Present useful destination information, including attractions and travel tips. 

- Provide clear links or integrations for accommodation and transport options. 

- Offer an accessible, mobile-friendly experience that reduces planning effort. 

## **4. Target Users / Stakeholders** 

- Guest visitor: explores destinations and public travel information. 

- Registered traveller: saves destinations, creates trips, manages itineraries, and tracks budgets. 

- Administrator: manages destination content, categories, reports, and inappropriate or outdated information. 

- External providers: map, weather, transport, accommodation, or payment services integrated where required. 

- Project team: product owner, designer, developer, and tester. 

## **5. Functional Requirements** 

|**ID / Feature**|**Requirement**|
|---|---|
|**FR-01: Registration and login**|Users can register, log in, log out, and securely manage<br>their profile. Guests may browse public content.|
|**FR-02: Destination discovery**|Users can browse and search destinations by name,<br>region, category, or interests.|
|**FR-03: Destination details**|The app displays available descriptions, images,<br>attractions, suggested activities, travel tips, and<br>estimated costs.|
|**FR-04: Trip creation**|Registered users can create a trip with a title,<br>destination, start date, end date, and number of<br>travellers.|
|**FR-05: Itinerary management**|Users can add, edit, reorder, and remove activities or<br>places by day.|
|**FR-06: Budget management**|Users can set a budget and record estimated or actual<br>expenses by category, such as transport, stay, food,<br>and activities.|
|**FR-07: Saved places**|Users can bookmark destinations and attractions for<br>later.|
|**FR-08: Maps and directions**|Where a map provider is available, users can view<br>locations and open directions.|
|**FR-09: Booking information**<br>**i**|The app can show or link to third-party transport and<br>accommodation options. In-app confirmation is only<br>included if provider APIs support it.|
|**FR-10: Notifications**|The app may send trip reminders or itinerary updates<br>when notification services are configured.|
|**FR-11: Admin content management**|i   i<br>Administrators can add, edit, publish, or remove<br>destination and attraction information.|
|**FR-12: Feedback and support**|Users can submit feedback or report incorrect<br>destination information.|



## **6. Non-Functional Requirements** 

- Usability: Common tasks should be understandable to first-time users, with clear navigation and helpful validation. 

- Responsive design: Core screens should work on mobile phones, tablets, and desktop browsers. 

- Performance: Main screens and searches should load promptly under normal network conditions. 

- Security: Passwords must not be stored in plain text; access to private trips and profile data must be controlled. 

- Privacy: Collect only necessary personal data and explain how it is used. 

- Reliability: Show clear errors when a third-party API is unavailable; do not present failed bookings as confirmed. 

- Maintainability: Keep destination data, trip logic, and external integrations organised so they can be updated independently. 

- Accessibility: Use readable contrast, labels, keyboard support, and meaningful alternative text where applicable. 

## **7. Business Rules** 

- A user must be authenticated to save a personal trip or modify their itinerary. 

- A trip end date must be the same as or later than its start date. 

- A budget and expense amount cannot be negative. 

- Only authorised administrators may publish or remove shared destination content. 

- A third-party booking is confirmed only when the provider returns a valid confirmation; a link-out is not a booking. 

- Prices, opening hours, weather, visa guidance, and availability may change and should display source or lastupdated information where possible. 

## **8. Project Scope** 

#### **In scope for the proposed MVP** 

- Account creation and login. 

- Destination listing, search, and detail pages. 

- Personal trip creation and day-by-day itinerary editing. 

- Basic budget and expense tracking. 

- Saved destinations and attractions. 

- Basic admin management of destination content. 

- Responsive user interface and basic error handling. 

#### **Potential later-phase features** 

- Live flight, train, bus, and hotel search through provider APIs. 

- In-app payments, refunds, and reservation management. 

- Collaborative trip planning with friends. 

- AI-generated itineraries and personalised recommendations. 

- Offline maps or downloadable itineraries. 

- Multi-language and multi-currency support. 

#### **Out of scope for the initial MVP** 

- Operating transport or accommodation services directly. 

- Guaranteeing third-party prices, schedules, availability, or entry requirements. 

- Providing emergency response or acting as an insurer. 

- Processing bookings or payments unless a provider integration is explicitly approved. 

## **9. Assumptions** 

- Users have access to a smartphone or web browser and an internet connection for online features. 

- Destination content can be entered by administrators or sourced from permitted APIs. 

- Third-party map, weather, and booking APIs may require keys, usage limits, or paid plans. 

- The initial release can use booking links if direct booking APIs are unavailable. 

- The project team will confirm the launch geography and supported currencies before implementation. 

## **10. Constraints and Dependencies** 

- Budget, team size, and delivery deadline have not yet been confirmed. 

- Features relying on external providers depend on their API access, pricing, terms, and uptime. 

- Personal data and payments must be handled according to applicable laws and provider requirements. 

- Accurate live information depends on the freshness and reliability of third-party data. 

## **11. High-Level User Flow** 

Open app → Browse/search destinations → View destination details → Register/log in → Create trip → Add dates and travellers → Build itinerary → Set budget → Save trip → Optionally open external booking links → Review trip plan 

## **12. Success Criteria** 

- A user can create an account and sign in successfully. 

- A user can find a destination using search or browsing. 

- A registered user can create, edit, and reopen a saved trip. 

- A user can add itinerary items and see them grouped by day. 

- A user can record expenses and view the remaining budget. 

- An administrator can update destination content. 

- Errors from unavailable external services are communicated clearly and do not create false booking confirmations. 

## **13. Risks and Mitigations** 

|**Risk**|**Mitigation**<br>l|
|---|---|
|**Outdated destination information**|Show update dates and provide an admin workflow to<br>review content.<br>i|
|**Third-party API limits or cost**|Confirm provider terms early; use a modular<br>integration and fallback links.<br>i|
|**Scope becoming too large**|Deliver the MVP first and treat live bookings/AI features<br>as later phases.|
|**Privacy or account security issues**|Use established authentication practices, access<br>controls, and minimal data collection.|
|**Unclear booking status**|Clearly distinguish information links, pending requests,<br>andprovider-confirmed bookings.|



## **14.Resources and Technologies Required** 

- Frontend: HTML, CSS, JavaScript, and React for the user interface. 

- Styling: Tailwind CSS or regular CSS for responsive page design. 

- Backend:Python,Fast API (Rest API). 

- Database: MySQL. 

- Maps: OpenStreetMap, or Google Maps API 

- Design: Figma for wireframes and UI planning 

- Version control: Git and GitHub. 

- Testing: Browser developer tools and manual functional testing. 

## **15. Acceptance and Approval** 

This BRD should be reviewed by all the members of the project before detailed software requirements, UI/UX design, database design, and implementation begin. 

