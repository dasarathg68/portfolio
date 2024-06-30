<template>
  <div class="mt-24">
    <h1 class="text-4xl font-bold text-center mb-8">Timeline</h1>
    <div class="flex justify-center">
      <ul
        class="timeline timeline-snap-icon max-md:timeline-compact timeline-vertical timeline-end"
      >
        <li v-for="item in timelineItems" :key="item.period">
          <div :class="`timeline-${item.position} mb-10 text-${item.position}`">
            <time class="font-mono italic text-gray-600">{{ item.period }}</time>
            <div class="text-lg font-black mb-2">{{ item.title }}</div>
            <div class="text-md font-semibold mb-1">{{ item.location }}</div>
            <div class="text-justify text-gray-800">{{ item.description }}</div>
            <div v-if="item.achievements" class="mt-2">
              <ul class="list-disc pl-5 text-gray-700">
                <li v-for="achievement in item.achievements" :key="achievement">
                  {{ achievement }}
                </li>
              </ul>
            </div>
          </div>
          <hr />
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
const timelineItems = [
  {
    period: 'June 2019 - June 2023',
    title: 'SASTRA University',
    location: 'B.Tech. Electronics & Communication',
    description: 'CGPA: 8.3575/10',
    achievements: [
      'Dean’s Merit List (Top 3-10% in the university) in the academic year 2019-2020',
      'Finalist in Evathon 2021, University of Limerick, Ireland',
      'Recipient of the Desh-Videsh scholarship'
    ],
    position: 'start'
  },
  {
    period: 'April 2022 - June 2022',
    title: 'Embedded SW Developer Intern',
    location: 'Analog Devices India, Bengaluru (Remote)',
    description:
      "Worked as a summer intern and gained insights about BMS, embedded software, and isoSPI. I completed a project titled 'Source Meter Control Automation & Complex Device Drivers (CDD).'",
    position: 'end'
  },
  {
    period: 'February 2023 - June 2023',
    title: 'R&D Intern',
    location: 'Gerontechnology Research Center, Taiwan (Onsite)',
    description:
      'Developed an IoT backend using Gin-Gonic in Go, managing users and devices. Assisted in Flutter feature development and built a dashboard for activity detection algorithms. My work contributed to our product rollout to over 250 customers.',
    achievements: [
      'Supported by the Taiwan Experience Education Program and Desh-Videsh Scholarship'
    ],
    position: 'start'
  },
  {
    period: 'April 2023 - January 2024',
    title: 'Lead Engineer',
    location: 'bEarly TechnoVations, Chennai (Hybrid)',
    description:
      "Developed paceB, a biomedical device for early-stage Parkinson's diagnosis. Optimized real-time data streaming by 13x. Built a patient management system with payment interface and IoT dashboard.",
    achievements: [
      "Published a patent titled 'A Device for Detection and Prognosis of Pathological Gait'",
      'Co-authored a white paper and led team members/interns'
    ],
    position: 'end'
  },
  {
    period: 'January 2024 - Present',
    title: 'Independent Contractor',
    location: '',
    description:
      'Completed over 10 projects covering IoT, Web3, Full Stack Development, and patent writing. Achieved a perfect Job Success Score of 100% on Upwork.',
    position: 'start'
  },
  {
    period: 'March 2024 - Present',
    title: 'Web3 Developer',
    location: 'Globe & Citizen, Canada (Remote)',
    description:
      'Building the CNC Portal, an app for financially acknowledging micro contributions of Open Source collaborators. Crafting user-friendly interfaces and handling backend development.',
    position: 'end'
  }
]
</script>
