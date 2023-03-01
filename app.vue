<template>
  <div class="container mx-auto p-4">
    <h1 class="text-3xl font-bold mb-4">My Profile</h1>
    <div class="flex mb-4">
      <div class="w-1/3">
        <img :src="profilePic" alt="Profile image" class="rounded-lg">
      </div>
      <div class="w-2/3 px-4">
        <h2 class="text-xl font-bold mb-2">Brandon Chew Wui Pin</h2>
        <h2 class="text-xl font-bold mb-2">IQI Realty - PRO Niaga Store on Mudah.my</h2>
        <p class="text-gray-600 mb-2">REN: 33756</p>
        <p class="mb-4">REN 33756 We are specialize in New Property Project Marketing, Subsales and Land Banking and Land Planning for Investments. https://www.mudah.my/brandonchew</p>
        <a href="tel:+0161278623" class="text-blue-500">Contact me</a>

      </div>
    </div>
    <div class="container mx-auto py-4">
    <h1 class="text-3xl font-bold mb-4">Property Listings</h1>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <div v-for="property in properties" :key="property.id">
        <div class="bg-white shadow-md rounded-md overflow-hidden">
          <div class="p-4">
            <h2 class="text-xl font-bold mb-2">{{ property.title }}</h2>
            <div class="font-bold text-lg mb-2">RM {{ property.price }}</div>
            <div class="text-gray-600 mb-2">{{ property.date }}</div>
            <div class="text-gray-600 mb-2">{{ property.location }}</div>
            <div class="text-gray-600 mb-2">{{ property.type }}</div>
            <div class="text-gray-600">{{ property.size }}</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
import profilePic from '~/assets/img/profile.jpg';
export default {
  data() {
    return {
      profilePic,
      properties: [
        {
          id: 1,
          title: "Wisma Hopoh Jalan P.Ramlee Retail For Sale",
          price: "360 000",
          date: "Today, 18:45",
          location: "Kuching",
          propertyType: "Commercial Property",
          size: "288 sq.ft",
          tenure: "Leasehold",
          details: "Retail space"
        },
        {
          id: 2,
          title: "Semi-D House for Sale in PJ",
          price: "1 200 000",
          date: "Yesterday, 13:00",
          location: "Petaling Jaya",
          propertyType: "Residential Property",
          size: "3000 sq.ft",
          tenure: "Freehold",
          details: "4 bedrooms, 3 bathrooms"
        },
        {
          id: 3,
          title: "Office Space for Rent in KLCC",
          price: "12 000",
          date: "2 days ago",
          location: "Kuala Lumpur",
          propertyType: "Commercial Property",
          size: "1000 sq.ft",
          tenure: "Leasehold",
          details: "High floor with great view"
        }
      ]
    };
  }
};
</script>
