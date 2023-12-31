<template>
    <div class="practice-areas">
      <div class="area" v-for="area in areas" :key="area.title">
        <img :src="area.image" :alt="area.title" class="area-image">
        <h2 class="area-title">{{ area.title }}</h2>
        <p class="area-description">{{ area.description1 }}</p>
        <p class="area-description">{{ area.description2 }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'PracticeAreas',
    data() {
      return {
        areas: [
  {
    title: 'Immigration Law',
    image: 'https://www.attorneygeneral.gov/wp-content/uploads/2020/03/CR_immigration_LG.jpg',
    description1: 'Our team of dedicated immigration attorneys is experienced in all aspects of immigration law. From assisting clients in obtaining visas, to handling complex deportation cases, our firm has the expertise necessary to navigate the often complicated U.S. immigration system.',
    description2: 'We believe in the importance of family reunification, the right to seek employment opportunities, and the ability to seek refuge from persecution. We are committed to providing exceptional service and results-oriented legal representation to clients from all over the world.',
  },
  {
    title: 'Criminal Law',
    image: 'https://edwardslawofficepc.com/wp-content/uploads/2019/05/criminal-law-plaque-ontable-with-gavel.jpg',
    description1: 'Our criminal law practice is dedicated to protecting the rights and interests of those accused of crimes. We handle a wide range of criminal cases, including DUI/DWI, drug offenses, theft crimes, violent crimes, white collar crimes, and more.',
    description2: 'We believe in the presumption of innocence and the right to a fair trial. Our experienced criminal defense attorneys are dedicated to providing aggressive, effective defense strategies tailored to the unique circumstances of each case.',
  },
  {
    title: 'Personal Injury Law',
    image: 'https://swartzlaw.com/wp-content/uploads/2021/12/Personal-Injury-Law-Firm-1.jpg',
    description1: 'Our personal injury lawyers are dedicated to helping individuals who have been injured due to the negligence or recklessness of others. We handle a variety of personal injury cases, including auto accidents, slip and fall accidents, medical malpractice, product liability, and wrongful death.',
    description2: 'We strive to obtain maximum compensation for our clients to cover medical expenses, loss of income, pain and suffering, and other damages. Our team provides compassionate and personalized legal representation, guiding our clients through each step of the legal process.',
  },
  {
    title: 'Business Law',
    image: 'https://www.broadviewsolicitorsllp.com/wp-content/uploads/2023/01/Business-Law-BVSLLP.jpg',
    description1: 'Our business law practice serves entrepreneurs, small businesses, and large corporations alike. We handle a broad spectrum of business-related issues, including business formation, contract drafting and negotiation, intellectual property protection, mergers and acquisitions, and dispute resolution.',
    description2: 'Our goal is to provide practical legal solutions that support our clients’ business objectives. We offer strategic advice and representation in both transactional matters and litigation, helping businesses navigate the complexities of the legal landscape.',
  },
  {
  title: 'Contract Law',
  image: 'https://media.istockphoto.com/id/1130476273/photo/signing-the-agreement-in-the-contract.jpg?s=612x612&w=0&k=20&c=NlA-eL5ELryzYJCG4HMRgliVG78gdYgw1bYyI_y9UdE=',
  description1: "Our contract law practice focuses on the drafting, negotiation, and enforcement of contracts in a variety of sectors. From business agreements to personal contracts, our team ensures that our clients' interests are protected and their obligations clearly defined.",
  description2: "We believe in the importance of a well-drafted contract as the foundation of any successful transaction or business relationship. Whether it's resolving contractual disputes or advising on complex contractual provisions, our attorneys bring a wealth of experience and insight to every contract-related challenge.",
},
],
      };
    },
  };
  </script>
  
  
  <style scoped>
.practice-areas {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  background-color: #001f3f;
  padding: 20px;
  padding-bottom: 100px; /* add padding bottom to ensure some visible background under the boxes */
  min-height: 100vh; /* Ensure full height of the viewport is used */
}

.area {
  flex: 1 0 300px;
  margin: 20px;
  padding: 20px;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  background-color: white;
  max-width: 800px;
}

.area-image {
  width: 100%;
  height: auto;
}

.area-title {
  font-size: 20px;
  font-weight: bold;
  margin-top: 20px;
}

.area-description {
  font-size: 16px;
  margin-top: 10px;
}

@media (max-width: 768px) {
  .practice-areas {
    flex-direction: column;
    align-items: center;
  }

  .area {
    flex-basis: 100%;
    max-width: 100%;
  }
}
</style>