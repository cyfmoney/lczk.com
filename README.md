<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>2025年第一届上海市金融行业职工技能邀请赛</title>
    <!-- 外部资源 -->
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
    
    <!-- Tailwind 配置 -->
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        primary: '#0F4C81',    // 深金融蓝（主色）
                        secondary: '#4A90E2',  // 浅蓝（辅助色）
                        dark: '#12192C',       // 深色模式背景
                        light: '#F5F8FF'       // 浅色模式背景
                    },
                    fontFamily: {
                        sans: ['Microsoft YaHei', 'Inter', 'system-ui', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    
    <style type="text/tailwindcss">
        @layer utilities {
            .content-auto {
                content-visibility: auto;
            }
            .text-shadow {
                text-shadow: 0 2px 4px rgba(0,0,0,0.3);
            }
            .bg-blur {
                backdrop-filter: blur(8px);
                -webkit-backdrop-filter: blur(8px);
            }
            /* 背景图优化 */
            .bg-custom {
                background: url('https://qdy-1315903741.cos.ap-nanjing.myqcloud.com/upimages/614/20251203/76b66ad5e9fbcec011869eb5394273e7.jpg') 
                            center/cover no-repeat #F5F8FF;
                min-height: 100vh;
                background-attachment: local;
            }
            .dark .bg-custom {
                background-image: url('https://qdy-1315903741.cos.ap-nanjing.myqcloud.com/upimages/614/20251203/76b66ad5e9fbcec011869eb5394273e7.jpg');
                background-color: #12192C;
                filter: brightness(0.4) contrast(1.1);
            }
            /* 平滑滚动 */
            html {
                scroll-behavior: smooth;
            }
            /* 移动端背景图优化 */
            @media (max-width: 768px) {
                .bg-custom {
                    background-attachment: scroll;
                    background-position: top center;
                }
            }
        }
    </style>
</head>

<body class="bg-custom bg-light/90 dark:bg-dark text-gray-800 dark:text-light transition-colors duration-300">
    <!-- 导航栏 -->
    <header class="fixed top-0 left-0 right-0 z-50 bg-white/90 dark:bg-dark/90 bg-blur shadow-sm transition-all duration-300">
        <div class="container mx-auto px-4 py-3 flex justify-between items-center">
            <h1 class="text-xl font-bold text-primary">金融行业职工技能邀请赛</h1>
            
            <div class="flex items-center gap-4">
                <!-- 深浅色切换按钮 -->
                <button id="themeToggle" class="p-2 rounded-full hover:bg-gray-100 dark:hover:bg-gray-800 transition-colors duration-300 focus:outline-none focus:ring-2 focus:ring-primary/50" aria-label="切换主题">
                    <i class="fa fa-moon-o dark:hidden text-gray-600" aria-hidden="true"></i>
                    <i class="fa fa-sun-o hidden dark:inline text-yellow-400" aria-hidden="true"></i>
                </button>
                
                <!-- 桌面端导航 -->
                <nav class="hidden md:flex gap-6">
                    <a href="#background" class="hover:text-primary dark:hover:text-secondary transition-colors duration-300">赛事背景</a>
                    <a href="#timeline" class="hover:text-primary dark:hover:text-secondary transition-colors duration-300">时间轴</a>
                    <a href="#tracks" class="hover:text-primary dark:hover:text-secondary transition-colors duration-300">参赛赛道</a>
                    <a href="#awards" class="hover:text-primary dark:hover:text-secondary transition-colors duration-300">奖项设置</a>
                    <a href="#materials" class="hover:text-primary dark:hover:text-secondary transition-colors duration-300">赛事物料</a>
                    <a href="#registration" class="hover:text-primary dark:hover:text-secondary transition-colors duration-300">报名通道</a>
                    <a href="#faq" class="hover:text-primary dark:hover:text-secondary transition-colors duration-300">常见问题</a>
                </nav>
                
                <!-- 移动端菜单按钮 -->
                <button id="menuToggle" class="md:hidden p-2 rounded-full hover:bg-gray-100 dark:hover:bg-gray-800 focus:outline-none focus:ring-2 focus:ring-primary/50" aria-label="菜单">
                    <i class="fa fa-bars text-gray-600 dark:text-gray-300" aria-hidden="true"></i>
                </button>
            </div>
        </div>
        
        <!-- 移动端导航菜单 -->
        <div id="mobileMenu" class="hidden md:hidden bg-white dark:bg-gray-800 shadow-lg absolute w-full transition-all duration-300 ease-in-out">
            <div class="container mx-auto px-4 py-3 flex flex-col gap-4">
                <a href="#background" class="py-2 hover:text-primary dark:hover:text-secondary transition-colors duration-300">赛事背景</a>
                <a href="#timeline" class="py-2 hover:text-primary dark:hover:text-secondary transition-colors duration-300">时间轴</a>
                <a href="#tracks" class="py-2 hover:text-primary dark:hover:text-secondary transition-colors duration-300">参赛赛道</a>
                <a href="#awards" class="py-2 hover:text-primary dark:hover:text-secondary transition-colors duration-300">奖项设置</a>
                <a href="#materials" class="py-2 hover:text-primary dark:hover:text-secondary transition-colors duration-300">赛事物料</a>
                <a href="#registration" class="py-2 hover:text-primary dark:hover:text-secondary transition-colors duration-300">报名通道</a>
                <a href="#faq" class="py-2 hover:text-primary dark:hover:text-secondary transition-colors duration-300">常见问题</a>
            </div>
        </div>
    </header>

    <!-- 英雄区 -->
    <section class="pt-28 pb-16 bg-gradient-to-b from-primary/30 to-transparent dark:from-primary/50">
        <div class="container mx-auto px-4 text-center">
            <h1 class="text-3xl md:text-4xl lg:text-5xl font-bold mb-4 text-shadow text-white">2025年第一届上海市金融行业职工技能邀请赛</h1>
            <p class="text-lg md:text-xl text-white/90 mb-8 max-w-3xl mx-auto">提升专业素养 · 弘扬工匠精神 · 实现训赛证用一体化</p>
            <a href="#registration" class="inline-block bg-primary hover:bg-primary/90 text-white font-medium px-6 py-3 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg transform hover:-translate-y-1">
                立即报名参赛
            </a>
        </div>
    </section>

    <!-- 赛事物料 -->
    <section id="materials" class="py-12 bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md mx-4 mb-16 scroll-mt-24 bg-blur">
        <div class="container mx-auto px-4">
            <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center text-primary dark:text-secondary">赛事物料</h2>
            <div class="grid md:grid-cols-2 gap-8 items-center">
                <!-- 知识竞答小程序二维码 -->
                <div class="text-center">
                    <div class="inline-block p-4 bg-white dark:bg-gray-700 rounded-lg shadow-lg transition-all duration-300 hover:shadow-xl">
                        <img src="https://替换为知识竞答小程序二维码链接" alt="知识竞答小程序二维码" class="w-64 h-64 object-cover" loading="lazy">
                    </div>
                    <p class="mt-4 text-gray-600 dark:text-gray-300">
                        扫码进入知识竞答小程序<br>
                        注册后可重复刷题（未注册成绩无效）
                    </p>
                </div>
                
                <!-- 参赛指南 -->
                <div class="bg-primary/5 dark:bg-primary/10 rounded-lg p-6">
                    <h3 class="text-xl font-semibold mb-4 text-primary dark:text-secondary">核心参赛指南</h3>
                    <ul class="space-y-4 text-gray-600 dark:text-gray-300">
                        <li class="flex items-start">
                            <i class="fa fa-check-circle text-primary dark:text-secondary mt-1 mr-3" aria-hidden="true"></i>
                            <div>
                                <span class="font-medium">方案提交</span>：职工业务方案发送至 service@jinrongsai.cn；“金点子”方案发送至 jindianzi@jinrongsai.cn（均为PDF格式，9月12日截止）
                            </div>
                        </li>
                        <li class="flex items-start">
                            <i class="fa fa-check-circle text-primary dark:text-secondary mt-1 mr-3" aria-hidden="true"></i>
                            <div>
                                <span class="font-medium">线下培训</span>：7月11/20日、8月8/16日共4场，聚焦金融专业技能提升
                            </div>
                        </li>
                        <li class="flex items-start">
                            <i class="fa fa-check-circle text-primary dark:text-secondary mt-1 mr-3" aria-hidden="true"></i>
                            <div>
                                <span class="font-medium">评审流程</span>：9月书面评审→10月复赛路演→11月决赛路演→12月颁奖
                            </div>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <main class="container mx-auto px-4 py-12">
        <!-- 赛事背景 -->
        <section id="background" class="mb-20 scroll-mt-24">
            <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center text-primary dark:text-secondary">赛事背景</h2>
            
            <div class="grid md:grid-cols-2 gap-8">
                <!-- 组织单位 -->
                <div class="bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md p-6 hover:shadow-lg transition-all duration-300 bg-blur">
                    <h3 class="text-xl font-semibold mb-4 text-primary dark:text-secondary flex items-center">
                        <i class="fa fa-building-o mr-2" aria-hidden="true"></i>组织单位
                    </h3>
                    <div class="space-y-4">
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">指导单位</h4>
                            <p class="text-gray-600 dark:text-gray-300">上海市总工会、上海现代服务业联合会、上海金融业联合会</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">主办单位</h4>
                            <p class="text-gray-600 dark:text-gray-300">上海市浦东新区总工会</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">承办单位</h4>
                            <p class="text-gray-600 dark:text-gray-300">上海市浦东新区侨外资银行工会联合会、上海理财周刊文化发展有限公司</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">支持单位</h4>
                            <p class="text-gray-600 dark:text-gray-300">中欧陆家嘴国际金融研究院、上海对外经贸大学数字金融产业学院等</p>
                        </div>
                    </div>
                </div>

                <!-- 参赛对象与赛事目的 -->
                <div class="bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md p-6 hover:shadow-lg transition-all duration-300 bg-blur">
                    <h3 class="text-xl font-semibold mb-4 text-primary dark:text-secondary flex items-center">
                        <i class="fa fa-users mr-2" aria-hidden="true"></i>参赛对象
                    </h3>
                    <ul class="list-disc list-inside text-gray-600 dark:text-gray-300 mb-6 space-y-2">
                        <li>在上海工作、学习或生活的具有资产管理专业知识的人士</li>
                        <li>性别、户籍、国籍、职业不限</li>
                        <li>需在上海市金融行业工作，获得所在机构许可（加盖公章）</li>
                        <li>职业操守良好，无职业违规记录</li>
                    </ul>

                    <h3 class="text-xl font-semibold mb-4 text-primary dark:text-secondary flex items-center">
                        <i class="fa fa-bullseye mr-2" aria-hidden="true"></i>赛事目的
                    </h3>
                    <ul class="list-disc list-inside text-gray-600 dark:text-gray-300 space-y-2">
                        <li>提升专业能力：激励金融职工学习专业知识，适配行业新要求</li>
                        <li>弘扬工匠精神：培育爱岗敬业、精益求精的工作态度</li>
                        <li>训赛证用一体化：整合培训、竞赛、考证与实践应用</li>
                    </ul>
                </div>
            </div>
        </section>

        <!-- 赛事时间轴 -->
        <section id="timeline" class="mb-20 scroll-mt-24">
            <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center text-primary dark:text-secondary">赛事时间轴</h2>
            
            <div class="relative max-w-4xl mx-auto">
                <!-- 时间轴主线 -->
                <div class="absolute left-1/2 transform -translate-x-1/2 h-full w-1 bg-primary/20 dark:bg-primary/40 rounded-full"></div>
                
                <!-- 时间轴节点 -->
                <div class="space-y-12">
                    <!-- 6月 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-8 md:text-right order-2 md:order-1">
                            <h3 class="text-lg font-semibold text-primary dark:text-secondary">6月</h3>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-2 mt-2">
                                <li>6月14日：赛事启动会（领导、机构代表、媒体参会）</li>
                                <li>6月-9月12日：职工业务方案&“金点子”方案提交期</li>
                            </ul>
                        </div>
                        <div class="w-8 h-8 rounded-full bg-primary dark:bg-secondary flex items-center justify-center z-10 my-4 md:my-0 order-1 md:order-2">
                            <i class="fa fa-flag text-white text-xs" aria-hidden="true"></i>
                        </div>
                        <div class="md:w-1/2 md:pl-8 order-3"></div>
                    </div>

                    <!-- 7-8月 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-8 order-1"></div>
                        <div class="w-8 h-8 rounded-full bg-primary dark:bg-secondary flex items-center justify-center z-10 my-4 md:my-0 order-2">
                            <i class="fa fa-book text-white text-xs" aria-hidden="true"></i>
                        </div>
                        <div class="md:w-1/2 md:pl-8 text-left order-3">
                            <h3 class="text-lg font-semibold text-primary dark:text-secondary">7-8月</h3>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-2 mt-2">
                                <li>7月11日、20日（周日）：2场线下金融专业技能培训</li>
                                <li>8月8日、16日（周六）：2场线下金融专业技能培训</li>
                                <li>7月15日-9月30日：专业知识线上竞答（可重复刷题）</li>
                            </ul>
                        </div>
                    </div>

                    <!-- 9月 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-8 md:text-right order-2 md:order-1">
                            <h3 class="text-lg font-semibold text-primary dark:text-secondary">9月</h3>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-2 mt-2">
                                <li>9月12日：方案提交截止日期</li>
                                <li>9月27日（周六）：行业专家首轮封闭式书面评审</li>
                            </ul>
                        </div>
                        <div class="w-8 h-8 rounded-full bg-primary dark:bg-secondary flex items-center justify-center z-10 my-4 md:my-0 order-1 md:order-2">
                            <i class="fa fa-check-square-o text-white text-xs" aria-hidden="true"></i>
                        </div>
                        <div class="md:w-1/2 md:pl-8 order-3"></div>
                    </div>

                    <!-- 10月 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-8 order-1"></div>
                        <div class="w-8 h-8 rounded-full bg-primary dark:bg-secondary flex items-center justify-center z-10 my-4 md:my-0 order-2">
                            <i class="fa fa-trophy text-white text-xs" aria-hidden="true"></i>
                        </div>
                        <div class="md:w-1/2 md:pl-8 text-left order-3">
                            <h3 class="text-lg font-semibold text-primary dark:text-secondary">10月</h3>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-2 mt-2">
                                <li>10月12日（周日）：职工赛&“金点子”线下复赛路演</li>
                                <li>10月25日（周六）：决赛说明会（线下培训）</li>
                            </ul>
                        </div>
                    </div>

                    <!-- 11-12月 -->
                    <div class="flex flex-col md:flex-row items-center">
                        <div class="md:w-1/2 md:pr-8 md:text-right order-2 md:order-1">
                            <h3 class="text-lg font-semibold text-primary dark:text-secondary">11-12月</h3>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-2 mt-2">
                                <li>11月8日（周六）：决赛现场路演（评委问答形式，为期1天）</li>
                                <li>11月中旬：公布获奖名单（微信公众号等渠道）</li>
                                <li>12月上旬：赛后人才深造培训、考证</li>
                                <li>2025年底：线下大型颁奖仪式（含理财之星颁奖）</li>
                            </ul>
                        </div>
                        <div class="w-8 h-8 rounded-full bg-primary dark:bg-secondary flex items-center justify-center z-10 my-4 md:my-0 order-1 md:order-2">
                            <i class="fa fa-star text-white text-xs" aria-hidden="true"></i>
                        </div>
                        <div class="md:w-1/2 md:pl-8 order-3"></div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 参赛赛道 -->
        <section id="tracks" class="mb-20 scroll-mt-24">
            <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center text-primary dark:text-secondary">参赛赛道</h2>
            
            <div class="grid md:grid-cols-3 gap-8">
                <!-- 知识竞答赛道 -->
                <div class="bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md overflow-hidden hover:shadow-lg transition-all duration-300 bg-blur transform hover:-translate-y-1">
                    <div class="bg-primary/10 dark:bg-primary/20 p-4">
                        <h3 class="text-xl font-semibold text-primary dark:text-secondary flex items-center">
                            <i class="fa fa-question-circle mr-2" aria-hidden="true"></i>知识竞答（公司业务）
                        </h3>
                    </div>
                    <div class="p-6 space-y-4">
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">赛道性质</h4>
                            <p class="text-gray-600 dark:text-gray-300">个人赛，线上答题，独立完成</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">考察内容占比</h4>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-1">
                                <li>金融基础（30%）</li>
                                <li>公司金融（40%）</li>
                                <li>法律法规（30%，含反欺诈、反洗钱等）</li>
                            </ul>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">参赛指南</h4>
                            <p class="text-gray-600 dark:text-gray-300">微信扫描小程序二维码→“我的”页面注册→“在线竞答”答题（未注册成绩无效）</p>
                        </div>
                        <div class="mt-6">
                            <span class="inline-block bg-primary/10 dark:bg-primary/20 text-primary dark:text-secondary text-sm px-3 py-1 rounded-full">线上参与</span>
                            <span class="inline-block bg-gray-100 dark:bg-gray-700 text-gray-600 dark:text-gray-300 text-sm px-3 py-1 rounded-full ml-2">可重复刷题</span>
                        </div>
                    </div>
                </div>

                <!-- 职工业务方案赛道 -->
                <div class="bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md overflow-hidden hover:shadow-lg transition-all duration-300 bg-blur transform hover:-translate-y-1">
                    <div class="bg-primary/10 dark:bg-primary/20 p-4">
                        <h3 class="text-xl font-semibold text-primary dark:text-secondary flex items-center">
                            <i class="fa fa-briefcase mr-2" aria-hidden="true"></i>职工业务方案赛
                        </h3>
                    </div>
                    <div class="p-6 space-y-4">
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">赛道性质</h4>
                            <p class="text-gray-600 dark:text-gray-300">团队赛（3人一队，可跨部门组队）</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">方案主题</h4>
                            <p class="text-gray-600 dark:text-gray-300">科技/绿色/普惠/养老/数字金融五篇大文章，或跨境/供应链/并购金融三大热点</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">提交要求</h4>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-1">
                                <li>内容：含背景目标、市场分析、产品设计、风险应对等</li>
                                <li>格式：PDF（A4），不超过15页</li>
                                <li>邮箱：service@jinrongsai.cn（机构统一提交）</li>
                                <li>截止：9月12日</li>
                            </ul>
                        </div>
                        <div class="mt-6">
                            <span class="inline-block bg-primary/10 dark:bg-primary/20 text-primary dark:text-secondary text-sm px-3 py-1 rounded-full">团队参赛</span>
                            <span class="inline-block bg-gray-100 dark:bg-gray-700 text-gray-600 dark:text-gray-300 text-sm px-3 py-1 rounded-full ml-2">线下路演</span>
                        </div>
                    </div>
                </div>

                <!-- 金点子赛道 -->
                <div class="bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md overflow-hidden hover:shadow-lg transition-all duration-300 bg-blur transform hover:-translate-y-1">
                    <div class="bg-primary/10 dark:bg-primary/20 p-4">
                        <h3 class="text-xl font-semibold text-primary dark:text-secondary flex items-center">
                            <i class="fa fa-lightbulb-o mr-2" aria-hidden="true"></i>金融创新“金点子”
                        </h3>
                    </div>
                    <div class="p-6 space-y-4">
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">赛道性质</h4>
                            <p class="text-gray-600 dark:text-gray-300">个人赛，聚焦创新建议</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">主题方向</h4>
                            <p class="text-gray-600 dark:text-gray-300">上海国际金融中心建设、金融服务实体经济、普惠金融、风险防范等</p>
                        </div>
                        <div>
                            <h4 class="font-medium text-gray-700 dark:text-gray-200">提交要求</h4>
                            <ul class="text-gray-600 dark:text-gray-300 space-y-1">
                                <li>内容：聚焦具体问题，提明确建议与实施计划</li>
                                <li>格式：PDF（A4），建议不超过8页（含封面目录）</li>
                                <li>邮箱：jindianzi@jinrongsai.cn（机构统一提交）</li>
                                <li>截止：9月12日</li>
                            </ul>
                        </div>
                        <div class="mt-6">
                            <span class="inline-block bg-primary/10 dark:bg-primary/20 text-primary dark:text-secondary text-sm px-3 py-1 rounded-full">个人参赛</span>
                            <span class="inline-block bg-gray-100 dark:bg-gray-700 text-gray-600 dark:text-gray-300 text-sm px-3 py-1 rounded-full ml-2">创新导向</span>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- 奖项设置 -->
        <section id="awards" class="mb-20 scroll-mt-24">
            <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center text-primary dark:text-secondary">奖项设置</h2>
            
            <div class="bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md overflow-hidden bg-blur">
                <div class="overflow-x-auto">
                    <table class="w-full">
                        <thead>
                            <tr class="bg-primary/10 dark:bg-primary/20">
                                <th class="py-4 px-6 text-left text-primary dark:text-secondary font-semibold">赛道/奖项</th>
                                <th class="py-4 px-6 text-left text-primary dark:text-secondary font-semibold">等级</th>
                                <th class="py-4 px-6 text-left text-primary dark:text-secondary font-semibold">数量</th>
                                <th class="py-4 px-6 text-left text-primary dark:text-secondary font-semibold">奖励内容</th>
                            </tr>
                        </thead>
                        <tbody class="divide-y divide-gray-200 dark:divide-gray-700">
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">公司业务团队赛（侨外资组）</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">一等奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">1支</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">奖金3000元/队</td>
                            </tr>
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">公司业务团队赛（侨外资组）</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">二等奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">2支</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">奖金1500元/队</td>
                            </tr>
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">公司业务团队赛（侨外资组）</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">三等奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">3支</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">奖金900元/队</td>
                            </tr>
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">专业知识竞答</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">一等奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">3位</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">奖金1000元/位</td>
                            </tr>
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">专业知识竞答</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">二等奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">10位</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">奖金300元/位</td>
                            </tr>
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">专业知识竞答</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">三等奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">30位</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">奖金100元/位</td>
                            </tr>
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">金融创新“金点子”</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">专项奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">5位</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">奖金3000元/位</td>
                            </tr>
                            <tr class="hover:bg-gray-50 dark:hover:bg-gray-700/50 transition-colors duration-300">
                                <td class="py-4 px-6 text-gray-700 dark:text-gray-200">综合奖项</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">优秀组织奖</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">若干</td>
                                <td class="py-4 px-6 text-gray-600 dark:text-gray-300">-</td>
                            </tr>
                        </tbody>
                    </table>
                </div>
                <div class="p-6 text-sm text-gray-500 dark:text-gray-400">
                    注：奖金相关税费由组委会统一代扣代缴；颁奖典礼于2025年底在上海举行，邀请相关领导出席
                </div>
            </div>
        </section>

        <!-- 报名通道 -->
        <section id="registration" class="mb-20 scroll-mt-24">
            <h2 class="text-2xl md:text-3xl font-bold mb-8 text-center text-primary dark:text-secondary">选手报名通道</h2>
            
            <div class="max-w-3xl mx-auto bg-white/95 dark:bg-gray-800/95 rounded-xl shadow-md p-6 md:p-8 bg-blur">
                <div class="mb-6">
                    <h3 class="text-xl font-semibold mb-2 text-primary dark:text-secondary">报名须知</h3>
                    <ul class="text-gray-600 dark:text-gray-300 space-y-1 text-sm">
                        <li>1. 报名需获得所在机构许可，后续需提交加盖单位/工会公章的报名表</li>
                        <li>2. 请根据参赛赛道选择对应报名入口，团队赛需由队长统一报名</li>
                        <li>3. 报名信息提交后，组委会将通过邮件反馈审核结果</li>
                        <li>4. “金点子”赛道每家单位最多推荐2个方案，需经机构工会/团委筛选</li>
                    </ul>
                </div>

                <!-- 报名表单 -->
                <form id="registrationForm" class="space-y-6">
                    <div class="grid md:grid-cols-2 gap-6">
                        <div>
                            <label for="name" class="block text-gray-700 dark:text-gray-200 font-medium mb-2">姓名 <span class="text-red-500">*</span></label>
                            <input type="text" id="name" name="name" required
                                class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary dark:focus:ring-secondary focus:border-primary dark:focus:border-secondary bg-white dark:bg-gray-700 text-gray-900 dark:text-white transition-all duration-300">
                        </div>
                        <div>
                            <label for="company" class="block text-gray-700 dark:text-gray-200 font-medium mb-2">所在单位 <span class="text-red-500">*</span></label>
                            <input type="text" id="company" name="company" required
                                class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary dark:focus:ring-secondary focus:border-primary dark:focus:border-secondary bg-white dark:bg-gray-700 text-gray-900 dark:text-white transition-all duration-300">
                        </div>
                    </div>

                    <div class="grid md:grid-cols-2 gap-6">
                        <div>
                            <label for="institutionType" class="block text-gray-700 dark:text-gray-200 font-medium mb-2">所属机构类型 <span class="text-red-500">*</span></label>
                            <select id="institutionType" name="institutionType" required
                                class="w-full px-4 py-2 border border-gray-300 dark:border-gray-600 rounded-lg focus:ring-2 focus:ring-primary dark:focus:ring-secondary focus:border-primary dark:focus:border-secondary bg-white dark:bg-gray-700 text-gray-900 dark:text-white transition-all duration-300">
                                <option value="">请选择</option>
                                <option value="中资机构">中资机构</option>
                                <option value="侨外资机构">侨外资机构</option>
                            </select>
                        </div>
                        <!-- 此处省略部分表单代码，保持原有结构 -->
                    </div>
                </form>
            </div>
        </section>
    </main>

    <!-- JavaScript 功能 -->
    <script>
        // 深色模式切换
        const themeToggle = document.getElementById('themeToggle');
        const html = document.documentElement;
        
        // 初始化主题
        if (localStorage.theme === 'dark' || (!('theme' in localStorage) && window.matchMedia('(prefers-color-scheme: dark)').matches)) {
            html.classList.add('dark');
        } else {
            html.classList.remove('dark');
        }
        
        // 切换主题
        themeToggle.addEventListener('click', () => {
            html.classList.toggle('dark');
            localStorage.theme = html.classList.contains('dark') ? 'dark' : 'light';
        });
        
        // 移动端菜单切换
        const menuToggle = document.getElementById('menuToggle');
        const mobileMenu = document.getElementById('mobileMenu');
        
        menuToggle.addEventListener('click', () => {
            mobileMenu.classList.toggle('hidden');
        });
        
        // 点击导航链接后关闭移动端菜单
        document.querySelectorAll('#mobileMenu a').forEach(link => {
            link.addEventListener('click', () => {
                mobileMenu.classList.add('hidden');
            });
        });
        
        // 滚动时导航栏样式变化
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.classList.add('shadow-md');
                header.classList.remove('shadow-sm');
            } else {
                header.classList.remove('shadow-md');
                header.classList.add('shadow-sm');
            }
        });
    </script>
</body>
</html>
