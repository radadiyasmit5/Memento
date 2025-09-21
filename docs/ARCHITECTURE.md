# Memento – Architecture Document

## 1. Overview
Memento is a cross-platform mobile app that automatically shares photos among friends based on face recognition. The MVP will focus on:
- Event creation & joining
- Photo uploads
- Face detection & matching
- Delivering photos to identified users

---

## 2. System Components
- **Mobile App (React Native / Expo)**
  - Create/join events
  - Capture/upload photos
  - Display "My Photos" & "Group Photos"
  - On-device face detection (ML Kit / Apple Vision)

- **Backend (Firebase)**
  - **Auth**: Google/Apple login
  - **Firestore**: Event & user metadata
  - **Storage**: Photo uploads
  - **Cloud Functions**: Orchestration, face matching logic
  - **FCM**: Notifications for new photos

- **ML (On-device first)**
  - Face detection → ML Kit (Android/iOS)
  - Embedding generation → MobileFaceNet (lightweight)
  - Matching → vector similarity search (local or in Firestore)

---

## 3. Data Models (MVP)
### User
- `userId`
- `name`
- `profileEmbeddings[]`
- `consentFlags`

### EventRoom
- `roomId`
- `hostId`
- `createdAt`
- `members[]`

### Photo
- `photoId`
- `uploaderId`
- `roomId`
- `storagePath`
- `faces[]`

### Face
- `faceId`
- `photoId`
- `boundingBox`
- `embedding`
- `matchedUserId?`

---

## 4. Flows
### Event Creation
1. Host creates room → QR code generated
2. Friends scan QR → join with profile

### Photo Upload
1. User uploads photo
2. On-device face detection → embeddings generated
3. Compare against room members
4. Share photo with matched users

---

## 5. Tech Stack
- **Frontend**: React Native (Expo)
- **Backend**: Firebase (Auth, Firestore, Storage, Functions)
- **ML**: ML Kit / CoreML + lightweight embedding model
- **CI/CD**: GitHub Actions (build + test + deploy)
