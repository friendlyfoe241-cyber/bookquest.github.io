

# 📚 BookQuest - Interactive Reading App for Kids

## Phase 1: Core Experience ✅

### 1. Welcome & Onboarding Screen ✅
### 2. Book Swipe Discovery ✅
### 3. For You Page (FYP) ✅
### 4. Book Reading Experience ✅
### 5. Post-Reading Quiz ✅
### 6. Settings (3-dot menu) ✅
### 7. User Levels & Progression ✅

## Phase 1.5: Content & Features ✅

### 8. Action Books (2 long-form ~20 pages) ✅
- "Race Against the Storm" - boy saves farm animals from storm (20 pages, 3 QTEs)
- "The Volcano Escape" - twins escape erupting volcano (20 pages, 3 QTEs)

### 9. Quick-Time Events (QTE) System ✅
- 3 QTE types: tap, swipe, mash (rapid tapping)
- Timer-based with visual feedback
- Success/fail results with encouraging messages
- QTEs embedded at climax pages in action books

### 10. Book Cover Images ✅
- Generated cover illustrations for all 11 books
- Covers used in Discovery cards, ForYou grid, Library list, Reader

### 11. Library Page with Search & Filters ✅
- Fuzzy search (doesn't require exact wording)
- Genre filter (Adventure, Fantasy, Animals, Action)
- Difficulty filter (Beginner, Intermediate)
- Shows page count, QTE badge, read status, quiz scores

## Phase 2: Cloud Backend 🔧 (In Progress)

### 12. Lovable Cloud Database ✅
- Books table (central catalog with JSONB pages/quiz)
- Profiles table (auto-created on signup)
- User_books table (tracks likes, reads, ratings, scores)
- Discovery_feed table (personalized daily feed)

### 13. Authentication ✅
- Email/password signup & login
- Auto-profile creation via trigger
- Guest mode still available (localStorage fallback)

### 14. Cloud-Synced Progress 🔜
- Wire up reading progress to user_books table
- Sync quiz scores, ratings, QTE scores
- Fallback to localStorage for guest users

### 15. Discovery Feed Engine 🔜
- Daily refresh of 5 books from cloud catalog
- 70% preferred genres / 30% discovery balance
- Personalized based on user interaction history

## Phase 3: Offline & Special Modes 🔜

### 16. Offline Mode
- Cache book content (pages + illustrations) for offline reading
- Service worker for PWA-style offline support
- Sync progress when back online
- Visual indicator for offline/online status
- Download books for offline reading (user-initiated)

### 17. Car Reading Mode 🚗
- Audio/TTS-focused interface for listening to stories
- Large, simple controls (play/pause/next)
- Auto-advancing pages with narration timing
- Reduced visual UI — focus on audio
- Night-safe dark theme variant
- Kid-friendly voice selection
- Speed control for narration

## Phase 4: Future Additions
- **Friend system**: Add friends, challenge them
- **More interactive games**: Mazes, puzzles at story points
- **Leaderboard**: Compare quiz scores globally
- **Profile pictures**: Unlockable avatars that progress with levels
- **More books**: Expand catalog with new genres and longer stories

## Design Approach
- **Kid-friendly UI** for ages 6-12 with large touch targets
- Light/dark mode with user-chosen accent color
- Playful animations on all transitions
- All data stored in Cloud with localStorage fallback
