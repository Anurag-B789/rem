<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Learning Platform</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/tailwindcss/2.2.19/tailwind.min.css" rel="stylesheet">
    <style>
        .course-card {
            transition: transform 0.2s;
        }
        .course-card:hover {
            transform: translateY(-5px);
        }
        .progress-bar {
            height: 10px;
            background-color: #e5e7eb;
            border-radius: 5px;
            overflow: hidden;
        }
        .progress-bar-fill {
            height: 100%;
            background-color: #3b82f6;
            transition: width 0.3s ease;
        }
        .lesson-complete {
            color: #10b981;
        }
    </style>
</head>
<body class="bg-gray-50">
    <nav class="bg-white shadow-lg">
        <div class="max-w-6xl mx-auto px-4">
            <div class="flex justify-between items-center py-4">
                <div class="text-xl font-bold">EdTech Platform</div>
                <div id="userSection">
                    <button id="loginBtn" class="bg-blue-500 text-white px-4 py-2 rounded-lg">Login</button>
                    <div id="userProfile" class="hidden">
                        <span id="userName"></span>
                        <button id="logoutBtn" class="bg-red-500 text-white px-4 py-2 rounded-lg ml-4">Logout</button>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <main class="max-w-6xl mx-auto px-4 py-8">
        <div id="courseGrid" class="grid grid-cols-1 md:grid-cols-3 gap-6">
            <!-- Course cards will be dynamically inserted here -->
        </div>

        <div id="courseContent" class="mt-8">
            <!-- Course content will be dynamically inserted here -->
        </div>
    </main>

    <!-- Login Modal -->
    <div id="loginModal" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center">
        <div class="bg-white p-8 rounded-lg w-96">
            <h2 class="text-2xl font-bold mb-4">Login</h2>
            <input type="email" id="emailInput" placeholder="Email" class="w-full p-2 mb-4 border rounded">
            <input type="password" id="passwordInput" placeholder="Password" class="w-full p-2 mb-4 border rounded">
            <button id="loginSubmitBtn" class="w-full bg-blue-500 text-white py-2 rounded">Login</button>
        </div>
    </div>

    <script>
        // Course data
        const courses = {
            python: {
                title: 'Python Programming',
                progress: 0,
                modules: [
                    {
                        title: 'Basics of Python',
                        lessons: [
                            {
                                title: 'Introduction to Python',
                                type: 'video',
                                link: 'https://youtube.com/your-channel/video1',
                                completed: false
                            },
                            {
                                title: 'Variables and Data Types',
                                type: 'video',
                                link: 'https://youtube.com/your-channel/video2',
                                completed: false
                            }
                        ]
                    },
                    {
                        title: 'Advanced Concepts',
                        lessons: [
                            {
                                title: 'Functions and OOP',
                                type: 'video',
                                link: 'https://youtube.com/your-channel/video3',
                                completed: false
                            }
                        ]
                    }
                ]
            },
            c: {
                title: 'C Programming',
                progress: 0,
                modules: [
                    {
                        title: 'C Fundamentals',
                        lessons: [
                            {
                                title: 'Introduction to C',
                                type: 'video',
                                link: 'https://youtube.com/your-channel/video4',
                                completed: false
                            }
                        ]
                    }
                ]
            }
        };

        // User state
        let currentUser = null;

        // Initialize the page
        function initializePage() {
            renderCourseGrid();
            setupEventListeners();
            checkLocalStorage();
        }

        // Render course grid
        function renderCourseGrid() {
            const courseGrid = document.getElementById('courseGrid');
            courseGrid.innerHTML = '';

            Object.entries(courses).forEach(([courseId, course]) => {
                const card = document.createElement('div');
                card.className = 'course-card bg-white p-6 rounded-lg shadow-md';
                card.innerHTML = `
                    <h2 class="text-xl font-bold mb-4">${course.title}</h2>
                    <div class="progress-bar">
                        <div class="progress-bar-fill" style="width: ${course.progress}%"></div>
                    </div>
                    <p class="mt-2 text-gray-600">${course.progress}% Complete</p>
                    <button 
                        class="mt-4 bg-blue-500 text-white px-4 py-2 rounded-lg"
                        onclick="showCourseContent('${courseId}')"
                    >
                        Continue Learning
                    </button>
                `;
                courseGrid.appendChild(card);
            });
        }

        // Show course content
        function showCourseContent(courseId) {
            const course = courses[courseId];
            const contentDiv = document.getElementById('courseContent');
            
            let html = `
                <h2 class="text-2xl font-bold mb-6">${course.title}</h2>
            `;

            course.modules.forEach((module, moduleIndex) => {
                html += `
                    <div class="bg-white p-6 rounded-lg shadow-md mb-6">
                        <h3 class="text-xl font-bold mb-4">${module.title}</h3>
                        <div class="space-y-4">
                `;

                module.lessons.forEach((lesson, lessonIndex) => {
                    html += `
                        <div class="flex items-center justify-between p-2 hover:bg-gray-50 rounded">
                            <div class="flex items-center">
                                <input 
                                    type="checkbox" 
                                    ${lesson.completed ? 'checked' : ''} 
                                    onchange="toggleLesson('${courseId}', ${moduleIndex}, ${lessonIndex})"
                                    class="mr-3"
                                >
                                <span class="${lesson.completed ? 'lesson-complete' : ''}">${lesson.title}</span>
                            </div>
                            <a 
                                href="${lesson.link}" 
                                target="_blank" 
                                class="text-blue-500 hover:text-blue-700"
                            >
                                Watch Video
                            </a>
                        </div>
                    `;
                });

                html += `
                        </div>
                    </div>
                `;
            });

            contentDiv.innerHTML = html;
        }

        // Toggle lesson completion
        function toggleLesson(courseId, moduleIndex, lessonIndex) {
            if (!currentUser) {
                alert('Please login to track your progress');
                return;
            }

            const course = courses[courseId];
            const lesson = course.modules[moduleIndex].lessons[lessonIndex];
            lesson.completed = !lesson.completed;

            // Update progress
            const totalLessons = course.modules.reduce((total, module) => total + module.lessons.length, 0);
            const completedLessons = course.modules.reduce((total, module) => {
                return total + module.lessons.filter(lesson => lesson.completed).length;
            }, 0);

            course.progress = Math.round((completedLessons / totalLessons) * 100);

            // Save to localStorage
            saveProgress();
            renderCourseGrid();
            showCourseContent(courseId);
        }

        // Setup event listeners
        function setupEventListeners() {
            const loginBtn = document.getElementById('loginBtn');
            const loginModal = document.getElementById('loginModal');
            const loginSubmitBtn = document.getElementById('loginSubmitBtn');
            const logoutBtn = document.getElementById('logoutBtn');

            loginBtn.addEventListener('click', () => {
                loginModal.classList.remove('hidden');
            });

            loginSubmitBtn.addEventListener('click', () => {
                const email = document.getElementById('emailInput').value;
                const password = document.getElementById('passwordInput').value;
                
                // Simple login (replace with proper authentication)
                currentUser = { email };
                localStorage.setItem('user', JSON.stringify(currentUser));
                
                loginModal.classList.add('hidden');
                updateUIForUser();
            });

            logoutBtn.addEventListener('click', () => {
                currentUser = null;
                localStorage.removeItem('user');
                updateUIForUser();
            });
        }

        // Check localStorage for user and progress
        function checkLocalStorage() {
            const savedUser = localStorage.getItem('user');
            if (savedUser) {
                currentUser = JSON.parse(savedUser);
                updateUIForUser();
            }

            const savedProgress = localStorage.getItem('courseProgress');
            if (savedProgress) {
                const progress = JSON.parse(savedProgress);
                Object.keys(progress).forEach(courseId => {
                    if (courses[courseId]) {
                        courses[courseId].progress = progress[courseId].progress;
                        courses[courseId].modules = progress[courseId].modules;
                    }
                });
                renderCourseGrid();
            }
        }

        // Update UI based on user state
        function updateUIForUser() {
            const loginBtn = document.getElementById('loginBtn');
            const userProfile = document.getElementById('userProfile');
            const userName = document.getElementById('userName');

            if (currentUser) {
                loginBtn.classList.add('hidden');
                userProfile.classList.remove('hidden');
                userName.textContent = currentUser.email;
            } else {
                loginBtn.classList.remove('hidden');
                userProfile.classList.add('hidden');
            }
        }

        // Save progress to localStorage
        function saveProgress() {
            if (currentUser) {
                localStorage.setItem('courseProgress', JSON.stringify(courses));
            }
        }

        // Initialize the page when loaded
        document.addEventListener('DOMContentLoaded', initializePage);
    </script>
</body>
</html>