<!DOCTYPE html>
<html lang="zh-CN">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
  <title>酸奶单词 - 趣味背单词</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link href="https://cdn.jsdelivr.net/npm/font-awesome@4.7.0/css/font-awesome.min.css" rel="stylesheet">
  
  <!-- 配置Tailwind -->
  <script>
    tailwind.config = {
      theme: {
        extend: {
          colors: {
            primary: '#3B82F6',
            secondary: '#10B981',
            accent: '#F59E0B',
            dark: '#1E293B',
            light: '#F8FAFC'
          },
          fontFamily: {
            sans: ['Inter', 'system-ui', 'sans-serif'],
          },
        },
      }
    }
  </script>
  
  <style type="text/tailwindcss">
    @layer utilities {
      .content-auto {
        content-visibility: auto;
      }
      .card-shadow {
        box-shadow: 0 10px 25px -5px rgba(59, 130, 246, 0.1), 0 8px 10px -6px rgba(59, 130, 246, 0.1);
      }
      .card-hover {
        transition: all 0.3s ease;
      }
      .card-hover:hover {
        transform: translateY(-5px);
        box-shadow: 0 20px 25px -5px rgba(59, 130, 246, 0.15), 0 8px 10px -6px rgba(59, 130, 246, 0.15);
      }
      .text-gradient {
        background-clip: text;
        -webkit-background-clip: text;
        color: transparent;
        background-image: linear-gradient(45deg, #3B82F6, #10B981);
      }
      .btn-bounce {
        transition: transform 0.2s ease;
      }
      .btn-bounce:active {
        transform: scale(0.95);
      }
      /* 确保Font Awesome图标在所有设备上正常显示 */
      .fa {
        display: inline-block !important;
        font-family: 'FontAwesome' !important;
        font-style: normal !important;
        font-weight: normal !important;
        line-height: 1 !important;
        speak: none;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        /* 确保图标大小在移动端足够清晰 */
        font-size: inherit !important;
      }
      
      /* 缩小例句、洗脑记忆和Rap记忆部分的喇叭图标 */
      h3 > button .fa-volume-up {
        font-size: 0.8em !important;
        width: 1em;
        height: 1em;
        display: flex !important;
        align-items: center;
        justify-content: center;
      }
      
      /* 设置标题前的彩色竖线 */
      .example-line {
        width: 3px;
        height: 0.9em;
        background-color: #3B82F6; /* 蓝色 */
        border-radius: 2px;
        align-self: center;
      }
      
      .memory-line {
        width: 3px;
        height: 0.9em;
        background-color: #10B981; /* 绿色 */
        border-radius: 2px;
        align-self: center;
      }
      
      .rap-line {
        width: 3px;
        height: 0.9em;
        background-color: #F59E0B; /* 黄色 */
        border-radius: 2px;
        align-self: center;
      }
      
      /* 移动端图标响应式优化 */
      @media (max-width: 640px) {
        .fa {
          font-size: 1.2em !important;
        }
        
        /* 确保标题前的图标在移动端正确显示 */
        h3 .fa {
          margin-right: 0.5rem;
          width: 1.2em;
          height: 1.2em;
          display: flex !important;
          align-items: center;
          justify-content: center;
        }
        
        /* 确保喇叭按钮在移动端足够大，易于点击 */
        button .fa-volume-up {
          font-size: 1.3em !important;
          width: 1.5em;
          height: 1.5em;
          display: flex !important;
          align-items: center;
          justify-content: center;
        }
      }
    }
  </style>
</head>
<body class="bg-gray-50 dark:bg-dark min-h-screen transition-colors duration-300">
  <!-- 顶部导航 -->
  <header class="bg-white dark:bg-gray-800 shadow-sm sticky top-0 z-50 transition-colors duration-300">
    <div class="container mx-auto px-4 py-4 flex justify-between items-center">
      <div class="flex items-center space-x-2">
        <i class="fa fa-book text-primary text-2xl"></i>
        <h1 class="text-xl md:text-2xl font-bold text-gradient">酸奶单词</h1>
      </div>
      
      <div class="flex items-center space-x-4">
        <button id="info-btn" class="p-2 rounded-full hover:bg-gray-100 dark:hover:bg-gray-700 transition-colors">
          <i class="fa fa-info text-gray-600 dark:text-gray-300"></i>
        </button>
      </div>
    </div>
  </header>

  <!-- 主内容区 -->
  <main class="container mx-auto px-4 py-8 md:py-16">
    
    
    <!-- 单词卡片 -->
    <div class="max-w-3xl mx-auto">
      <div id="word-card" class="bg-white dark:bg-gray-800 rounded-2xl p-6 md:p-8 card-shadow card-hover transition-all duration-500">
        <!-- 单词和音标 -->
        <div class="mb-2">
          <h2 id="word" class="text-3xl md:text-4xl font-bold text-gray-800 dark:text-white inline-block">diligent</h2>
          <span id="phonetic" class="text-gray-500 dark:text-gray-400 italic ml-3 mr-2">/ˈdɪlɪdʒənt/</span>
          <button onclick="speakWord()" class="text-primary hover:text-primary/80 transition-colors btn-bounce inline-block">
            <i class="fa fa-volume-up"></i>
          </button>
        </div>
        
        <!-- 单词释义 -->
        <div class="mb-6">
          <span id="part-of-speech" class="bg-primary/10 text-primary px-3 py-1 rounded-full text-sm font-medium">adj. 勤奋的，勤勉的</span>
        </div>
        
        <!-- 例句 -->
        <div class="mb-6">
          <h3 class="text-lg font-semibold text-gray-700 dark:text-gray-200 mb-3 flex items-center">
            <span class="example-line mr-2"></span>例句
            <button onclick="speakExample()" class="text-primary hover:text-primary/80 transition-colors btn-bounce ml-2">
              <i class="fa fa-volume-up"></i>
            </button>
          </h3>
          <div class="bg-gray-50 dark:bg-gray-700/50 p-4 rounded-xl">
            <p id="example-sentence" class="text-gray-800 dark:text-gray-200 mb-2">I am diligent in my studies.</p>
            <p id="example-translation" class="text-gray-600 dark:text-gray-400 text-sm">我学习很勤奋。</p>
          </div>
        </div>
        
        <!-- 中英文结合语句 -->
        <div class="mb-6">
          <h3 class="text-lg font-semibold text-gray-700 dark:text-gray-200 mb-3 flex items-center">
            <span class="memory-line mr-2"></span>洗脑记忆
            <button onclick="speakMixedSentence()" class="text-secondary hover:text-secondary/80 transition-colors btn-bounce ml-2">
              <i class="fa fa-volume-up"></i>
            </button>
          </h3>
          <p id="mixed-sentence" class="text-gray-800 dark:text-gray-200 bg-secondary/5 p-4 rounded-xl">
            小明是个<strong class="text-secondary">diligent</strong>的学生，每天<strong class="text-secondary">diligent</strong>地刷题，成绩一直很优异。在学习上<strong class="text-secondary">diligent</strong>，是通往成功的阶梯，他因此收获了老师的表扬和同学的敬佩。
          </p>
        </div>
        
        <!-- Rap语句 -->
        <div>
          <h3 class="text-lg font-semibold text-gray-700 dark:text-gray-200 mb-3 flex items-center">
            <span class="rap-line mr-2"></span>Rap记忆
            <button onclick="speakRapSentence()" class="text-accent hover:text-accent/80 transition-colors btn-bounce ml-2">
              <i class="fa fa-volume-up"></i>
            </button>
          </h3>
          <div id="rap-sentence" class="text-gray-800 dark:text-gray-200 bg-accent/5 p-4 rounded-xl">
            <p>勤奋<strong class="text-accent">diligent</strong>从不懒，学习工作冲在前。每日耕耘不停歇，成功大门为你开～</p>
          </div>
        </div>
      </div>
      
      <!-- 导航按钮 -->
      <div class="flex justify-between items-center mt-8">
        <button id="prev-btn" class="bg-white dark:bg-gray-700 text-gray-700 dark:text-gray-200 px-6 py-3 rounded-full shadow hover:shadow-md transition-all disabled:opacity-50 disabled:cursor-not-allowed btn-bounce">
          <i class="fa fa-arrow-left mr-2"></i>上一个
        </button>
        <span id="word-counter" class="text-gray-400 dark:text-gray-500">1/10</span>
        <button id="next-btn" class="bg-secondary text-white px-6 py-3 rounded-full shadow hover:shadow-md hover:bg-secondary/90 transition-all btn-bounce">
          下一个<i class="fa fa-arrow-right ml-2"></i>
        </button>
      </div>
    </div>
  </main>
  
  <!-- 信息弹窗 -->
  <div id="info-modal" class="fixed inset-0 bg-black/50 z-50 flex items-center justify-center hidden">
    <div class="bg-white dark:bg-gray-800 rounded-2xl p-6 max-w-md w-full mx-4 transform transition-all">
      <div class="flex justify-between items-start mb-4">
        <h3 class="text-xl font-bold text-gray-800 dark:text-white">使用说明</h3>
        <button id="close-modal" class="text-gray-500 hover:text-gray-700 dark:text-gray-400 dark:hover:text-gray-200">
          <i class="fa fa-times"></i>
        </button>
      </div>
      <ul class="space-y-3 text-gray-600 dark:text-gray-300">
        <li class="flex items-start">
          <i class="fa fa-volume-up text-primary mt-1 mr-2"></i>
          <span>点击喇叭图标可以朗读单词和例句</span>
        </li>
        <li class="flex items-start">
          <i class="fa fa-arrow-left text-gray-500 mt-1 mr-2"></i>
          <i class="fa fa-arrow-right text-gray-500 mt-1 mr-2"></i>
          <span>使用箭头按钮切换单词</span>
        </li>

        <li class="flex items-start">
          <i class="fa fa-star text-accent mt-1 mr-2"></i>
          <span>通过趣味Rap语句和中英文洗脑内容帮助记忆单词</span>
        </li>
      </ul>
      <button id="got-it-btn" class="mt-6 w-full bg-primary text-white py-3 rounded-lg hover:bg-primary/90 transition-colors btn-bounce">
        明白了
      </button>
    </div>
  </div>
  <script>
    // 单词数据
    const vocabularyList = [
      {
        word: "lucky",
        phonetic: "/ˈlʌki/",
        partOfSpeech: "adj. 幸运的;侥幸的",
        example: "I have been very lucky recently.",
        exampleCn: "自己最近非常幸运。",
        mixed: "昨天我出门没带伞，本以为会被淋成落汤鸡，结果刚走到公交站，雨就停了，我可真是<strong class='text-secondary'>lucky</strong>。今天去买彩票，没想到还中了个小奖，哎呀，感觉自己最近<strong class='text-secondary'>lucky</strong>极了。希望这份<strong class='text-secondary'>lucky</strong>能一直延续下去呀。",
        rap: "昨日出门忘带伞，以为要成落汤汉。\n走到站时雨刚散，好运降临心喜欢。\n今日彩票买一玩，中个小奖乐翻天。\n最近<span style='color: orange;'><strong>lucky</strong></span>特别赞，但愿一直不间断。"
      },
      {
        word: "generous",
        phonetic: "/ˈdʒenərəs/",
        partOfSpeech: "adj. 慷慨的，大方的",
        example: "She is generous to help others.",
        exampleCn: "她很慷慨地帮助他人。",
        mixed: "李姐是个<strong class='text-secondary'>generous</strong>的人，经常<strong class='text-secondary'>generous</strong>地分享自己的资源，大家都很喜欢她。为人<strong class='text-secondary'>generous</strong>，能收获真诚的友谊，她的善良也让身边充满温暖。",
        rap: "慷慨<strong class='text-accent'>generous</strong>真大方，分享帮助暖心房。待人接物有格局，好人缘来不用慌～"
      },
      {
        word: "persistent",
        phonetic: "/pərˈsɪstənt/",
        partOfSpeech: "adj. 坚持不懈的，执着的",
        example: "He is persistent in achieving his goal.",
        exampleCn: "他执着于实现自己的目标。",
        mixed: "小张对梦想很<strong class='text-secondary'>persistent</strong>，即便遇到困难也<strong class='text-secondary'>persistent</strong>地坚持，从未放弃。做事<strong class='text-secondary'>persistent</strong>，才能突破重重阻碍，他的毅力最终让梦想照进现实。",
        rap: "执着<strong class='text-accent'>persistent</strong>不退缩，目标在前勇拼搏。风雨兼程不放弃，终有一日花结果～"
      },
      {
        word: "ambitious",
        phonetic: "/æmˈbɪʃəs/",
        partOfSpeech: "adj. 有雄心的，有抱负的",
        example: "She is an ambitious young woman.",
        exampleCn: "她是个有雄心的年轻女性。",
        mixed: "小王是个<strong class='text-secondary'>ambitious</strong>的创业者，他有很多<strong class='text-secondary'>ambitious</strong>的计划，并且正在努力实现。拥有<strong class='text-secondary'>ambitious</strong>的目标，能让人不断进步，最终成就更好的自己。",
        rap: "雄心勃勃<strong class='text-accent'>ambitious</strong>，目标清晰不迷失。敢想敢做有魄力，未来可期展宏图～"
      },
      {
        word: "tolerant",
        phonetic: "/ˈtɑːlərənt/",
        partOfSpeech: "adj. 宽容的，容忍的",
        example: "We should be tolerant of different opinions.",
        exampleCn: "我们应该容忍不同的意见。",
        mixed: "张老师是个<strong class='text-secondary'>tolerant</strong>的人，对学生总是很<strong class='text-secondary'>tolerant</strong>，耐心引导。学会<strong class='text-secondary'>tolerant</strong>，能让人际关系更和谐，也能让自己的心态更平和。",
        rap: "宽容待人<strong class='text-accent'>tolerant</strong>，心胸开阔路更宽。理解尊重多包容，生活处处是阳光～"
      },
      {
        word: "confident",
        phonetic: "/ˈkɑːnfɪdənt/",
        partOfSpeech: "adj. 自信的，有信心的",
        example: "He feels confident about his future.",
        exampleCn: "他对自己的未来充满信心。",
        mixed: "小李在演讲时总是很<strong class='text-secondary'>confident</strong>，这种<strong class='text-secondary'>confident</strong>的态度感染了很多人。保持<strong class='text-secondary'>confident</strong>，能让我们更好地发挥自己的能力，迎接各种挑战。",
        rap: "自信满满<strong class='text-accent'>confident</strong>，昂首挺胸向前行。相信自己有力量，困难面前不慌张～"
      },
      {
        word: "curious",
        phonetic: "/ˈkjʊriəs/",
        partOfSpeech: "adj. 好奇的，求知欲强的",
        example: "Children are naturally curious about the world.",
        exampleCn: "孩子们对世界天生好奇。",
        mixed: "小林是个<strong class='text-secondary'>curious</strong>的科学家，他对一切未知都很<strong class='text-secondary'>curious</strong>。保持<strong class='text-secondary'>curious</strong>，能让我们不断探索新知识，拓展自己的视野。",
        rap: "充满好奇<strong class='text-accent'>curious</strong>，世界奥秘去探知。问个究竟不满足，知识海洋任遨游～"
      },
      {
        word: "sincere",
        phonetic: "/sɪnˈsɪr/",
        partOfSpeech: "adj. 真诚的，诚挚的",
        example: "She gave a sincere apology for her mistake.",
        exampleCn: "她为自己的错误真诚道歉。",
        mixed: "王阿姨待人很<strong class='text-secondary'>sincere</strong>，她的<strong class='text-secondary'>sincere</strong>总能打动别人。待人<strong class='text-secondary'>sincere</strong>，能收获真正的友谊，让生活更加温暖。",
        rap: "待人真诚<strong class='text-accent'>sincere</strong>，表里如一不虚假。真心换得真情在，生活处处有花开～"
      },
      {
        word: "courageous",
        phonetic: "/kəˈreɪdʒəs/",
        partOfSpeech: "adj. 勇敢的，有胆量的",
        example: "It was courageous of her to speak out.",
        exampleCn: "她敢于直言不讳，真是勇敢。",
        mixed: "消防员们都是<strong class='text-secondary'>courageous</strong>的英雄，他们在危险面前总是<strong class='text-secondary'>courageous</strong>地冲在前面。拥有<strong class='text-secondary'>courageous</strong>的品质，能让我们克服恐惧，面对挑战。",
        rap: "勇敢无畏<strong class='text-accent'>courageous</strong>，危难时刻不退缩。挺身而出显担当，英雄本色永流传～"
      },
      {
        word: "modest",
        phonetic: "/ˈmɑːdɪst/",
        partOfSpeech: "adj. 谦虚的，谦逊的",
        example: "He is successful but remains modest.",
        exampleCn: "他很成功但仍然很谦虚。",
        mixed: "李教授虽然学识渊博，但为人非常<strong class='text-secondary'>modest</strong>，总是<strong class='text-secondary'>modest</strong>地向别人学习。保持<strong class='text-secondary'>modest</strong>，能让我们不断进步，赢得更多尊重。",
        rap: "谦虚谨慎<strong class='text-accent'>modest</strong>，不骄不躁向前行。学海无涯勤作舟，虚怀若谷方进步～"
      }
    ];
    
    // 当前单词索引
    let currentIndex = 0;
    
    // DOM元素
    const wordElement = document.getElementById('word');
    const phoneticElement = document.getElementById('phonetic');
    const partOfSpeechElement = document.getElementById('part-of-speech');
    const exampleElement = document.getElementById('example-sentence');
    const mixedElement = document.getElementById('mixed-sentence');
    const rapElement = document.getElementById('rap-sentence');
    const counterElement = document.getElementById('word-counter');
    const prevBtn = document.getElementById('prev-btn');
    const nextBtn = document.getElementById('next-btn');
    const infoBtn = document.getElementById('info-btn');
    const infoModal = document.getElementById('info-modal');
    const closeModal = document.getElementById('close-modal');
    const gotItBtn = document.getElementById('got-it-btn');
    const wordCard = document.getElementById('word-card');
    
    // 初始化页面
    function init() {
      updateWordCard();
      setupEventListeners();
    }
    
    // 更新单词卡片内容
    function updateWordCard() {
      const wordData = vocabularyList[currentIndex];
      
      // 添加动画效果
      wordCard.classList.add('opacity-0', 'scale-95');
      
      setTimeout(() => {
        wordElement.textContent = wordData.word;
        phoneticElement.textContent = wordData.phonetic;
        partOfSpeechElement.textContent = wordData.partOfSpeech;
        exampleElement.textContent = wordData.example;
        // 更新例句中文翻译，移除括号
        const exampleTranslation = document.getElementById('example-translation');
        exampleTranslation.textContent = wordData.exampleCn.replace(/[()]/g, '');
        mixedElement.innerHTML = wordData.mixed;
        rapElement.innerHTML = `<p>${wordData.rap}</p>`;
        counterElement.textContent = `${currentIndex + 1}/${vocabularyList.length}`;
        
        // 更新按钮状态
        prevBtn.disabled = currentIndex === 0;
        
        // 检查是否是最后一个单词
        if (currentIndex === vocabularyList.length - 1) {
          nextBtn.innerHTML = '返回<i class="fa fa-arrow-right ml-2"></i>';
        } else {
          nextBtn.innerHTML = '下一个<i class="fa fa-arrow-right ml-2"></i>';
        }
        
        // 移除动画类以显示元素
        wordCard.classList.remove('opacity-0', 'scale-95');
      }, 200);
    }
    
    // 朗读单词
    function speakWord() {
      const word = vocabularyList[currentIndex].word;
      speakText(word);
    }
    
    // 朗读例句
    function speakExample() {
      const example = vocabularyList[currentIndex].example;
      speakText(example);
    }
    
    // 朗读洗脑记忆内容
    function speakMixedSentence() {
      const mixedSentence = document.getElementById('mixed-sentence').innerText;
      speakText(mixedSentence, 'zh-CN'); // 使用中文语音播放混合内容
    }
    
    // 朗读Rap记忆内容
    function speakRapSentence() {
      const rapSentence = document.getElementById('rap-sentence').innerText;
      speakText(rapSentence, 'zh-CN'); // 使用中文语音播放Rap内容
    }
    
    // 文本朗读功能
    function speakText(text, lang = 'en-US') {
      // 停止任何正在进行的朗读
      window.speechSynthesis.cancel();
      
      // 创建新的语音实例
      const utterance = new SpeechSynthesisUtterance(text);
      utterance.lang = lang;
      utterance.rate = 0.9; // 稍微放慢速度
      
      // 播放语音
      window.speechSynthesis.speak(utterance);
    }
    
    // 切换到上一个单词
    function prevWord() {
      if (currentIndex > 0) {
        currentIndex--;
        updateWordCard();
      }
    }
    
    // 切换到下一个单词或返回第一个单词
    function nextWord() {
      if (currentIndex < vocabularyList.length - 1) {
        currentIndex++;
      } else {
        // 如果是最后一个单词，返回第一个
        currentIndex = 0;
      }
      updateWordCard();
    }
    
    // 显示信息弹窗
    function showInfoModal() {
      infoModal.classList.remove('hidden');
      // 添加动画效果
      const modalContent = infoModal.querySelector('div');
      modalContent.classList.add('scale-95', 'opacity-0');
      setTimeout(() => {
        modalContent.classList.remove('scale-95', 'opacity-0');
        modalContent.classList.add('scale-100', 'opacity-100', 'transition-all', 'duration-300');
      }, 10);
    }
    
    // 隐藏信息弹窗
    function hideInfoModal() {
      const modalContent = infoModal.querySelector('div');
      modalContent.classList.remove('scale-100', 'opacity-100');
      modalContent.classList.add('scale-95', 'opacity-0', 'transition-all', 'duration-300');
      
      setTimeout(() => {
        infoModal.classList.add('hidden');
      }, 300);
    }
    
    // 设置事件监听器
    function setupEventListeners() {
      prevBtn.addEventListener('click', prevWord);
      nextBtn.addEventListener('click', nextWord);
      infoBtn.addEventListener('click', showInfoModal);
      closeModal.addEventListener('click', hideInfoModal);
      gotItBtn.addEventListener('click', hideInfoModal);
      
      // 键盘导航
      document.addEventListener('keydown', (e) => {
        if (e.key === 'ArrowLeft') prevWord();
        if (e.key === 'ArrowRight') nextWord();
      });
    }
    
    // 初始化应用
    document.addEventListener('DOMContentLoaded', init);
  </script>
</body>
</html>
