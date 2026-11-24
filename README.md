# Smart India Hackathon Workshop
# Date: 24/11/2026
## Reference Number: 26017964
## Name: Shuban S

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers' earnings and increase consumer prices.

## Problem Creator's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Expected Solution: Create a digital marketplace that:

• Connects farmers/FPOs directly with consumers and bulk buyers.
• Provides logistics support.
• Uses AI for demand forecasting and route optimization.

Benefits:

• Better prices for farmers.
• Lower prices for consumers.
• Reduced supply chain inefficiencies.

## Proposed Solution
**KisanSetu – "A Bridge from Farm to Fork"**

KisanSetu is a voice-first, multilingual digital marketplace that removes middlemen and gives farmers a larger share of the final price.

1. **Detailed explanation**
   - Farmers and FPOs list produce (crop, quantity, harvest date, photo) through an app, WhatsApp bot, or IVR call, with no typing needed.
   - Consumers, restaurants, retailers, and bulk buyers browse, place orders, or pre-book upcoming harvests.
   - Local collection hubs aggregate small lots, grade the quality, and dispatch orders through pooled logistics.
   - Payments are held in UPI-based escrow and released to the farmer once delivery is confirmed.

2. **How it addresses the problem**
   - Direct farmer-to-buyer trade removes 3–4 layers of intermediaries (mandi agents, wholesalers, and retailers).
   - AI demand forecasting tells farmers what to grow and when to sell, which reduces distress sales and wastage.
   - Route optimization and shared transport cut logistics cost, so savings reach both farmers and consumers.

3. **Innovation and uniqueness**
   - **Fair Price Meter:** every order shows a transparent breakdown (farmer share, logistics, platform fee) so buyers see where their money goes.
   - **Pre-Harvest Booking:** buyers commit to crops before harvest, giving farmers guaranteed demand and price.
   - **Spoilage-Aware Dynamic Pricing:** perishable produce nearing its shelf-life limit is auto-discounted and routed to the nearest buyers.
   - **Community Group Buying:** neighbourhoods and apartments pool orders to unlock bulk prices and one shared delivery.
   - **QR Farm Traceability:** each batch carries a QR code showing the farmer, farm location, and harvest date.
   - **Low-Literacy Access:** regional-language voice interface and offline-first design for poor connectivity.

## Technical Approach
1. **Technologies to be used**
   - **Frontend:** React Native (mobile app), React.js (web dashboard)
   - **Backend:** Node.js with Express, REST APIs
   - **Database:** PostgreSQL (orders, users) and MongoDB (listings, logs)
   - **AI/ML:** Python, scikit-learn / Prophet (demand and price forecasting), Google OR-Tools (route optimization), a CNN model for produce quality grading from photos
   - **Voice/Language:** Speech-to-text and text-to-speech APIs, Bhashini for Indian languages
   - **Messaging:** WhatsApp Business API, Twilio IVR
   - **Payments:** UPI / Razorpay escrow
   - **Maps and Logistics:** OpenStreetMap / Google Maps API
   - **Hosting:** AWS / Azure with Docker

2. **Methodology and process for implementation** **(Flow Charts/Images/ working prototype)**
   1. **Onboarding:** farmer/FPO registers using Aadhaar-linked or mobile OTP verification.
   2. **Listing:** the farmer uploads produce details by voice or photo, and the AI grades quality.
   3. **Matching:** the platform matches supply to buyer demand by location and price.
   4. **Order and payment:** the buyer orders and pays into escrow.
   5. **Logistics:** the optimizer groups orders and assigns pooled vehicles through the nearest hub.
   6. **Delivery and settlement:** delivery is confirmed by QR scan and funds are released to the farmer.
   7. **Feedback loop:** ratings and sales data feed back into the forecasting models.

   ```
   Farmer/FPO → Listing (Voice/App) → AI Grading → Marketplace
        → Buyer Order → Escrow Payment → Hub + Route Optimization
        → Delivery (QR Verified) → Farmer Payout → Data → AI Forecasting
   ```

## Feasibility and Viability
1. **Analysis of the feasibility of the idea**
   - Smartphone and UPI penetration in rural India is high enough to support the app, and WhatsApp/IVR covers basic-phone users.
   - Existing FPOs, e-NAM, and government hubs can serve as ready-made aggregation points.
   - All proposed technologies are mature and available as open-source or affordable APIs.

2. **Potential challenges and risks**
   - Low digital literacy among some farmers.
   - Poor internet connectivity in remote areas.
   - Last-mile logistics and cold-chain gaps for perishables.
   - Trust and adoption resistance from existing trade networks.
   - Quality consistency and buyer disputes.

3. **Strategies for overcoming these challenges**
   - Voice-first, regional-language interface with an offline mode and SMS fallback.
   - Training through local FPO leaders and "Kisan Mitra" village agents.
   - Pooled logistics and partnerships with local transporters and cold-storage hubs.
   - Escrow payments, ratings, and AI quality grading to build trust.
   - Pilot in one district first, then scale state by state.

## Impact and Benefits
1. **Potential impact on the target audience**
   - **Farmers/FPOs:** an estimated 20–30% higher income, with assured demand and faster payments.
   - **Consumers:** fresher produce at lower prices with full price transparency.
   - **Bulk buyers:** reliable supply and traceable sourcing.

2. **Benefits of the solution (social, economic, environmental, etc.)**
   - **Social:** empowers small and marginal farmers, with inclusion through local-language and voice access.
   - **Economic:** reduces middleman margins, creates rural jobs (hub operators, delivery partners), and stabilizes prices.
   - **Environmental:** less food wastage, optimized routes mean lower fuel use and emissions, and pre-harvest booking reduces overproduction.

## Research and References
1. Details / Links of the reference and research work
   - Smart India Hackathon – https://www.sih.gov.in
   - e-NAM (National Agriculture Market) – https://enam.gov.in
   - Agmarknet (mandi price data) – https://agmarknet.gov.in
   - Bhashini (Indian language AI) – https://bhashini.gov.in
   - Google OR-Tools (route optimization) – https://developers.google.com/optimization
   - Ministry of Agriculture & Farmers Welfare, FPO scheme – https://www.agricoop.nic.in
