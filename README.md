# Omidha
<!DOCTYPE html>
<html lang="fafa" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>هوشمند سازی صنعت امید</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Vazirmatn:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Clean Innovation -->
    <!-- Application Structure Plan: The application is structured as a single-page scrolling narrative to guide users through the company's story. It starts with a high-impact Hero section (Identity), followed by an interactive showcase of their Core Solutions (Technology), a dedicated section for the source Script/Narration, a visual representation of their Process (Timeline), and concludes with a clear Contact section. This structure was chosen to transform the passive video brief into an active, exploratory user journey, allowing users to delve into the company's services at their own pace while maintaining a logical flow from brand identity to call-to-action. -->
    <!-- Visualization & Content Choices: Report Info: Company Branding -> Goal: Inform -> Viz: Hero section with a dynamic canvas background simulating circuits -> Interaction: None -> Justification: Creates a memorable, futuristic first impression. | Report Info: Solution Montage -> Goal: Explore -> Viz: Interactive cards for each technology (Robotics, PCB, Smart Panels) -> Interaction: Click to reveal detailed descriptions -> Justification: Converts a fast-paced video clip into a user-controlled information discovery tool. | Report Info: Script Text -> Goal: Inform -> Viz: Structured text blocks with time segmentation -> Interaction: None -> Justification: Provides the source material and context for the entire video plan. | Report Info: Implied Professionalism -> Goal: Organize -> Viz: A simple, elegant HTML/CSS timeline diagram -> Interaction: Hover to highlight stages -> Justification: Adds value by structuring the company's workflow, enhancing their professional image. | Report Info: Contact Details -> Goal: Inform -> Viz: Cleanly formatted list -> Interaction: None -> Justification: Provides a clear and accessible call to action. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Vazirmatn', sans-serif;
            background-color: #f8f9fa;
            color: #212529;
        }
        .neon-green {
            color: #00ff85;
            text-shadow: 0 0 5px #00ff85, 0 0 10px #00ff85, 0 0 15px #00ff85;
        }
        .bg-deep-blue {
            background-color: #0a192f;
        }
        .card-content {
            max-height: 0;
            overflow: hidden;
            transition: max-heimax-heightght 0.7s ease-in-out;
        }
        .card.active .card-content {
            max-height: 500px;
        }
        .timeline-item:hover .timeline-dot {
            background-color: #00ff85;
            transform: scale(1.2);
        }
        .timeline-item:hover .timeline-content h3 {
            color: #0a192f;
        }
        .hero-canvas {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
        }
        .script-segment {
            transition: all 0.3s ease;
        }
        .script-segment:hover {
            background-color: rgba(255, 255, 255, 0.1);
        }
    </style>
</head>
<body class="antialiased">

    <div class="relative overflow-hidden">
        <header class="bg-deep-blue text-white relative">
            <canvas id="heroCanvas" class="hero-canvas"></canvas>
            <div class="container mx-auto px-6 py-24 md:py-32 text-center relative z-10">
                <div class="flex justify-center mb-6">
                    <img src="https://iili.io/KkY9L3G.jpg" alt="لوگو هوشمند سازی صنعت امید" class="h-24 w-24 rounded-full border-4 border-[#00ff85]">
                </div>
                <h1 class="text-4xl md:text-6xl font-bold">هوشمند سازی صنعت امید</h1>
                <p class="mt-4 text-lg md:text-2xl font-light text-gray-300">«ما می‌سازیم تا شما راحت زندگی کنید.»</p>
            </div>
        </header>

        <main>
            <section id="solutions" class="py-16 md:py-24 bg-white">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-12">
                        <h2 class="text-3xl md:text-4xl font-bold text-gray-800">راهکارهای نوآورانه ما</h2>
                        <p class="mt-4 text-lg text-gray-600 max-w-3xl mx-auto">ما با ترکیب فناوری‌های پیشرفته و طراحی هوشمندانه، راهکارهایی ارائه می‌دهیم که کیفیت زندگی و کارایی صنعت را متحول می‌کنند. برای آشنایی بیشتر با هر بخش، روی آن کلیک کنید.</p>
                    </div>
                    <div class="grid md:grid-cols-3 gap-8">
                        <div class="card bg-gray-50 rounded-lg shadow-lg overflow-hidden cursor-pointer transition-transform transform hover:scale-105" onclick="toggleCard(this)">
                            <div class="p-6 flex items-center space-x-4 space-x-reverse">
                                <div class="text-4xl">🦾</div>
                                <h3 class="text-xl font-semibold text-gray-800">بازوهای رباتیک دقیق</h3>
                                <div class="ml-auto text-2xl transition-transform transform">+</div>
                            </div>
                            <div class="card-content px-6 pb-6">
                                <p class="text-gray-700">اتوماسیون صنعتی با استفاده از بازوهای رباتیک پیشرفته که دقت، سرعت و تکرارپذیری بی‌نظیری را در فرآیندهای تولیدی به ارمغان می‌آورند. مناسب برای خطوط مونتاژ، بسته‌بندی و کنترل کیفیت.</p>
                            </div>
                        </div>
                        <div class="card bg-gray-50 rounded-lg shadow-lg overflow-hidden cursor-pointer transition-transform transform hover:scale-105" onclick="toggleCard(this)">
                            <div class="p-6 flex items-center space-x-4 space-x-reverse">
                                <div class="text-4xl">💡</div>
                                <h3 class="text-xl font-semibold text-gray-800">مدارهای الکترونیکی هوشمند</h3>
                                <div class="ml-auto text-2xl transition-transform transform">+</div>
                            </div>
                            <div class="card-content px-6 pb-6">
                                <p class="text-gray-700">طراحی و تولید بردهای مدار چاپی (PCB) سفارشی که مغز متفکر دستگاه‌های هوشمند شما هستند. ما با بهینه‌سازی عملکرد و کاهش مصرف انرژی، محصولاتی پایدار و قدرتمند خلق می‌کنیم.</p>
                            </div>
                        </div>
                        <div class="card bg-gray-50 rounded-lg shadow-lg overflow-hidden cursor-pointer transition-transform transform hover:scale-105" onclick="toggleCard(this)">
                            <div class="p-6 flex items-center space-x-4 space-x-reverse">
                                <div class="text-4xl">📲</div>
                                <h3 class="text-xl font-semibold text-gray-800">پنل‌های کنترل یکپارچه</h3>
                                <div class="ml-auto text-2xl transition-transform transform">+</div>
                            </div>
                            <div class="card-content px-6 pb-6">
                                <p class="text-gray-700">کنترل کامل خانه یا محیط کار خود را با پنل‌های لمسی مدرن و اپلیکیشن‌های کاربرپسند در دست بگیرید. مدیریت روشنایی، دما، امنیت و سایر تجهیزات هوشمند هرگز به این سادگی نبوده است.</p>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Script Section -->
            <section id="script" class="py-16 md:py-24 bg-deep-blue text-white">
                <div class="container mx-auto px-6">
                    <div class="text-center mb-12">
                        <p class="mt-4 text-lg text-gray-300 max-w-3xl mx-auto"></p>
                    </div>
                    
                    <div class="max-w-4xl mx-auto space-y-6">
                        <!-- Scene 1 -->
                        <div class="script-segment p-5 rounded-lg border border-gray-700 bg-gray-800">
                            <h3 class="text-xl font-semibold text-[#00ff85] mb-2"> </h3>
                            <p class="text-gray-300 mb-2"><strong>:</strong>

                        <!-- Scene 2 -->
                        <div class="script-segment p-5 rounded-lg border border-gray-700 bg-gray-800">
                            <h3 class="text-xl font-semibold text-[#00ff85] mb-2">

                        <!-- Scene 3 -->
                        <div class="script-segment p-5 rounded-lg border border-gray-700 bg-gray-800">
                            </ul>
                        </div>
                    </div>
                </div>
            </section>
            
            <!-- Process Section -->
            <section id="process" class="py-16 md:py-24 bg-f8f9fa">
                 <div class="container mx-auto px-6">
                    <div class="text-center mb-16">
                        <h2 class="text-3xl md:text-4xl font-bold text-gray-800">فرآیند همکاری با ما</h2>
                        <p class="mt-4 text-lg text-gray-600 max-w-3xl mx-auto">از ایده تا اجرا، ما یک مسیر شفاف و کارآمد را دنبال می‌کنیم تا اطمینان حاصل شود که بهترین راهکار متناسب با نیازهای شما ارائه می‌گردد. با نگه داشتن ماوس روی هر مرحله، جزئیات آن را مشاهده کنید.</p>
                    </div>
                    <div class="relative">
                        <div class="hidden md:block absolute top-1/2 left-0 w-full h-0.5 bg-gray-300 transform -translate-y-1/2"></div>
                        <div class="grid md:grid-cols-4 gap-8 relative">
                            <div class="timeline-item text-center">
                                <div class="timeline-dot w-6 h-6 mx-auto bg-gray-300 rounded-full border-4 border-white transition-all duration-300"></div>
                                <div class="timeline-content mt-4 p-4 rounded-md">
                                    <h3 class="text-lg font-semibold text-gray-700 transition-colors duration-300">۱. مشاوره و نیازسنجی</h3>
                                    <p class="text-sm text-gray-600 mt-2">تحلیل دقیق نیازمندی‌ها و اهداف شما برای ارائه راهکار اولیه.</p>
                                </div>
                            </div>
                            <div class="timeline-item text-center">
                                <div class="timeline-dot w-6 h-6 mx-auto bg-gray-300 rounded-full border-4 border-white transition-all duration-300"></div>
                                <div class="timeline-content mt-4 p-4 rounded-md">
                                    <h3 class="text-lg font-semibold text-gray-700 transition-colors duration-300">۲. طراحی و مهندسی</h3>
                                    <p class="text-sm text-gray-600 mt-2">ایجاد نقشه فنی و طراحی سیستم هوشمند متناسب با پروژه.</p>
                                </div>
                            </div>
                            <div class="timeline-item text-center">
                                <div class="timeline-dot w-6 h-6 mx-auto bg-gray-300 rounded-full border-4 border-white transition-all duration-300"></div>
                                <div class="timeline-content mt-4 p-4 rounded-md">
                                    <h3 class="text-lg font-semibold text-gray-700 transition-colors duration-300">۳. پیاده‌سازی و اجرا</h3>
                                    <p class="text-sm text-gray-600 mt-2">نصب و راه‌اندازی تجهیزات توسط تیم متخصص ما در محل پروژه.</p>
                                </div>
                            </div>
                            <div class="timeline-item text-center">
                                <div class="timeline-dot w-6 h-6 mx-auto bg-gray-300 rounded-full border-4 border-white transition-all duration-300"></div>
                                <div class="timeline-content mt-4 p-4 rounded-md">
                                    <h3 class="text-lg font-semibold text-gray-700 transition-colors duration-300">۴. پشتیبانی و بهینه‌سازی</h3>
                                    <p class="text-sm text-gray-600 mt-2">ارائه خدمات پس از فروش و به‌روزرسانی سیستم برای عملکرد بهتر.</p>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>
        </main>

        <footer class="bg-deep-blue text-white py-12">
            <div class="container mx-auto px-6 text-center">
                <h2 class="text-2xl md:text-3xl font-bold">با ما در تماس باشید</h2>
                <p class="mt-4 text-gray-300">برای شروع پروژه هوشمندسازی خود، همین امروز با ما تماس بگیرید.</p>
                <div class="mt-8 text-lg text-left inline-block" style="direction: ltr;">
                    <p class="flex items-center justify-end">
                        <span class="ml-3">www.omidkit.ir</span>
                        <span>🌐</span>
                    </p>
                    <div class="mt-4">
                        <p class="flex items-center justify-end font-semibold">
                            <span class="ml-3">تماس‌ها</span>
                            <span>📞</span>
                        </p>
                        <ul class="mt-2 space-y-1">
                            <li>کیمیا زهرا براتی: 09390886132</li>
                            <li>محسن بابایی: 09361717490</li>
                            <li>امید براتی: 09363399726</li>
                        </ul>
                    </div>
                </div>
                <div class="mt-10 border-t border-gray-700 pt-6">
                    <p class="text-gray-400">&copy; <span id="year"></span> هوشمند سازی صنعت امید. تمام حقوق محفوظ است.</p>
                </div>
            </div>
        </footer>
    </div>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();

        function toggleCard(cardElement) {
            const allCards = document.querySelectorAll('.card');
            allCards.forEach(c => {
                if (c !== cardElement && c.classList.contains('active')) {
                    c.classList.remove('active');
                    c.querySelector('.ml-auto').style.transform = 'rotate(0deg)';
                }
            });

            cardElement.classList.toggle('active');
            const icon = cardElement.querySelector('.ml-auto');
            if (cardElement.classList.contains('active')) {
                icon.style.transform = 'rotate(45deg)';
            } else {
                icon.style.transform = 'rotate(0deg)';
            }
        }
        
        const canvas = document.getElementById('heroCanvas');
        const ctx = canvas.getContext('2d');
        let particles = [];
        

        function resizeCanvas() {
            canvas.width = canvas.offsetWidth;
            canvas.height = canvas.offsetHeight;
        }

        class Particle {
            constructor() {
                this.x = Math.random() * canvas.width;
                this.y = Math.random() * canvas.height;
                this.vx = (Math.random() - 0.5) * 0.5;
                this.vy = (Math.random() - 0.5) * 0.5;
                this.radius = Math.random() * 1.5 + 1;
            }

            update() {
                this.x += this.vx;
                this.y += this.vy;

                if (this.x < 0 || this.x > canvas.width) this.vx *= -1;
                if (this.y < 0 || this.y > canvas.height) this.vy *= -1;
            }

            draw() {
                ctx.beginPath();
                ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2);
                ctx.fillStyle = 'rgba(0, 255, 133, 0.5)';
                ctx.fill();
            }
        }

        function init() {
            resizeCanvas();
            particles = [];
            for (let i = 0; i < 80; i++) {
                particles.push(new Particle());
            }
        }

        function animate() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            
            particles.forEach(p => {
                p.update();
                p.draw();
            });

            for (let i = 0; i < particles.length; i++) {
                for (let j = i; j < particles.length; j++) {
                    const dist = Math.hypot(particles[i].x - particles[j].x, particles[i].y - particles[j].y);
                    if (dist < 100) {
                        ctx.beginPath();
                        ctx.moveTo(particles[i].x, particles[i].y);
                        ctx.lineTo(particles[j].x, particles[j].y);
                        ctx.strokeStyle = `rgba(0, 255, 133, ${1 - dist / 100})`;
                        ctx.stroke();
                    }
                }
            }
            
            requestAnimationFrame(animate);
        }

        window.addEventListener('resize', init);
        init();
        animate();
    </script>
</body>
</html>
