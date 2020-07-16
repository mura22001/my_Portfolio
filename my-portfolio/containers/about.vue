<template>
  <section id="about" class="about-wrapper">
    <pageTitle title="About" />
    <div class="box-wrapper">
      <table>
        <tbody>
          <tr v-for="(contact, index) in contacts" :key="index">
            <th>{{ contact.key }}</th>
            <td v-if="contact.url" class="last-td">
              <a :href="contact.url" target="_blank" rel="noopener noreferrer">
                {{ contact.value }}
              </a>
            </td>
            <td v-else class="last-td">
              {{ contact.value }}
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>
</template>

<script>
import pageTitle from '@/components/pageTitle'

export default {
  name: 'About',
  components: {
    pageTitle,
  },
  data() {
    return {
      contacts: [
        { key: 'Name', value: '村橋　達明 (Tatsuaki Murahashi)', url: '' },
        { key: 'University', value: '岐阜大学大学院　工学研究科　応用情報学専攻', url: '' },
        {
          key: 'GitHub',
          value: 'mura22001',
          url: 'https://github.com/mura22001',
        },
      ],
    }
  },
}
</script>

<style scoped>
.about-wrapper {
  text-align: left;
  display: flex;
  flex-wrap: wrap;
  padding: 60px 12vw;
  justify-content: center;
    &:last-child{
    border-bottom:none;
  }

  @media (max-width: 1250px) {
    padding: 30px 60px;
    border:none;
  }

  @media (max-width: 670px) {
    padding: 30px;
  }
}

.box-wrapper {
  display: flex;
  margin: 0;
  flex-wrap: wrap;

  width: 100%;
  justify-content:center;
  color: #343434;

  table {
    text-align: left;
  }

  th {
    padding-right: 20px;
    font-weight: normal;
    color: rgba(40, 40, 40, 0.8);
  }

  td {
    font-size: 20px;
    padding: 5px 8px 5px 0;
  }
}

a {
  text-decoration: none;
  text-align: left;
}

/*スマートフォン*/
@media (max-width: 670px) {
  .box-wrapper {
    td {
      display: block;
      font-size: 16px;
      width: 100%;
      padding: 5px 0;
      border-bottom: none;
    }
  }
}
</style>
