<script>
    import logo from "../assets/sft_logo.svg"
    import {sftInfo} from "../scripts/store.js";

    function showSftInfo() {
        sftInfo.set(true)
    }

    function hideSftInfo() {
        sftInfo.set(false)
    }

    export let path = "/"
</script>
<div id="Main"
     class="{$sftInfo ? 'flex justify-start items-start h-screen bg-white flex-col navigation relative'
     : 'flex justify-start items-start h-screen bg-white flex-col navigation relative rounded-tr-3xl'}">
  <div class="flex justify-center items-center w-full space-x-3 logo-container">
    <a href="/"><img src={logo} alt="logo" class="border-8 border-white rounded-full"/></a>
    {#if !$sftInfo}
      <div class="cursor-pointer absolute right-2 top-2" on:click={()=>showSftInfo()}>
        <svg width="24" height="25" viewBox="0 0 24 25" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M14 10.3999L19 5.1999M19 5.1999L19 10.3999M19 5.1999L14 5.1999" stroke="#9D9D9D" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M14 10.3999L19 5.1999M19 5.1999L19 10.3999M19 5.1999L14 5.1999" stroke="black" stroke-opacity="0.2"
                stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M10 14.5601L5 19.7601M5 19.7601L5 14.5601M5 19.7601H10" stroke="#9D9D9D" stroke-width="2"
                stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M10 14.5601L5 19.7601M5 19.7601L5 14.5601M5 19.7601H10" stroke="black" stroke-opacity="0.2"
                stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
    {/if}
  </div>
  <div class="mt-6 flex flex-col justify-start items-center w-full">
    <a href=""
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400 rounded py-2 text-nav font-semibold pl-5">
      <p class="text-base leading-5">SFT</p>
    </a>
    <a href="/"
       class:active={path==='/'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M2.77778 7.22222V15C2.77778 16.1046 3.67321 17 4.77778 17H9M2.77778 7.22222L8.29289 1.70711C8.68342 1.31658 9.31658 1.31658 9.70711 1.70711L14.5 6.5M2.77778 7.22222L1 9M15.2222 7.22222V15C15.2222 16.1046 14.3268 17 13.2222 17H9M15.2222 7.22222L17 9M15.2222 7.22222L14.5 6.5M14.5 6.5V3M9 17V12"
              stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">Home</p>
    </a>
    <a href="/mint"
       class:active={path==='/mint'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="19" height="10" viewBox="0 0 19 10" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M9.62695 9L9.62695 5M9.62695 1L9.62695 5M9.62695 5L1.62696 5M9.62695 5L17.627 5M1.62696 5L4.12696 7.5M1.62696 5L4.12695 2.5M17.627 5L15.127 2.5M17.627 5L15.127 7.5"
              stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">Mint/Redeem</p>
    </a>
    <a href="/members"
       class:active={path==='/members'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="16" height="19" viewBox="0 0 16 19" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M1 18V17C1 14.2386 3.23858 12 6 12H10C12.7614 12 15 14.2386 15 17V18M12 5C12 7.20914 10.2091 9 8 9C5.79086 9 4 7.20914 4 5C4 2.79086 5.79086 1 8 1C10.2091 1 12 2.79086 12 5Z"
              stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">Members</p>
    </a>
    <a href="/roles"
       class:active={path==='/roles'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="20" height="21" viewBox="0 0 20 21" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M1 18V17C1 14.2386 3.23858 12 6 12H9.75M14.5355 11.9645V15.5M14.5355 15.5V19.0355M14.5355 15.5H18.0711M14.5355 15.5H11M12 5C12 7.20914 10.2091 9 8 9C5.79086 9 4 7.20914 4 5C4 2.79086 5.79086 1 8 1C10.2091 1 12 2.79086 12 5Z"
              stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">SFT Roles</p>
    </a>
    <a href="/audits"
       class:active={path==='/audits'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="16" height="20" viewBox="0 0 16 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M5.34876 9.50002L7.34876 11.5L11.5 7.34878M7.72528 1.07852L1.72528 2.7928C1.29598 2.91546 1 3.30784 1 3.75432L1 8.85384C1 12.0834 2.55966 15.1141 5.18762 16.9912L7.41876 18.5849C7.76646 18.8332 8.23354 18.8332 8.58124 18.5849L10.8124 16.9912C13.4403 15.1141 15 12.0834 15 8.85384V3.75432C15 3.30784 14.704 2.91546 14.2747 2.7928L8.27472 1.07852C8.09517 1.02721 7.90483 1.02721 7.72528 1.07852Z"
              stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">Audits</p>
    </a>
    <a href="/asset-register"
       class:active={path==='/asset-register'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="16" height="20" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="4 2 16 20">
          <path
              d="M13.5 3H12H8C6.34315 3 5 4.34315 5 6V18C5 19.6569 6.34315 21 8 21H16C17.6569 21 19 19.6569 19 18V8.625M13.5 3L19 8.625M13.5 3V7.625C13.5 8.17728 13.9477 8.625 14.5 8.625H19"
              stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M9 13H15" stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          <path d="M9 17H15" stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">Asset Register</p>
    </a>
    <a href="/manual"
       class:active={path==='/manual'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="22" height="20" viewBox="0 0 22 20" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M11 4.05337V18.3025M4 6.25464C5.26578 6.45067 6.67778 6.77657 8 7.28788M4 10.2546C4.63949 10.3537 5.3163 10.4859 6 10.6584M2.99433 1.01127C5.21271 1.26195 8.19313 1.93632 10.3168 3.42445C10.725 3.71045 11.275 3.71045 11.6832 3.42445C13.8069 1.93632 16.7873 1.26195 19.0057 1.01127C20.1036 0.887209 21 1.80402 21 2.93518V14.2C21 15.3311 20.1036 16.2483 19.0057 16.3723C16.7873 16.623 13.8069 17.2974 11.6832 18.7855C11.275 19.0715 10.725 19.0715 10.3168 18.7855C8.19313 17.2974 5.21271 16.623 2.99433 16.3723C1.89642 16.2483 1 15.3311 1 14.2V2.93518C1 1.80402 1.89642 0.887209 2.99433 1.01127Z"
              stroke="#575757" stroke-width="2" stroke-linecap="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">Manual</p>
    </a>
  </div>
  <div class="items-center pt-16 border-b w-11/12 self-center"></div>
  <div class="mt-6 flex flex-col justify-start items-center w-full">
    <a href=""
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400 rounded py-2 text-nav font-semibold pl-5">
      <p class="text-base leading-5">Web 3</p>
    </a>
    <a href="/ipfs"
       class:active={path==='/ipfs'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path
              d="M18 10.6562V8.625C18 7.72754 17.2538 7 16.3333 7H4.66667C3.74619 7 3 7.72754 3 8.625V12.6875C3 13.585 3.74619 14.3125 4.66667 14.3125H9.5625M16.3333 15.125V13.5C16.3333 12.6025 15.5871 11.875 14.6667 11.875C13.7462 11.875 13 12.6025 13 13.5V15.125M12.1667 20H17.1667C17.6269 20 18 19.6362 18 19.1875V15.9375C18 15.4888 17.6269 15.125 17.1667 15.125H12.1667C11.7064 15.125 11.3333 15.4888 11.3333 15.9375V19.1875C11.3333 19.6362 11.7064 20 12.1667 20Z"
              stroke="#575757" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          <circle cx="6.5" cy="10.5" r="1.5" fill="#575757"/>
          <circle cx="11.5" cy="10.5" r="1.5" fill="#575757"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">IPFS</p>
    </a>
    <a href="/sft-setup"
       class:active={path==='/sft-setup'}
       class="flex jusitfy-start items-center space-x-6 w-full  focus:outline-none  focus:text-indigo-400  nav-item rounded py-2 font-bold pl-5">
      <div class="w-3">
        <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
          <circle cx="9" cy="9" r="8" stroke="#575757" stroke-width="2" stroke-linecap="round"
                  stroke-linejoin="round"/>
        </svg>
      </div>
      <p class="text-base leading-5  ">SFT Setup</p>
    </a>
  </div>
</div>
{#if ($sftInfo)}
  <div class="bg-white w-5/12 rounded-tr-3xl relative border-l">
    <div class="cursor-pointer absolute right-2 top-2" on:click={()=>hideSftInfo()}>
      <svg width="25" height="24" viewBox="0 0 25 24" fill="none" xmlns="http://www.w3.org/2000/svg">
        <path d="M5.96387 5L10.9731 10M10.9731 10V5M10.9731 10H5.96387" stroke="#9D9D9D" stroke-width="2"
              stroke-linecap="round" stroke-linejoin="round"/>
        <path d="M5.96387 5L10.9731 10M10.9731 10V5M10.9731 10H5.96387" stroke="black" stroke-opacity="0.2"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        <path d="M19.9902 19L14.981 14M14.981 14L14.981 19M14.981 14L19.9902 14" stroke="#9D9D9D" stroke-width="2"
              stroke-linecap="round" stroke-linejoin="round"/>
        <path d="M19.9902 19L14.981 14M14.981 14L14.981 19M14.981 14L19.9902 14" stroke="black" stroke-opacity="0.2"
              stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </div>
    <div class="flex flex-col py-5 px-9 ">
      <span class="font-bold self-center">Token Overview</span>
      <table class="w-8/12 leading-8 w-full mt-5 leading-10">
        <tr>
          <td class="font-bold">Token Name</td>
          <td class="sft-name">OPUS</td>
        </tr>
        <tr>
          <td class="font-bold">Token Symbol</td>
          <td class="sft-info">OPS</td>
        </tr>
        <tr>
          <td class="font-bold">Creation Date</td>
          <td class="sft-info">30/09/2022</td>
        </tr>
        <tr>
          <td class="font-bold">Number of holders</td>
          <td class="sft-info">3,000,000</td>
        </tr>
        <tr>
          <td class="font-bold">Token Supply</td>
          <td class="sft-info">123,000,000</td>
        </tr>
        <tr>
          <td class="font-bold">Name of Auditor(s)</td>
          <td class="sft-info">KPMG</td>
        </tr>
        <tr>
          <td class="font-bold">Name of issuer</td>
          <td class="sft-info">British Land</td>
        </tr>
      </table>
      <span class="font-bold">About</span>

    </div>
  </div>

{/if}

<style>

    .text-nav {
        color: #5F9AD1;
    }

    .nav-item {
        color: #575757;
    }

    .nav-item:hover {
        background: #ECECEC
    }

    .active {
        background: #CAE6FF;
    }

    .logo-container {
        margin-top: -30px;
    }

    .navigation {
        min-width: 203px;
        max-width: 203px;
    }
</style>
