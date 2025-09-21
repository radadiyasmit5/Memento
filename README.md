# Memento (Working Title) – Product Requirements Document (PRD)

## 1. Problem Statement
When friends go out together, photos are usually taken on one or two people’s phones. Sharing them afterward is inconvenient and messy (group chats, manual uploads, poor quality). There’s no seamless, automatic way to ensure everyone gets the photos they appear in.

## 2. Target Users
- Friends at social gatherings (parties, dinners, trips).
- Small groups (3–15 people) who want an easy way to share event photos.
- Tech-savvy early adopters who are open to new apps.

## 3. Value Proposition
Memento automatically identifies who is in each photo and delivers those photos directly to them — saving time, reducing friction, and keeping memories organized.

## 4. User Stories
- As a user, I want to **create an event room** so that my friends can join easily.  
- As a user, I want to **join a room via QR code or link** so I can start receiving photos.  
- As a user, I want to **upload my photos from the event** so others can get their pictures.  
- As a user, I want to **provide reference photos/selfies** so the system can recognize me.  
- As a user, I want the app to **show me only the photos I am in**, so I don’t have to sort through irrelevant ones.  
- As a user, I want the option to **approve photos before they are shared** with me, to protect my privacy.  

## 5. Functional Requirements
- Event room creation and joining (QR code / link).  
- User profiles with reference selfies for recognition.  
- Photo upload to event room.  
- Face detection and matching against room members.  
- Delivery of photos to the correct users.  
- Privacy controls (auto-share vs approve).  

## 6. Non-Functional Requirements
- **Privacy-first:** Face data should stay on-device where possible.  
- **Cross-platform:** App must work on both Android and iOS.  
- **Scalability:** Support groups of up to 20 people in MVP, more later.  
- **Usability:** Simple onboarding; minimal taps to share photos.  
- **Performance:** Face recognition within 2–3 seconds per photo.  

## 7. MVP Scope
The MVP will include:
- Create/join event rooms.  
- Upload photos to an event.  
- On-device face detection and basic matching (5–10 enrolled friends).  
- Display “My Photos” tab (only photos user appears in).  
- Manual approval flow for shared photos.  

## 8. Out of Scope (Future Enhancements)
- Automatic background photo syncing.  
- Peer-to-peer live sharing without cloud.  
- Event highlight reels / AI summaries.  
- Large event scaling (50+ people).  
- Monetization model.  

## 9. Success Metrics
- D1 retention (do users come back next day to view photos?).  
- % of photos correctly matched to at least one friend.  
- Average # of photos shared per event.  
- User feedback rating (1–5 stars).  

---
