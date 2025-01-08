---
categories:
- Travel
- Photos
- Week-notes
- Travel
- Micro
author: SSP
date: "2024-11-10"
draft: true
layout: indie
month: 2024-11
tags:
- Tag1
title: Indiewebify this site
year: 2024
---
{{< updatetags >}}




{{< gallery >}}









#### Adding the H-card

Add this to the footer

	        <p class="feet h-card vcard">{{ .Site.Title }} &copy; 
            <a href={{ .Site.BaseURL }} 
                class="p-name u-url url author metatag" rel="me">
                {{ .Site.Author.name }}
            </a>
                <img src="{{ .Site.BaseURL }}{{ .Site.Author.photo }}" 
                class="u-photo" style="display: none"> 
                <a class="p-nickname u-email email metatag" rel="me" 
                href="mailto:{{ .Site.Author.email }}">
                {{ .Site.Author.nick }}
            </a> 
                2011-{{ .Now.Format "2006" }} &bull; Licenced under 
                <a href="{{ .Site.BaseURL }}page/licence" 
                class="metatag">
                {{ .Site.Author.licence }}
            </a> 