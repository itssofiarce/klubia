---  
title: Demo page
summary: Example page for mkdocs-shadcn users
new: true
description: Example page for mkdocs-shadcn users
keywords: mkdocs,shadcn,demo
author: asiffer
image: https://raw.githubusercontent.com/asiffer/mkdocs-shadcn/refs/heads/master/.github/assets/logo.svg
order: 5
sidebar_title: Demo
external_links:
  "API Reference": https://ui.shadcn.com/docs/components
  GitHub: "https://github.com/asiffer/mkdocs-shadcn"

#extra_javascript:
#  - js/custom-script.js

---

# Machine Learning Title

This is a test to see how the doucmentation will look like


!!! info "Information:"
    Something **new** is coming to `mkdocs-shadcn`

!!! note "Note:"
    We notice that `x=2`

!!! warning "Warning:"
    There is a *risk* doing `x/0`

!!! danger "Danger:"
    Don't look at `node_modules` **please**!


## Testing other extensions
/// echarts
    renderer: "canvas"
    attrs:
        style: "width:100%;height:60vh;"

const option = {
  tooltip: {
    trigger: "none",
    axisPointer: {
      type: "cross",
    },
  },
  legend: {},
  grid: {
    top: 70,
    bottom: 50,
  },
  xAxis: [
    {
      type: "category",
      axisTick: {
        alignWithLabel: true,
      },
      axisLine: {
        onZero: false,
      },
      axisPointer: {
        label: {
          formatter: function (params) {
            return (
              "Precipitation  " +
              params.value +
              (params.seriesData.length ? "：" + params.seriesData[0].data : "")
            );
          },
        },
      },
      data: [
        "2016-1",
        "2016-2",
        "2016-3",
        "2016-4",
        "2016-5",
        "2016-6",
        "2016-7",
        "2016-8",
        "2016-9",
        "2016-10",
        "2016-11",
        "2016-12",
      ],
    },
    {
      type: "category",
      axisTick: {
        alignWithLabel: true,
      },
      axisLine: {
        onZero: false,
      },
      axisPointer: {
        label: {
          formatter: function (params) {
            return (
              "Precipitation  " +
              params.value +
              (params.seriesData.length ? "：" + params.seriesData[0].data : "")
            );
          },
        },
      },
      data: [
        "2015-1",
        "2015-2",
        "2015-3",
        "2015-4",
        "2015-5",
        "2015-6",
        "2015-7",
        "2015-8",
        "2015-9",
        "2015-10",
        "2015-11",
        "2015-12",
      ],
    },
  ],
  yAxis: [
    {
      type: "value",
    },
  ],
  series: [
    {
      name: "Precipitation(2015)",
      type: "line",
      xAxisIndex: 1,
      smooth: true,
      emphasis: {
        focus: "series",
      },
      data: [
        2.6, 5.9, 9.0, 26.4, 28.7, 70.7, 175.6, 182.2, 48.7, 18.8, 6.0, 2.3,
      ],
    },
    {
      name: "Precipitation(2016)",
      type: "line",
      smooth: true,
      emphasis: {
        focus: "series",
      },
      data: [
        3.9, 5.9, 11.1, 18.7, 48.3, 69.2, 231.6, 46.6, 55.4, 18.4, 10.3, 0.7,
      ],
    },
  ],
};

///



### Keeping testing
### FAQ

/// details | Why copy/paste and not packaged as a dependency?
The idea behind this is to give you ownership and control over the code, allowing you to decide how the components are built and styled.

Start with some sensible defaults, then customize the components to your needs.

*One of the drawbacks of packaging the components in an npm package is that the style is coupled with the implementation. The design of your components should be separate from their implementation.*
///

/// details | Do you plan to publish it as an npm package?
No. I have no plans to publish it as an npm package.
///

/// details | Which frameworks are supported?
You can use any framework that supports React. Next.js, Astro, Remix, Gatsby etc.
///


