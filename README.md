# CampusVibe
Social Media Site.
Root of the Project
│
├── 📁 backend/                           # Flask or FastAPI Backend
│   ├── 📁 app/
│   │   ├── 📁 __init__.py
│   │   ├── 📁 config/                    # Environment configs
│   │   │   ├── development.py
│   │   │   ├── production.py
│   │   │   └── testing.py
│   │   ├── 📁 api/                        # API Versioning
│   │   │   ├── v1/
│   │   │   │   ├── __init__.py
│   │   │   │   ├── auth.py               # Authentication APIs
│   │   │   │   ├── users.py              # User Profile APIs
│   │   │   │   ├── campuses.py           # Campus Page APIs
│   │   │   │   ├── posts.py              # Post Text/Photos/Videos
│   │   │   │   ├── comments.py           # Commenting on posts
│   │   │   │   ├── likes.py              # Likes/Reactions
│   │   │   │   ├── media.py              # Uploading photos/videos
│   │   │   │   ├── chat.py               # Real-time messaging
│   │   │   │   ├── groups.py             # Student groups
│   │   │   │   ├── events.py             # Campus/student events
│   │   │   │   ├── marketplace.py        # Marketplace module (optional)
│   │   │   │   ├── notifications.py      # Notifications
│   │   │   │   └── admin.py              # Admin-specific APIs
│   │   ├── 📁 models/
│   │   │   ├── user.py
│   │   │   ├── campus.py
│   │   │   ├── post.py
│   │   │   ├── comment.py
│   │   │   ├── like.py
│   │   │   ├── media.py
│   │   │   ├── chat_message.py
│   │   │   ├── group.py
│   │   │   ├── event.py
│   │   │   ├── marketplace_item.py
│   │   │   └── notification.py
│   │   ├── 📁 services/                  # Business Logic
│   │   │   ├── auth_service.py
│   │   │   ├── post_service.py
│   │   │   ├── media_service.py
│   │   │   ├── chat_service.py
│   │   │   ├── campus_service.py
│   │   │   ├── notification_service.py
│   │   │   └── event_service.py
│   │   ├── 📁 workers/                   # Async Tasks (Celery/RQ)
│   │   │   ├── send_email.py
│   │   │   ├── video_processor.py        # Compress videos
│   │   │   └── notification_dispatcher.py
│   │   ├── 📁 utils/                      # Utilities
│   │   │   ├── jwt_utils.py
│   │   │   ├── image_optimizer.py
│   │   │   ├── video_optimizer.py
│   │   │   ├── file_storage.py
│   │   │   └── pagination.py
│   │   ├── 📁 middleware/
│   │   │   ├── auth_middleware.py
│   │   │   ├── error_handler.py
│   │   │   └── cors_middleware.py
│   │   └── extensions.py                 # db, cache, login manager etc.
│   ├── 📁 migrations/
│   ├── 📁 tests/
│   │   ├── unit/
│   │   ├── integration/
│   │   └── e2e/
│   ├── requirements.txt
│   ├── run.py
│   └── wsgi.py
│
├── 📁 frontend/                          # Frontend (React or Next.js)
│   ├── 📁 public/
│   ├── 📁 src/
│   │   ├── 📁 assets/
│   │   │   ├── images/
│   │   │   ├── fonts/
│   │   │   └── icons/
│   │   ├── 📁 components/
│   │   │   ├── Navbar/
│   │   │   │   ├── Navbar.jsx
│   │   │   │   └── Navbar.css
│   │   │   ├── Sidebar/
│   │   │   │   ├── Sidebar.jsx
│   │   │   │   └── Sidebar.css
│   │   │   ├── Post/
│   │   │   │   ├── PostCard.jsx
│   │   │   │   └── PostCard.css
│   │   │   ├── Comment/
│   │   │   │   ├── CommentBox.jsx
│   │   │   │   └── CommentBox.css
│   │   │   ├── Chat/
│   │   │   │   ├── ChatWindow.jsx
│   │   │   │   └── ChatWindow.css
│   │   │   ├── Event/
│   │   │   │   ├── EventCard.jsx
│   │   │   │   └── EventCard.css
│   │   │   ├── Campus/
│   │   │   │   ├── CampusPage.jsx
│   │   │   │   └── CampusPage.css
│   │   │   ├── Group/
│   │   │   │   ├── GroupPage.jsx
│   │   │   │   └── GroupPage.css
│   │   │   ├── Marketplace/
│   │   │   │   ├── MarketplaceItem.jsx
│   │   │   │   └── MarketplaceItem.css
│   │   │   └── Profile/
│   │   │       ├── ProfilePage.jsx
│   │   │       └── ProfilePage.css
│   │   ├── 📁 pages/
│   │   │   ├── 📁 Home/
│   │   │   │   ├── Home.jsx
│   │   │   │   └── Home.css
│   │   │   ├── 📁 Explore/
│   │   │   │   ├── Explore.jsx
│   │   │   │   └── Explore.css
│   │   │   ├── 📁 Notifications/
│   │   │   │   ├── Notifications.jsx
│   │   │   │   └── Notifications.css
│   │   │   ├── 📁 Messenger/
│   │   │   │   ├── Messenger.jsx
│   │   │   │   └── Messenger.css
│   │   │   ├── 📁 Campus/
│   │   │   │   ├── Campus.jsx
│   │   │   │   └── Campus.css
│   │   │   ├── 📁 Group/
│   │   │   │   ├── Group.jsx
│   │   │   │   └── Group.css
│   │   │   ├── 📁 Marketplace/
│   │   │   │   ├── Marketplace.jsx
│   │   │   │   └── Marketplace.css
│   │   │   └── 📁 Profile/
│   │   │       ├── Profile.jsx
│   │   │       └── Profile.css
│   │   ├── 📁 services/                  # API Communication
│   │   │   ├── authService.js
│   │   │   ├── postService.js
│   │   │   ├── mediaService.js
│   │   │   ├── chatService.js
│   │   │   ├── campusService.js
│   │   │   ├── groupService.js
│   │   │   ├── eventService.js
│   │   │   ├── notificationService.js
│   │   │   └── marketplaceService.js
│   │   ├── 📁 store/                     # Redux / Zustand
│   │   │   ├── authSlice.js
│   │   │   ├── postSlice.js
│   │   │   ├── mediaSlice.js
│   │   │   ├── chatSlice.js
│   │   │   ├── campusSlice.js
│   │   │   └── notificationSlice.js
│   │   ├── 📁 hooks/
│   │   │   ├── useAuth.js
│   │   │   ├── useChat.js
│   │   │   └── useCampus.js
│   │   └── App.jsx
│   ├── .env
│   ├── package.json
│   └── vite.config.js
│
├── 📁 devops/                             # Deployment
│   ├── 📁 nginx/
│   │   └── default.conf
│   ├── Dockerfile
│   ├── docker-compose.yml
│   └── supervisord.conf
│
├── 📁 payments/                           # (If you allow donations, buying items)
│   ├── stripe/
│   ├── paypal/
│   └── interfaces.py
│
├── 📁 scripts/
│   ├── seed.py
│   ├── generate_fake_data.py
│   ├── backup_db.py
│   └── clear_cache.py
│
├── 📁 docs/                               
│   ├── architecture.md
│   ├── db_schema.png
│   ├── api_contracts.md
│   ├── deployment.md
│   ├── scalability_plan.md
│   ├── security_best_practices.md
│   └── roadmap.md
│
├── .env
├── README.md
├── .gitignore
└── LICENSE
