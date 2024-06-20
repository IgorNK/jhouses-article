<script setup lang="ts">
  import { ref } from "vue";
  import ImageBlock from "../components/ImageBlock.vue";
  import QuoteBlock from "../components/QuoteBlock.vue";
  import Modal from "../components/Modal.vue";

  const isModalOpened = ref(false);

  const modalImage = ref("");

  const openModal = () => {
    isModalOpened.value = true;
  };

  const closeModal = () => {
    isModalOpened.value = false;
    modalImage.value = "";
  };

  const handleImageClick = (value: string) => {
    modalImage.value = value;
    openModal();
  }
</script>

<template>
  <div class="article-main">
    <h1 class="article-main__title">Японские традиционные дома</h1>
    
    <div class="article-main__text-block">
      <h2 class="article-main__subtitle">Минка, нока, матия</h2>
      <p class="article-main__text">Япония славится своей культурой и&nbspтрадициями, которые отражаются в&nbspархитектуре страны. Одним из&nbspнаиболее узнаваемых элементов японской архитектуры являются традиционные&nbspдома.</p>
      <p class="article-main__text"><span class="article-main__accent">Минка&nbsp</span>— традиционный японский дом. В&nbspузком смысле термин обозначает крестьянские дома, построенные вплоть до&nbspконца эпохи Эдо. В&nbspшироком смысле термин включает как крестьянские «<span class="article-main__accent">нока</span>», так и&nbspгородские дома «<span class="article-main__accent">матия</span>» того времени, а&nbspтакже дома, возведённые позже в&nbspтрадиционном стиле и&nbspтехнике.</p>
    </div>
    
    <div class="article-main__image-quote-container">
      <ImageBlock @click="handleImageClick" class="article-main__image-quote-container__image" src="src/assets/images/mak-oTHW-Gl9MPg-unsplash.jpg" alt="Интерьер традиционного японского дома" />
      <QuoteBlock class="article-main__quote"><p>В&nbspтрадиционных японских домах комнаты отделяются друг от&nbspдруга с&nbspпомощью раздвижных дверей, называемых «<span class="article-main__accent">фусума</span>». Это позволяет изменять конфигурацию помещения в&nbspзависимости от&nbspпотребностей&nbspхозяев.</p></QuoteBlock>
    </div>

    <div class="article-main__text-block">
      <h2 class="article-main__subtitle">Характерная форма</h2>
      <p class="article-main__text">Традиционные японские дома имеют характерную форму, которая называется «<span class="article-main__accent">минано</span>». Их отличает крыша, украшенная свисающими краями. Они часто строятся из дерева и имеют сложную систему каркаса, которая позволяет им выдерживать сильные&nbspземлетрясения.</p>
    </div>
  
    <div class="article-main__image-block-column">
      <ImageBlock @click="handleImageClick" src="src/assets/images/david-emrich-9a0S_8bU0lo-unsplash.jpg" alt="Японский сад, сочетающий естественность и&nbspтщательную проработку ландшафта" />
    </div>
  
    <div class="article-main__quote-block-centered">
      <QuoteBlock class="article-main__quote"><p>Основной пол земляной, над ним на&nbspвысоте около 50&nbspсм устанавливается деревянный настил, на&nbspкотором сидят, спят, принимают пищу.</p>
        <p>Часть дома имеет лишь глинобитные полы.</p>
        <p>В&nbspэтих частях обычно располагаются кухни или&nbspмастерские.</p></QuoteBlock>
    </div>
  
    <div class="article-main__image-block-column">
      <ImageBlock @click="handleImageClick" src="src/assets/images/julie-fader-I4plBnRzJ94-unsplash.jpg" alt="Вход в дом" />
    </div>
  
    <div class="article-main__text-block">
      <h2 class="article-main__subtitle">В&nbspгармонии с&nbspприродой</h2>
      <p class="article-main__text">В&nbspтаких домах используются только натуральные материалы: дерево, тростник и&nbspбумага. Такой подход позволяет создавать дома, которые гармонично сочетаются с&nbspокружающей природой, что является одним из&nbspфундаментальных принципов японской архитектуры. «Скелет» дома, крыши, стены и&nbspопоры делаются из&nbspдерева.</p>
      <p class="article-main__text">Типичный дом имеет от&nbsp3 до&nbsp6 комнат. Комнаты обычно располагаются вокруг центрального двора, который может быть украшен садом или&nbspпрудом.</p>
    </div>
  
    <div class="article-main__image-block-full">
      <ImageBlock @click="handleImageClick" src="src/assets/images/sava-bobov-24c1mCPTa0E-unsplash.jpg" alt="Интерьер традиционного японского дома. Раздвижные двери и низкий столик" />
    </div>
  
    <div class="article-main__quote-block-centered">
      <QuoteBlock class="article-main__quote"><p>Внутри домов можно увидеть «<span class="article-main__accent">татами</span>»&nbsp— традиционные японские ковры, «<span class="article-main__accent">футон</span>»&nbsp— матрасы для сна, «<span class="article-main__accent">шири&#8209;кавадзе</span>»&nbsp— традиционные японские шкафы, а&nbspтакже «<span class="article-main__accent">шодзи</span>»&nbsp— декоративные перегородки из&nbspбумаги и&nbspдерева.</p></QuoteBlock>
    </div>

    <div class="article-main__image-quote-container">
      <ImageBlock @click="handleImageClick" class="article-main__image-quote-container__image" src="src/assets/images/falco-negenman-K8MMfFifWcE-unsplash.jpg" alt="Японский сад" />
      <QuoteBlock class="article-main__quote"><p>Японские традиционные дома продолжают вдохновлять современных архитекторов по&nbspвсему миру. Многие современные здания сочетают в&nbspсебе элементы старинной японской архитектуры с&nbspсовременными технологиями и&nbspматериалами.</p></QuoteBlock>
    </div>

    <div class="article-main__image-block-full">
      <ImageBlock @click="handleImageClick" src="src/assets/images/xiaocong-yan-M9NTnUlNiEM-unsplash.jpg" alt="Интерьер дома" />
    </div>

    <div class="article-main__author-block">
      <p class="article-main__author-block__title">Автор статьи:</p>
      <p class="article-main__author-block__name">Александра Александрова</p>
    </div>
    
  </div>

  <Modal :isOpen="isModalOpened" @modal-close="closeModal" name="image">
    <template #content><img class="modal-image" :src="modalImage" alt="image" /></template>
  </Modal>
  
</template>

<style scoped>
  .article-main {
    margin: 0;
    padding: 0;
    margin-left: 100px;
    margin-right: 100px;
    margin-top: var(--padding-10);
    max-width: 100vw;
    display: flex;
    flex-direction: column;
    row-gap: var(--padding-10);
  }

  .article-main__text-block {
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    row-gap: var(--padding-5);
    width: calc(10/17 * 100%);
  }

  .article-main__image-quote-container {
    display: grid;
    grid-template-columns: minmax(0, 10fr) minmax(0, 6fr);
    grid-template-rows: min-content;
    align-items: center;
    column-gap: 73px;
    position: relative;
  }

  .article-main__image-quote-container__image {
    
  }

  .article-main__image-block-full {
    max-width: 100%;
  }

  .article-main__image-block-column {
    width: calc(10/17 * 100%);
  }

  .article-main__author-block {
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    font-family: var(--font-main);
    font-size: var(--font-size-description);
    line-height: var(--line-height-description);
  }

  .article-main__author-block__name {
    margin: 0;
    padding: 0;
    color: var(--color-text-primary);
  }

  .article-main__author-block__title {
    margin: 0;
    padding: 0;
    color: var(--color-text-secondary);    
  }

  .article-main__title {
    margin: 0;
    padding: 0;
    font-family: var(--font-title);
    color: var(--color-text-primary);
    font-size: var(--font-size-title);
    line-height: var(--line-height-title);
  }

  .article-main__subtitle {
    margin: 0;
    padding: 0;
    font-family: var(--font-title);
    color: var(--color-text-primary);
    font-size: var(--font-size-subtitle);
    line-height: var(--line-height-subtitle);
  }

  .article-main__text {
    margin: 0;
    padding: 0;
    font-family: var(--font-main);
    color: var(--color-text-primary);
    font-size: var(--font-size-main);
    line-height: var(--line-height-main);
  }

  .article-main__quote {
    font-family: var(--font-quote);
    color: var(--color-text-primary);
    font-size: var(--font-size-quote);
    line-height: var(--line-height-quote);
    font-weight: var(--font-weight-quote);
    font-style: italic;
  }

  .article-main__accent {
    color: var(--color-accent);
  }
  
  .article-main__quote p {
    margin: 0;
    padding: 0;
  }

  .modal-image {
    max-width: 100%;
    max-height: 80vh;
  }

  @media (max-width: 768px) {
    .article-main {
      margin-left: var(--padding-2);
      margin-right: var(--padding-2);
      margin-top: var(--padding-4);
      row-gap: var(--padding-4);
    }

    .article-main__text-block {
      row-gap: var(--padding-3);
      width: 100%;
    }

    .article-main__image-quote-container {
      display: flex;
      flex-direction: column;
      row-gap: var(--padding-4);
      max-width: 100%;
    }

    .article-main__image-quote-container__image {
      width: 100%;
    }

    .article-main__image-block-column {
      width: 100%;
    }

    .article-main__author-block {
      font-size: var(--font-size-description-mobile);
    }

    .article-main__title {
      font-size: var(--font-size-title-mobile);
    }

    .article-main__subtitle {
      font-size: var(--font-size-subtitle-mobile);
    }

    .article-main__text {
      font-size: var(--font-size-main-mobile);
    }

    .article-main__quote {
      font-size: var(--font-size-quote-mobile);
    }
    
  }
  
  
</style>