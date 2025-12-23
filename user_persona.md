## Persona 1 – Admin (System Owner)

**Name:** Aarav Mehta, 29, Bengaluru  
**Role:** CoWatch platform administrator and developer  
**Background:** Full-stack engineer managing the Django + React codebase, deployments, and real-time features (WebSockets for sync and chat).

- **Goals:**
	- Keep CoWatch stable, secure, and fast for concurrent watch rooms.
	- Monitor abuse (spam rooms, offensive names) and maintain a safe community.
	- Roll out new features like better sync, presence, and analytics without breaking existing rooms.

- **Frustrations:**
	- Bug reports about logout not updating UI or rooms not loading without refresh.
	- Handling edge cases where many users join a room and WebSocket performance degrades.

- **Key Needs in CoWatch:**
	- Admin dashboard to view users, rooms, and active sessions.
	- Logs/metrics for errors, failed sync events, and authentication issues.
	- Ability to disable/flag problematic rooms or users.

## Persona 2 – Regular User (Viewer / Room Owner)

**Name:** Priya Sharma, 24, Bengaluru  
**Role:** Authenticated CoWatch user (creates and owns rooms)  
**Background:** Final-year CS student who logs in, creates rooms with YouTube URLs, and shares links with friends.

- **Goals:**
	- Login quickly and see only “My Rooms” to manage watch parties.
	- Create a room with a YouTube link and share `/rooms/:id` to friends in under 30 seconds.
	- Enjoy fully synced playback (play/pause/seek) with real-time chat in the same room.

- **Frustrations:**
	- Other platforms desync after a few minutes or need screen-sharing that drains battery.
	- UI bugs like logout requiring refresh or room clicks failing occasionally.

- **Key Needs in CoWatch:**
	- Simple login/register flow, no subscription or payment.
	- “My Rooms” page showing only her rooms, with create / edit / delete controls.
	- Room detail page with embedded YouTube player, synced controls, and chat box.

## Persona 3 – You (Project Builder / Power User)

**Name:** Sujal, 22, Bengaluru  
**Role:** Creator and power user of CoWatch (developer + tester)  
**Background:** Aspiring full-stack and AI/ML engineer building CoWatch as a portfolio project using Django backend and React frontend with real-time features.

- **Goals:**
	- Implement clean auth-first flow: login/registration, token handling, protected routes, and logout that updates UI instantly.
	- Build robust room CRUD (owner-only) and a smooth watch-together experience with YouTube sync + chat.
	- Keep the codebase structured, bug-free, and ready to show in interviews and portfolios.

- **Frustrations:**
	- Legacy bugs like logout state not updating until refresh and room click issues after earlier iterations.
	- Long chats getting messy, making it hard to keep track of context while iterating features.

- **Key Needs in CoWatch (as builder):**
	- Clear separation of backend (Django/DRF/Channels) and frontend (React) with small, testable features.
	- Real-time behavior that is easy to debug: clear WebSocket events for playback and chat, predictable room permissions.
	- A UI that looks clean (purple/white branding) but is simple enough to implement quickly.
