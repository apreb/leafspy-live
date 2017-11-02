
![](https://lh3.googleusercontent.com/CsLHWdHVCAt-KWosWwc9-U9d_5u-2AwKIA5Yspvs9L9l-1WvFBqrrtVBkw766DT01YPL80Mn1mgPjrkYWK_gCjqswhHi05O1NKdt_l00czVyBYA4BrTskUvk5D7nyN4kc3E-RCVl149SK3_fdVHPJplLq_2GjJcuKt6h0ktB3FyIUtuOjC8PyMH4-K5uX3bKFcKoumoq92WeG-AB8poxMcXqRfYeDrydJax_R_i7oFCGrDGi88ssbCChICJ-oxM3z0g37LO5c0QWPof7TH2AJ6am_bEZpnZdi4LaTfOMDGxyJgZpse7iBtqvUNpb9eAHG-7IC5I740IGKe0TGcp3gRwolPkYuHZgZhsKhKR7XFroSdavnfZ8bW1w4QVhXre6HsIMg0rqWK5tfsKEIGk-EUpfqbCIKrikobcNTJEdiouO81z1Ibav5dGu_yxgIDUth9mbsKnwRXmIJOCilmNo2Cj_W9uXMuldJSa2qf7pGKrXn3pSJ7G_pV5ynugSy6i1FVnfCLVzi9y2tYgIWU-lMYxn1jkkOjAr5jDDIp55KheO100zPxxJEgW6-G9hvHKG9qmwRfKUeugD02OTfrPkMlgM56O9-zY2PW0V50qW1Q9_nNHfwXSyY1cyLun8G80mv2_OLeZUlJI3NEfUZT34cJtkkphr7SnSZc4=w874-h233-no)

Leaf Spy Pro (LS) is a mandatory app for every Nissan Leaf owner. Some of this APP potential is hidden away in CSV generated files that can be hard to evaluate and handle over time.
Leaf Spy Live captures live data from LS and automatically processes many of the available data to facilitate its visualization.
It is possible to generate the following information:
- Live trip on map with live statistics, SOC, GIDS, kWh, Battery temperature, etc.
- Browse trip history
- Send charging statistics to emoncms for energy visualization
- Keep track of latest Km, Battery temperature, AHr, location of the vehicle, etc.





### Prerequisites

- One OBD II compatible bluetooth dongle
- Leaf Spy Pro
- Dedicated smartphone with bluethooth, GPS and mobile data plan
- One Raspberry Pi with [emonSD](https://github.com/openenergymonitor/emonpi/wiki/emonSD-pre-built-SD-card-Download-&-Change-Log) image 


#### Leaf Spy Pro Settings


![](https://lh3.googleusercontent.com/U3IWT1p4BnRmnbstUZ4a9926tldol-9HhCu2cBdK4Qr7e_Vqbzw58FEcwhbyWnEbivXX3Zz5Ah5JyuuFnkQakC2z42wc5QMuBYfcNi_fNthWn4y2eLl9ykfgPJUraTXmBm_X7lcMthVQhl51AgYLTg3X7Y6OXmTdH3ZLVd5IN8q8p9TK3K7kNQ3h1goLQG4Hdq5fk46x1Dzi0bk_XajALUa7tLyU7L1BbdGpTC2mhQcQVaDzxxHyvhtwtMaU_PaudxqWdvxwwMaXZWKo6Lx-5T-_JDQk8QylSEY6cbV25mMUG5b93ynepFfpfn8nAuEPQRHRWzZ5XlUU-5K7J4GScTo5Dt8PkibhRzetSpsMaWNkZ8ocni9XvTAkOOb60LjPtVsmnZpdVAD_GT-NUA3Rm8uqXXQlpklS1RikI3bibAHDi_rHriMKVNtUXr1rgEQbBF3Fmr4U_uJ9tx2SFoakIGBuriJ5NYEkwCiXHVyEEKNAkJ7BqEdwaaHKJNTO8QchVVJCgil-Fmm2K3VaUWogVlrKLbF8ktUK8rCOmXRhrHe8TI2rnIDHvJt47vh0Wa_kzfZC4YdcbqW8nrOT0SA85hBNlf4Si_BhbodLfaEXUWmI4ZqL0qGE-_IUTiOb0lYyvJlnLanZ6zG_O3Ifg4Zi5YN2iS1CzdEFqNo=w429-h364-no)

Go to LS Setings, Server section and fill the info below:

- Enable
- Send interval = 5 sec
- URL: 192.168.1.1:1880/ls (change to your own IP address)

It is possible to use https, however a valid certificate, issued by a trusted authority is needed.


![](https://lh3.googleusercontent.com/91wQlgf2gKfSZ-OmDvldh1GVEYHFWppWFOUDFdg7UVEeCvLLBOuzcdxVFji7V0iW5qKAfVW8Nswnhv32zo0l4zUipWbHNvT4bnbPulIPv75CwnYwXyuFfG-zY3FlCrhYijO-X-dlU1qlLYFIU8rvW7FA5D0RNWIdY4IaUa-70pUyficXUkEn0TmE4yelzvScs-tX6m5Ge6bEeq1OoufQf_hXL0yg08NlGqNtwlg64sYFtjP0DqB3G6xkjj-sML_HK-d9DPXpA-l8H2Q8pEVW62c2fKP6W1PmV37nTM1duvhCn6vdp04ZAM4AKxc_PFiiuD3W2A8UFI2-gRVs5A7Dnl5CMjgCW0-J8dBslkdts9H0axYtux0-kf_kyTkxb1uZCOymPAEYORxtGpDtYNgu-NYEKaQ3-Lt0gbLpZIZhJKd-nwnX4kDMCBZrln0HaN3qbnJDvQ3SyUsP_BCNtjfGOhW0-choZob5gHQoKvS4NRUDfheKOV9IxJxU6RO9H17_wQNde1zTaE93dvqKjWgPQcRxLbh9ufxha3wY3yR0JF8Upcbz-omZaVaZcsA-pD0zfGETWFIHPCFfLi_uHPtV46HRgcuzC0d6lBn3s3cGIoIDpfUMPm1v1An5YkSYeYTkguuGgdme5LpaWTEmhbwrLiCKg7hw1X0JtX8=w822-h417-no)

Now make sure Leaf Spy is connected to the OBD Dongle in the car so the data is sent to the server. 
Leaf Spy will complain if the response from the server is not adequate. 


One of the main features is live trip tracking, so reachability between Leaf Spy and the server is needed. There are many ways to achieve this and are out of the scope of this blog post:

- Use a VPN (OpenVPN) between the remote smartphone and Rasperry Pi
- Use a free dynamic DNS service to resolve your public ip address and create a port forward rule to your Raspberry Pi.






##### Server side - Raspberry Pi

Bits of software required to parse the live streams:

- Emoncms
- MongoDB to store trip data
- Node-RED with the following extra nodes:
  - node-red-node-mongodb
  - node-red-contrib-mongodb2
  - node-red-node-emoncms

  
To install mongoDB simply access the bash of the rpi and copy-paste the following commands  

```
rpi-rw && sudo su
apt-get update && apt-get upgrade
apt-get install mongodb-server
```

Before running the DB we must change the directory of the data and disable logging:

```
mkdir /home/pi/data/mongodb
chown -R mongodb:mongodb /home/pi/data/mongodb
vi /etc/mongodb.conf
```

and replace the contents with the info below:

```
bind_ip = 127.0.0.1
port = 27017
quiet = true
dbpath = /home/pi/data/mongodb
journal = true
```



Save, permit the mongoDB port in the firewall and reboot


```
ufw allow 27017
reboot
```
Reboot and check if the mongoDB is running by trying to connect

```
root@emonpi(rw):pi# mongo 
MongoDB shell version: 2.4.10
connecting to: test
Server has startup warnings: 
Wed Nov  1 17:38:56.658 [initandlisten] 
Wed Nov  1 17:38:56.659 [initandlisten] ** NOTE: This is a 32 bit MongoDB binary.
Wed Nov  1 17:38:56.659 [initandlisten] **       32 bit builds are limited to less than 2GB of data (or less with --journal).
Wed Nov  1 17:38:56.659 [initandlisten] **       See http://dochub.mongodb.org/core/32bit
Wed Nov  1 17:38:56.660 [initandlisten] 
> 

```


Copy (ctrl+c) the flows from the repository [here](https://github.com/apreb/leafspy-live/blob/master/Node-RED%20flows/flow)

Open the Node-RED dash `http://ip_of_rpi:1880` and paste them to a new tab:

![](https://lh3.googleusercontent.com/B1UDLos9pw9D8XyQI4Fg-0Ax7f67QbTm9aFyES5MjGWQ2cRjkeg2j4y7cSTLdDSVTiUq0wxlkWsQCKRzsJFvzlPHuSBNGZYi72slify-2gokJNdontUGZiTyuaKqzlhAVRgcjJTIYg14BRID3GblKc1KYmnZ9qH2ceSiAXi4o6WYbfNrLcDTKva1oEeQyYKxZn6C6ItdI3z392hx0QD8py86x2r9YPbHa4UkuyfBSLcVyV7hePynxd2ekMA_NYOaaP049yKqcmH_bevGwh_PEELHkoGyBNGADkEsZlr6SRmWi4xNPW-bb27DtoetITTS5PCMTlAZ03lzguuLtUzQmR-m_zxsGx1vkaQxHT517SASNNxDUJr5SbJ6i9iv7Cq586AbqqtL-ZjzgrqL2etuun_oYzOxOF87LHzCq0iRzI8pXdv7LREu6j-wpLUinDvnhuGht-6bTttgIIl8VVvjmhk2wtcg3ORYMJQgkbB0UGRgBBdcgQFLU9xziQ3cktyFQ9D4ESw2OhtiwaryoCBBo18EYXhyhaJSwp3X7Z_IhCr0CbXloRBFxeuxGkHJIm0LaOxxlmf78zKm97S3Xou2kbqsh1hKLHGpAKI-4_Ho-4dAWmY7gy9Qj6XIC06JXmsfMzHxJCpem4w6Xj728MW3a4T7CFgSHPhWc_w=w475-h162-no)

![](https://lh3.googleusercontent.com/n5CaQPr_hCPqOOCKnLhB56JNPY2AKprieC0plETFcs2kj8jLcZGmdTA1Y36DWHjAgrrQT74J7BCo1jKZjfUAUIs2hnhVcc9E1NCnfmdAMVYFJ_PvirciTNMnF-waOtwtxOpSEPguYx9ibrGU6hfhCYTqTF3cIH1SoKbdzUEieuYLr62a9c3pPG4rkGLS-GW8hKC4JMBtupmO5SerxA4BHL0OyJaKZN-sEVetoRVFqlrIydrfxvOCy9Tv3QImn1oLKIwJ2qmp38dEC1H1LGom3rykCgGXqQ-zVbQKas1cJ2vp9GkBCGVwJf5_hDZHhx_ajLBHpratjEm5un2q7ETBCEvHeqVkqP6MxQ4FIn96lJ_wZBnm3CwGj1p4vH4HcCMwgkWIp5D7AAdHmBzwvmI4cHMhOkclkHlIK5PUczZMvH8ZE9xv0yJVrVUFhdmgqmZ63V0TCYKk5exoPOPURKdw3Cz8GQpIp4rGNubYkPat54tH9kWWPgv2ohMxb5TrKMtGf349FEVNzl2434410qn3DrZ7Y6Bubdby25fs7xHAiHLAXhzk8gKPpX7uPt1vArIa1pE5pkBPZ4Q9ZYCHSD8Xj786KW0kMswZaUnxwcdLoiR9L5fD9unS-K5-lRrFSckeFFLhZekKIWRrUKl5_euLuYMZDo1iZG0g1Ys=w947-h459-no)


Some nodes may need additional configuration, such as MongoDB, MQTT, Emoncms.
The flows are broken down into sections which are explained in more detail below.



##### Leaf Spy Server

![](https://lh3.googleusercontent.com/zUiJtrK95MObSq_orQsD-u0aEEzoBqOJpanC1Rv8Zevv8rEWJtJWJpV_F6vWac8U1Wt55xaQx-QPCuH-JpS084fhQEUxys8no71tRnCzAxypUZHGuOYtRuMpxYgIH4nkqTn37U64v81Hvvu0EFVVjGBJQhQ-hQdtQgaoThnTs0SdUz6Hs5CDtvCyVZH-D2Gjlkv97Dw9vG65Pt0q-8mUNNdz4oKOpiWRT3oe1hgiAchDhSMxEYhP5_JSzkDbSPRoo_HE6D3aZ1N54yEcrCVXj09uCqMblW42_f50UNQ7mtU_W6giE36hUq0zC11ZbBuuI_BgXISVW-yN4njJLydB55hUktYjWop0gX6sMzQR9_2amtTn8gJPOUSwk8emOLLDcFVCHhpZoy_xvSStrAnwx0BT2izh57ifCNpzqAmeFK8bPNt0JhSYZnso77Qt2SDFRbdk7-Oaulrye25SjnxEkoMf4ZayODJrDwg8pX1GErLS_buDOmvfkSJLI-BzHDkZ0j1zT6hRW-Zg7MeaVLlOUMgXurBhzOFn_8QCe323ela_9UodP4r2EiNiIT-k3diYBrN5c7EiMlhoSd8kqgqtwDsqfQ9UV-_DrHBA3RrmYzSnLzHAAkhm1ZrXNVW5emuWmNt4_KA_6SFtBKde5vl8fqxcq4DJME_nPlc=w720-h394-no)

First http Node listens for Leaf Spy data at `http://ip_of_rpi:1880/ls`. A debug node can be attached direcly to check incoming messages.
The arrival of data triggers a response back to the server to keep LeafSpy happy. The data passes through a function node to prepare the data for three main purposes:

 - Together with a timestamp the original data is posted to a persistent MQTT topic.
 - Charging statistics are gathered to be posted to Emoncms.
 - Filter trip data and save it ot the mongoDB.

If the trip data has valid GPS coordinates and the car is ON, the trip point is eligible to be stored in a array of trip data. However the data must be trimmed at the end of a trip to keep the statistics coherent. 


>To uniquely identify a trip, Leaf Spy sends a "Trip" variable that increments every time there is a new trip. When the car is turned on ( ON or "Ready to Drive") this trip value is not yet incremented and reamins with the previous value. The increment happens when the car starts moving so there is no need to trim the beginning of the trip. The actual trip ends when the driver stops and turns the car off. A variable on the data signals the status of the car and trip data is not updated. However, when the driver starts the next trip, or if it turns the car to the ON position, the trip data is resumed with the old trip number. In order to avoid this effect, every datapoint of the trip must be checked against the last correct trip data and must not be more than 30 seconds apart. There are caveats associated with this method:
> 
>- When the trip ends, the driver should wait 30 seconds before turning the car ON again in order to maintain trip statistics coherent
>- If during a trip communication fails for more than 30 seconds, the trip will no longer be logged 


To trim the trip data, the function stores the data in memory and queries the mongoDB for the last saved trip entry. 
The Epoch timestamp of boths entries is compared and stored if they differ no more than 30 seconds.
 
If the "LIVE" switch is enabled on the user interface, the valid trip entries trigger updates to a unique MQTT topic. The websockets section is listening on this topic and updates the map in real time.


##### Live Map HTML and WS:

![](https://lh3.googleusercontent.com/UP9p01mRo-ExQ1cV6LCyDQ0zASOE3SaIO8gVRHiSzIng5ZTOq1ElwXxgEkBSrSnj6Fs8VpTz9Yt5pla0ASkdeOSxdcuLmUIrKC0bDUuwOH3X_YdFRvgbU7ZWNb1GqPlvDjwf0lWXMDbBtzCYkJ0U3wLFOe0pNKX8hfl4RccX10K3Y6VrGVFZhLXPo6bej3bHLuU1luCiUx3hN0FWQC8_ImNogKkPXN5_7_aSCg_490tThhKxOyt24bETMUyZMDZMMwTKCFZbK6N7615VQib8cgin4IaGlB0roiYfz1nn-9eQx-_NYDmd5aEUgitH6k-izS4I3c4kBIqEbrvvQgBzNHXNytEllmiJR0rAOsWoCMbaisu2L-1F_RIjJ_L8STKm8Wtn2NQwyE7VdwAa1FjDGVGG1zoKakxStdOEJg2nE6P6SnQvD1cKpl9j08TT1Uho4HWobjP6Bryc9aFoJ8ClV6i9NxdxdkIbxXha_7MhTmocHc8iFAXx_NA_xnlK4vL02AAhQ2gYv-4hVTWmVSIjdiwNxxLwarNJgXBhz9LpXuK2N9-7QIJGlN6VmBVLAH0odYySeesrLe2-hFukBqhJJMIxv7hHnj3ZvNsOmu2ISDFGD8A-3ldC466pLKUvRvnmeD23nFrH66BjwQnUUUfUkrAixaJB1kbSUUk=w448-h120-no)

Pointing a web browser to `http://ip_of_rpi:1880/map` loads a map with some javascript that opens a websocket connection to Node-RED at `ws://ip_of_rpi:1880/ws/location` to draw the latest trip over a map.
Open the Map template and replace the ip address with the real ip address of the raspberry pi.


![](https://lh3.googleusercontent.com/nTIqV3f_4wPJNa2M4VBZpOedd_MG1d_TmNHHdAAE6FMz-PCE9Hl92bZiVsVMsclLT4DWDMYIz42jajkFUch_1rhZcpZfawEo1rt8Ky9vGpgYbaUPn-lzCl8A7B5rgqztUThrVkViyr685Wc3oZzkUw_3S8FbgnRyKhu80vDBJwh0CKSvVBw66WWt18zrCe9aAZobIvGqg35R30UoTFJOM2iaDsSgWrp_84LtpIWg0bBnLxGn1TfczrhXu0QyIIIfv9jH1qli9DKjuC8XTqNstDgtgxr09fhQM3GbjZ1Q_Nhmk_AC0SQx8UiO1JxHZqWyuUtt0TYQ5s8W5lyiRbAGRff9ZYoMY3GK6kRXUqduxO0jQPaqGzJFRaaTJRulixBqhQfazJu2VNnS8Vq9YkqVKB7iseo1PxdJ0R4m9gF0WZjBtUW4de_OX2U2Q403YRxoaqa0eTOAb2aBH3t2Vp2G4IxXj9niSCt3WsqdVFHerchuFumhUteJpjzj-cwm1FK65LDCLaICvcSBf8r7mv2HY6UO-W4HfWccyq3sGnkpvDdq3lH8HjYcxLfx9arSZ8Js1xN0ofezlDQL916Ccvr9F0OhorThb4Muo27W4hdKNfJBNsAaskRn8hj9XRQ-9rzC7j8O3jlE0syB0TsQo9jIZ4xjKwxkI4pTvL4=w709-h328-no)


Every WS request triggers a mongoDB query for the last trip index. A second query of the DB deliver the particular trip's data back to the browser.
It is also possible to query direclty the DB for a paricular trip using MQTT. Every request is also sent to a persistent MQTT topic. MQTT enables building the user interface that is described on the next section.



##### User Interface (UI)

![](https://lh3.googleusercontent.com/weGgL_NsmD23zD0fcDp-z6V2gwfpB3AD8UXxTl0wG2nspBxAGKko7pMexRedKhtxsCCxdoP868PUlWcxwuT239dwYoEnUjbpVLLuV3mQIXEHRHPJhvv8xAVI5q-dFG8V5pULf4XThAtpYkRm9-RfoChpCgE78GGO5GbzhxIAuVcg_ks8_HkgLbaa3jEa4V-kBpXC1pqNX4Ncz7HVajNIRUgwNEpj7djv18ir96sPN_fCtRSTCqY24ISiGC53X8vvrEJqtuigis8gQUCVKU6doythrb0KLZxUafXGm-xpZQ3WDb_e37Z8rMIBTCtoMG0Pl1F0etB2hcs2MExzwTH1x7_F7W29cKA4mUcoqysKVJu3ufz3HpIlZi9i1bIsZHAjFUVFjz-nrvvjKr4loH1BjgmSux7eXwPu58_UHG-uqK-o7FOPK_GnYAyx6t7PNff-q6nIrEKkd56uyyIi0Diom0P2i6UedrYYfWh6boCmSl2z7FfGT-M-RHVv-GxlpwTtB7SNHofFCuE3amFyksFvDViVmTBZqk_jP93nuHpvE1KEfHSoPnCug9awYmO50OKpIxyVwCAQp9AIQ_v57pO7D9i7vxwZeUyV1AIty-GwK710d3APGwBHYWPo-hOTBLpuEygh90SacjHTzCalRedPjHrJ-ZxJzx_zENE=w658-h562-no)

Two pages are created, the first shows the raw data coming from the APP. The second page shows a map and statistics associated with trips. The map can go live to follow the real time trip or can be used to browse trip history.
The URL of the LiveMap template need to be replaced with the real IP of the rasberry Pi.

To access the UI, browse to `http://ip_of_rpi:1880/ui`


User interface pictures:

Live Trip             |  Live Info
:-------------------------:|:-------------------------:
![](https://lh3.googleusercontent.com/GavC3tpJnyBjLfkexw_fxuoFwAFV6-40QdLeAjyJXg_XHWqOKPsBgd2sSGIU0_Ib4apKYzqWc5iCWbdrdXCJIFitrhxZu86C4Q-Ki0Hc-YAMb1kenxt8liaBuZGMoTojhTYfr1slXQ=w344-h695-no)  |  ![](https://lh3.googleusercontent.com/Lax3EkdPKx15suZ2r4ce2-2u80-VmO5drZAbAW1ZrhtLK4TERxOyqKns9zpL8Rz-Mk6SK2Ts88LXeDBW-VkCqP1WVKc0szm5VRKK7pAm7BnN9dV1PulFlVBWSe2AZn-DIm1QhqliQw=w342-h650-no))



Some early examples of the Leaf Spy Live in action:

[Live Map #1](https://www.youtube.com/watch?v=LtvB6V47V2A)

[Live Map #2](https://youtu.be/yWC1Gfmsmf4)
