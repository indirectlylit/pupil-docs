---
description: Pupil Invisible and Pupil Cloud documentation ranging from getting started guides to explanations of advanced concepts, how-to guides, and references on export formats and APIs.
---
# Pupil Invisible & Cloud Documentation
Welcome to the Pupil Invisible & Pupil Cloud docs! In this section of the docs you will learn everything there is to learn about the Pupil Invisible ecosystem. Start by making your first recording and proceed all the way to implementing advanced applications. Everything you need is here.

## Getting Started
This section is for new users who want to get to grips with the tools. Working through the tutorials will put you in a great position to follow along with the rest of the documentation and get started with your project.

<div>
  <div class="grid grid-cols-1 sm-grid-cols-2 md-grid-cols-3 lg-grid-cols-2 xl-grid-cols-3 gap-8">
    <div v-for="(item,index) in gettingStarted">
      <v-img class="rounded" style="margin-bottom:32px;" :src="require(`../media/invisible/overview-${index + 1}.jpg`)"></v-img>
      <p class="caption--1 font-weight-bold pb-3">{{ item.title }}</p>
      <p class="caption--1">
        {{ item.text }}
      </p>
    </div>
  </div>
</div>

<router-link class="underline" to="/invisible/getting-started/first-recording">View more</router-link>

<v-divider />

## Explainers
This section explains all relevant concepts in detail and provides background information on how everything works. If you want to understand a certain aspect in detail, check out the respective section here.

Examples that might interest you are an overview of all the [available data streams](/invisible/explainers/data-streams) generated by Pupil Invisible and Pupil Cloud, or a detailed description on one of the available [Enrichments](/invisible/explainers/enrichments).

<div class="pb-4">
  <v-btn
    v-for="(item,index) in explainers"
    :key="index"
    outline
    round
    color="primary"
    :to="item.link"
    style="font-weight:normal;border-color"
  >
    {{ item.title }}
  </v-btn>
</div>

<router-link class="underline" to="/invisible/explainers/basic-concepts/">View more</router-link>

<v-divider />

## How-Tos
This section contains a range of how-tos that address specific topics and challenges.

<div class="howto-container">
  <v-expansion-panel v-model="panel">
    <v-expansion-panel-content
      v-for="(item, index) in panelContent"
      :key="index"
      hide-actions
    >
      <template v-slot:header>
        <div class="flex">
          <div style="width:16px;margin-right:8px">{{ panel == index ? '-' : '+' }}</div>
          <span>{{ item.title }}</span>
        </div>
      </template>
      <v-card>
        <v-card-text class="pt-0 pl-5">
          <div class="pb-2">
            {{ item.text }}
          </div>
          <router-link class="underline" :to="item.link">Read more</router-link>
        </v-card-text>
      </v-card>
    </v-expansion-panel-content>
  </v-expansion-panel>
</div>

<v-divider />

## Reference
This section is where you will find reference for [export formats](/invisible/reference/export-formats), which you can consult when working with any data coming out of Pupil Cloud.

It also contains a full API reference for the [real-time API client](https://pupil-labs-realtime-api.readthedocs.io/en/stable/api/index.html).

<router-link class="underline" to="/invisible/reference/export-formats">Jump to section</router-link>

<v-divider />

## Troubleshooting
Having trouble with Pupil Invisible or Pupil Cloud? We have collected the most common issues you may run into together with solutions in [this](/invisible/troubleshooting) section.

<router-link class="underline" to="/invisible/troubleshooting">Jump to section</router-link>

<script>
export default {
  data() {
    return {
      panel: null,
      gettingStarted: [
        {
          title: "Make Your First Recording",
          text: "Using your Pupil Invisible eye tracking system for the first time? Follow these steps to make your first recording!",
        },
        {
          title: "Understand The Ecosystem",
          text: "The Pupil Invisible ecosystem contains a range of tools that support you during data collection and data analysis. Learn more about all the tools available to power your eye tracking research!",
        },
        {
          title: "Analyse Recordings in Pupil Cloud",
          text: "This guide shows you how to go from newly uploaded Pupil Invisible recordings to enriched data ready for analysis and download using Pupil Cloud.",
        }
      ],
      panelContent: [
        {
          title: "Monitor your Data Collection in Real-Time",
          text: "All data generated by Pupil Invisible can be monitored in real-time using the Pupil Invisible Monitor app. To access the app simply visit pi.local in your browser while being connected to the same WiFi network as your Companion Device.",
          link: "/invisible/how-tos/data-collection-with-the-companion-app/monitor-your-data-collection-in-real-time",
        },
        {
          title: "Exchange the Lenses of Pupil Invisible glasses",
          text: "You can easily change the lenses of your Pupil Invisible glasses. You can swap to the shaded lenses (included with every Pupil Invisible system) or if you purchased the accessory prescription lens kit.",
          link: "/invisible/how-tos/pupil-invisible-glasses/exchange-lenses",
        },
        {
          title: "Introduction to the Real-Time API",
          text: "All data generated by Pupil Invisible is accessible to developers in real-time via our Real-Time API. Follow this how-to article to learn how to use the Real-Time API with our Python client.",
          link: "/invisible/how-tos/integrate-with-the-real-time-api/introduction/",
        },
      ],
      explainers: [
        {
          title: "Gaze",
          link: "/invisible/explainers/data-streams/#gaze",
        },
        {
          title: "Fixations",
          link: "/invisible/explainers/data-streams/#fixations",
        },
        {
          title: "Wearers",
          link: "/invisible/explainers/basic-concepts/#wearers",
        },
        {
          title: "Templates",
          link: "/invisible/explainers/basic-concepts/#templates",
        },
        {
          title: "Enrichments",
          link: "/invisible/explainers/enrichments",
        },
        {
          title: "Publications",
          link: "/invisible/explainers/publications",
        },
      ]
    };
  },
}
</script>
