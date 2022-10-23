---
layout: post
title: 'Eyes for Darkness'
---

[GitHub Repo](https://github.com/drunken-boat/EYES-4-DARKNESS)

## 0. Intro
This is a project in memory of a Chinese poet, 顾城([Gu Cheng](https://en.wikipedia.org/wiki/Gu_Cheng)), which is named after his most known poem:

>***一代人***
>*黑夜给了我黑色的眼睛*
>*我却用它寻找光明*
>
>***One Generation***
>*Dark night endowed me with eyes for darkness,*
>*yet with them I seek light*

This poem uses metaphor to suggest that a certain generation of people suffering in a darkened age still yearn and search for light, hope, and beauteous things.

Because of its simplicity with powerful contrast, rhyme, and atmosphere, it was widely considered a masterpiece in Chinese modern poetry.

## 1. Overview 

#### Aim
Perceive a poem set by Gu Cheng in a geographical way.
Combine coding skills with interest in poetry.
Show my art manifesto that poet encrypes the reality in a dreamy way.

#### Data sources and description
Text data: from the second part of《顾城诗全集》(Collected Works of Gu Cheng), page 832.

#### Techniques used
Python - Pandas, Requests(with Gaode Map Web API), Json, Re.
QGIS - Add delimited text layer, Mean Coordinates

#### Results
1. Find 3 patterns in the distribution of locations mentioned in the poem set: even, symmetry, shrinking in range.
2. Most mentioned place type is bridge.
3. Coincidence: the mean coordinate's location is a NGO for children's benefits.

## 2. Mapping
In 1991-1993, Gu Cheng wrote an unfinished set of 52 poems, 城(the City), to recall the place in **Beijing** where he grow up with deep attachment and memory.

Through the power of his strong imagination, Gu Cheng can walk around Beijing even though he was living on another continent, to see things and places that did not exist anymore; he can “refurbish” or “rebuild” the gates pulled down, the bricks, the walls, the trees, in a moment, like a god with the power of his poetry and of his enchanting words. 

42 poems in this poem set are named after a place in Beijing, for example, 故宫(the Palace Museum), so I use Gaode Map Web API to geocode them and locate them into a map in QGIS **(by Add delimited text layer tool, with the '1991_1993.csv' as input)** to visualize and find patterns.

This is the geocode map in Chinese.

![geocoding_poem_place](https://user-images.githubusercontent.com/80751447/197374387-057f6b82-eb96-4b3a-829f-e5e533e3dbf7.png)

This is the geocode map in English.
*The official English names of these places are mostly 拼音(Pinyin), the romanization of a phonetic notation for Chinese characters, but my translation is based on its location type and meaning to facilitate understanding. For example, the 柳荫街(Liu Yin Jie) is translated as "Willow-shade Street".*

![geocoding_in_english](https://user-images.githubusercontent.com/80751447/197374450-99bda6f5-1bd6-4039-b285-deb2619f71c9.png)

## 3. Patterns found
Here are patterns I found according to the map:

1. **EVEN**
Places in his poems have a relatively even distribution inside Beijing Second Ring Road, with is known as the "old city part". 

2. **TWO-SIDES**
Place in poems written in 1991 and 1992 mainly distributed in the west and east sides of Beijing in a symmetry way, seperated by the 中轴线(the old city axis).

3. **SHRINKING**
Place range shrank regularly from 1991 to 1993, and four places mentioned in 1993 are all in the "old city part".

4. **BRIDGE**
The bridge is the most mentioned place type, for example, 白石桥(Baishi Bridge).

####COINCIDENCE
Additionally, as I used the Mean Coordinates tool in QGIS to explore the places, I realize the point with mean coords of all places is pretty near the hospital he was born, which is a geographical coincidence or metaphor of life and death, for this poet set were written before his suicide.

The reverse geocoding shows this point is 中国儿童中心(China National Children's Center), and considering his hazy and sometimes child-like writing style, this is something even more profound.

![mean_coords](https://user-images.githubusercontent.com/80751447/197374461-272fb3a9-a02e-4443-86cd-99cc8b4043ef.png)

## 4. Mourning 
#### Place, time, and route
On **Oct 7th**, the day before Gu Cheng's death anniversary, I decided to mourn him by going to several important places for him and planning my route using Gaode Map JS API. 

This is the map annotating places I would visit and why, and the English version.

<img src="https://user-images.githubusercontent.com/80751447/197374518-75b3a7bf-30cb-476d-9d28-d9c5d70e957a.png" width="400" align=left>
<img src="https://user-images.githubusercontent.com/80751447/197374580-450a2077-6398-4a99-8a0e-ebb797087c2c.png" width="400" align=center>


This is a screenshot of my route planning.
<img width="1096" alt="route_planning_screenshot" src="https://user-images.githubusercontent.com/80751447/197374468-b0282139-25b6-41c0-b9d8-b34b51631a72.png">

#### Activities and thougts
Sadly, the area of these places are all tourist attractions now, with noisy restaurants in 帽儿胡同(Hat Hutong) and a bookstore under 地安门桥(Di'an Gate Bridge) closed for decades. 

In a pavilion bathing warm sunlight in dusk despite for loud crowd, I wrote down some lines in one of my favorite poems by Gu Cheng, 北方的孤独者之歌(Song of a Loner in North), and took a picture. 
![IMG_0553](https://user-images.githubusercontent.com/80751447/197374835-f6a837b6-d688-4acf-a283-6001a6e62fa4.jpeg)

I looked into the direction he mentioned in a letter explaining the poem set,

> *可以看见西直门——那黄昏凄凉的光芒照着堞垛和瓮城巨大的剪影，直洇开来……*
>
> *(In the direction)The desolate setting sun lingering on the magnificent wall of Xizhi Gate, and the silhouette creeps...*

yet the Xizhi Gate had been torn dowm, and here is the picture of the desolate setting sun.
![IMG_0558](https://user-images.githubusercontent.com/80751447/197374837-ad128450-7ebe-4971-b7cc-94e0baff9e9e.jpeg)

To conclude, this project is my manifesto that poems encrypt the reality, like the hash function, in a private and dreamy way.

## Note

I declare NO interest in his love affairs, relationship, and homicide! It is his poems, and poems only that make me nostalgic and mourn him in this way.

For privacy concerns, I delete my API key in 'geocode.py' and 'route_planning.html'. If you want to run this code, please get your key [here](https://lbs.amap.com/api/webservice/summary/)

## Reference

[One Generation's translation](https://leonarddurso.com/2016/02/08/one-generation-by-gu-cheng/)

MARGARITO, A. S. (2012). Reflections of the West in Gu Cheng’s Life and Poems. Asian Studies, -16(2), 3–19. https://doi.org/10.4312/as.2012.-16.2.3-19

[顾城之城(Archive of Gu Cheng)](http://www.gucheng.net/index.htm)


