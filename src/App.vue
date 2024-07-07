<template>
  <div class="relative flex h-screen bg-rustoreBlue">
    <!-- Основной контейнер чата -->
    <div
      class="flex flex-col flex-1 max-w-4xl mx-auto border border-gray-300 rounded-lg shadow-lg bg-white"
    >
      <!-- Плашка для выбора версий и логотип Rustore -->
      <div class="p-4 flex items-center justify-between">
        <div class="flex items-center">
          <h2 class="text-lg font-bold text-black mr-2">Выберите версию</h2>
          <div class="relative">
            <button @click="showMenu = !showMenu" class="flex items-center focus:outline-none">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="w-6 h-6"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
            </button>
            <div
              v-if="showMenu"
              class="absolute right-0 mt-2 w-36 bg-white border border-gray-300 rounded-lg shadow-lg py-2"
            >
              <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-200">
                Версия 1
              </a>
              <a href="#" class="block px-4 py-2 text-sm text-gray-700 hover:bg-gray-200">
                Версия 2
              </a>
            </div>
          </div>
        </div>
        <a href="https://www.rustore.ru/" target="_blank">
          <svg
            width="144"
            height="36"
            viewBox="0 0 144 36"
            class="h-12 ml-4 hover:opacity-75"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              clip-rule="evenodd"
              d="M17.28 36C9.13414 36 5.0612 36 2.5306 33.4694C-2.23137e-07 30.9388 -4.02706e-07 26.8658 -7.61841e-07 18.7199L-8.25329e-07 17.2799C-1.18446e-06 9.134 -1.36403e-06 5.06105 2.5306 2.53046C5.0612 3.59535e-06 9.13413 3.41884e-06 17.28 3.06582e-06L17.28 3.06581e-06L18.72 3.00341e-06L18.72 3.00341e-06C26.8659 2.65038e-06 30.9388 2.47387e-06 33.4694 2.53046C36 5.06105 36 9.134 36 17.2799L36 18.7199C36 26.8658 36 30.9388 33.4694 33.4694C30.9388 36 26.8659 36 18.72 36L17.28 36Z"
              fill="#0077FF"
            />
            <path
              d="M20.818 22.1855C19.8481 21.9432 19.168 21.0756 19.168 20.0805L19.168 8.35681C19.168 7.22652 20.236 6.39756 21.3377 6.67277L28.3144 8.41557C29.2843 8.65786 29.9644 9.5255 29.9644 10.5206L29.9644 22.2443C29.9644 23.3746 28.8963 24.2035 27.7947 23.9283L20.818 22.1855Z"
              fill="white"
            />
            <path
              d="M7.68519 27.5844C6.71525 27.3421 6.03516 26.4745 6.03516 25.4794L6.03516 13.7557C6.03516 12.6254 7.1032 11.7965 8.20488 12.0717L15.1815 13.8145C16.1515 14.0568 16.8316 14.9244 16.8316 15.9195L16.8316 27.6432C16.8316 28.7735 15.7635 29.6024 14.6618 29.3272L7.68519 27.5844Z"
              fill="white"
            />
            <path
              d="M14.2516 24.8852C13.2817 24.6429 12.6016 23.7753 12.6016 22.7802L12.6016 11.0565C12.6016 9.92621 13.6696 9.09724 14.7713 9.37245L21.7479 11.1153C22.7179 11.3575 23.398 12.2252 23.398 13.2203L23.398 24.944C23.398 26.0743 22.3299 26.9032 21.2283 26.628L14.2516 24.8852Z"
              fill="white"
            />
            <path
              d="M18.8164 26.0288C18.5109 25.951 18.2934 25.6808 18.2827 25.3657L17.9792 16.4124C17.8914 15.2275 17.0118 14.285 16.0926 14.0075C16.041 13.9919 15.9859 14.0129 15.9554 14.0573C15.9243 14.1024 15.9363 14.1649 15.9796 14.1984C16.2066 14.3741 16.8313 14.9475 16.8313 15.9366L16.8295 25.5253L18.8164 26.0288Z"
              fill="#0077FF"
            />
            <path
              d="M25.3828 23.3271C25.0776 23.2507 24.8599 22.9813 24.8492 22.6669L24.5456 13.7142C24.4579 12.5292 23.5782 11.5868 22.659 11.3092C22.6074 11.2937 22.5523 11.3147 22.5218 11.3591C22.4907 11.4042 22.5027 11.4666 22.546 11.5002C22.773 11.6759 23.3978 12.2493 23.3978 13.2383L23.3959 22.8303L25.3828 23.3271Z"
              fill="#0077FF"
            />
            <path
              d="M56.7238 20.6814C59.45 19.9864 61.2415 17.9013 61.2415 15.1727C61.2415 11.8005 58.5413 9.43222 54.7506 9.43222H48V27.5803H51.1156V20.9131H53.3226L58.1518 27.5803H61.8127L56.7238 20.6814ZM54.7506 12.2638C56.6978 12.2638 58.0479 13.448 58.0479 15.1727C58.0479 16.8974 56.6978 18.0815 54.7506 18.0815H51.1156V12.2638H54.7506Z"
              fill="#222222"
            />
            <path
              d="M68.8247 27.8377C70.4604 27.8377 71.9663 26.9882 72.8231 25.5724L73.4203 27.5803H75.6531V14.1945H72.6673V21.9428C72.6673 23.8477 71.3951 25.1863 69.6555 25.1863C67.9419 25.1863 66.7476 23.8477 66.7476 21.9428V14.1945H63.7618V22.2774C63.7618 25.4952 65.9427 27.8377 68.8247 27.8377Z"
              fill="#222222"
            />
            <path
              d="M85.182 27.8377C88.6352 27.8377 91.4912 25.8813 91.4912 22.6378C91.4912 19.0082 88.5054 17.9528 85.935 17.0776C83.9358 16.4083 82.1962 15.7905 82.1962 14.1687C82.1962 12.7529 83.5203 12.0064 85.0782 12.0064C86.7139 12.0064 87.8822 12.8559 88.5313 14.2974L91.4912 13.8084C90.5565 10.9767 88.1938 9.1748 84.9743 9.1748C81.651 9.1748 79.0027 11.0797 79.0027 14.3232C79.0027 17.9785 81.9885 18.9825 84.5589 19.832C86.5321 20.4755 88.2977 21.0933 88.2977 22.7408C88.2977 24.1823 86.9735 25.0061 85.208 25.0061C83.1828 25.0061 82.0923 24.0536 81.1317 22.3289L78.1199 22.8438C79.0027 25.9071 81.8067 27.8377 85.182 27.8377Z"
              fill="#222222"
            />
            <path
              d="M99.6138 25.0061C98.6012 25.0061 98.1079 24.517 98.1079 23.5131V16.7687H102.132V14.1945H98.1079V10.3332H95.875L95.122 14.1945H92.9151V16.7687H95.122V23.5131C95.122 26.1387 96.6539 27.5803 99.6138 27.5803H102.132L102.392 25.0061H99.6138Z"
              fill="#222222"
            />
            <path
              d="M110.924 27.8377C115.156 27.8377 118.142 24.9546 118.142 20.8874C118.142 16.8202 115.156 13.9371 110.924 13.9371C106.692 13.9371 103.706 16.8202 103.706 20.8874C103.706 24.9546 106.692 27.8377 110.924 27.8377ZM110.924 25.1348C108.484 25.1348 106.822 23.4101 106.822 20.8874C106.822 18.3647 108.484 16.64 110.924 16.64C113.365 16.64 115.026 18.3647 115.026 20.8874C115.026 23.4101 113.365 25.1348 110.924 25.1348Z"
              fill="#222222"
            />
            <path
              d="M123.724 27.5803V19.6775C123.724 17.9785 124.555 17.0261 126.372 17.0261H128.086L127.826 14.1945H127.255C125.671 14.1945 124.451 14.6321 123.542 16.1251L122.971 14.1945H120.738V27.5803H123.724Z"
              fill="#222222"
            />
            <path
              d="M142.778 20.7329C142.778 16.8716 139.87 13.9371 135.767 13.9371C131.665 13.9371 128.757 16.8459 128.757 20.8874C128.757 24.9289 131.665 27.8377 135.767 27.8377C138.571 27.8377 141.22 26.5249 142.232 23.9764L139.428 23.5131C138.779 24.4655 137.533 25.1348 135.949 25.1348C133.664 25.1348 132.158 23.7447 131.873 21.6854H142.726C142.752 21.4022 142.778 21.0933 142.778 20.7329ZM135.767 16.5113C137.637 16.5113 139.039 17.6954 139.532 19.3686H132.055C132.548 17.6439 133.95 16.5113 135.767 16.5113Z"
              fill="#222222"
            />
          </svg>
        </a>
      </div>

      <div class="flex-1 p-4 overflow-y-auto bg-gray-50">
        <div v-for="(message, index) in messages" :key="message.id" class="mb-4 flex items-start">
          <div v-if="message.user" class="flex items-center ml-auto">
            <span class="inline-block bg-gray-300 text-gray-800 py-2 px-4 rounded-lg shadow-sm">
              {{ message.text }}
            </span>
            <img
              src="@/assets/path_to_user_icon.png"
              alt="Пользователь"
              class="w-8 h-8 rounded-full ml-2 shadow-sm"
            />
          </div>
          <div v-else class="flex items-start">
            <img
              v-if="!message.typing"
              src="@/assets/path_to_bot_icon.png"
              alt="Бот"
              class="w-8 h-8 rounded-full mr-2 shadow-sm"
            />
            <div>
              <span
                v-if="!message.typing"
                class="inline-block bg-blue-500 text-white py-2 px-4 rounded-lg shadow-sm"
              >
                {{ message.text }}
              </span>
              <span
                v-else
                class="inline-block bg-blue-500 text-white py-2 px-4 rounded-lg shadow-sm"
              >
                Бот печатает...
              </span>
              <div v-if="message.links && message.links.length" class="mt-2">
                <div v-for="(link, linkIndex) in message.links" :key="linkIndex" class="mt-1">
                  <a
                    :href="link"
                    target="_blank"
                    class="inline-flex items-center text-sm text-blue-600 hover:underline"
                  >
                    {{ link }}
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="p-4 border-t border-gray-300 bg-white flex items-center ml-2">
        <input
          v-model="input"
          @keyup.enter="sendMessage"
          type="text"
          placeholder="Написать сообщение..."
          class="w-full p-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500"
        />
        <div class="flex items-center ml-2">
          <button
            @click="sendMessage"
            title="Отправить сообщение"
            class="ml-2 p-2 bg-blue-500 text-white rounded-full flex items-center justify-center shadow-lg hover:bg-blue-700 focus:outline-none focus:ring-2 focus:ring-blue-700"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-6 h-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M5 12h14M12 5l7 7-7 7"
              />
            </svg>
          </button>
          <button
            @click="clearHistory"
            title="Очистить чат"
            class="ml-2 p-2 bg-gray-300 text-black rounded-full flex items-center justify-center shadow-lg hover:bg-gray-400 focus:outline-none focus:ring-2 focus:ring-gray-300"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              class="w-6 h-6"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M19 7l-.867 12.142A2 2 0 0116.138 21H7.862a2 2 0 01-1.995-1.858L5 7m5 4v6m4-6v6m1-10V4a1 1 0 00-1-1h-4a1 1 0 00-1 1v3M4 7h16"
              />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import '@/assets/vksansdisplay-medium.css'
import axios from 'axios'
import { v4 as uuidv4 } from 'uuid'

export default {
  data() {
    return {
      showMenu: false,
      messages: [
        {
          id: uuidv4(),
          text: 'Привет, это QnA бот RuStore – система по технической документации. Задавай мне вопросы, я с радостью отвечу!',
          user: false,
          links: ['https://www.rustore.ru/help/']
        }
      ],
      input: ''
    }
  },
  methods: {
    mounted() {
      const storedMessages = JSON.parse(localStorage.getItem('chatHistory'))
      if (storedMessages) {
        this.messages = storedMessages
      }
    },
    clearHistory() {
      if (confirm('Вы уверены, что хотите очистить чат?')) {
        this.messages = []
        localStorage.removeItem('chatHistory')
      }
    },

    async sendMessage() {
      if (this.input.trim() === '') return
      const userMessage = { id: uuidv4(), text: this.input, user: true }
      this.messages.push(userMessage)
      this.input = ''

      const botTyping = {
        id: uuidv4(),
        text: '',
        user: false,
        typing: true,
        relatedTo: userMessage.id
      }
      this.messages.push(botTyping)

      try {
        const response = await axios.post('http://localhost:8000/help_bot', {
          query: userMessage.text
        })
        this.messages = this.messages.map((msg) => {
          if (msg.id === botTyping.id) {
            return { ...msg, text: response.data.answer, typing: false, links: [response.data.url] }
          }
          return msg
        })
      } catch (error) {
        this.messages = this.messages.map((msg) => {
          if (msg.id === botTyping.id) {
            return { ...msg, text: 'Ошибка связи с сервером.', typing: false }
          }
          return msg
        })
      }
      localStorage.setItem('chatHistory', JSON.stringify(this.messages))
    }
  }
}
</script>
