# Data-Science: Crimes Analysis.

# Components:
   - Guilherme Bertelli
   - Tomaz Filgueira 
   
   
# Objectives
In this work we have analyzed the data of Montgomery County, in the state of Maryland - USA. The dataset has been analyzed in different ways such as time, location, types of crimes and combined analysis.

# 1. Time Analyzis
## 1.1 Comparison "Dispatch Date / Time" and Start/End Time
   Dispatached Date / Time means the time when a Police Office has been dispatched to the site whereas the Start/End Time mean the times when the crime occorred from and to, respectively.
   
   According to the Dispatched plot, it is possible to see that the peak of frequency that a Police Office has been dispatched to site where the crime occured is from 7 am to 8 am, probably meanning when the shift timetable starts. On the other hand, when seeing the Crime Start Hour plot, it is possible to analize that most of crimes occur from 0 am to 1 am with a number of over 1750 occurences. At the same period of time in Dispatched plot, we have got a number of 900 occurences, concluding that 850 crimes occured and no police office was despatched in that period.
   
   The minimum number of occurences if found from 4 am to 5 am in both plots
   
## 1.2 Month
   According to Month's analyzis we can see that the Montgomery dataset started in July and its crimes' occurrences reached the number of 3500 situations. The following months, from august to dezember, the crimes occurences remained steady around 4000 situations.

## 1.3 Day of week
   The week analysis tells us which day of week has occurred the most of crimes. Surprisingly the weekend period has less crimes then the week period. Sunday is the day when the crimes less occurs. It is roughly 40% lesser than the highest values found  in Tuesday with the number of 3800 occurences.
   
   # 2 Location Analyzis (By Beat)
The "Beat" dataset's column has been used to analyze where the most of crimes occurs. Beat is a subsection of the sector which is a subsection of the district. In other word, using the beat values we can garantee that the analyze is done with good Granularity. Furthermore, the beat column has the least NAN values found in the dataset when analyzing the crimes' locations.

## 2.1 Introduction
The values are shown in a following manner: 1º - District; 2º - Sector; 3º - Beat. For example: 3I2 means the second beat of the sector I of the third district. Each district has a limited number of sectors and beat, and they are distributed in a sequence.
For example:

For District 1 we have:
        
        Sectors: A,B
        
        Beat: [A1,A2,A3,A4] and [B1,B2,B3,B4]

For District 2:
        
        Sectors: E,D
        
        Beats: [E1,E2,E3,E4] and [D1,D2,D3,D4]

For District 3:
        
        Sectors: G,H,I
        
        Beats: [G1,G2];[H1,H2];[I1,I2]

For District 4:        
        
        Sectors: J,K,L
        
        Beats: [J1,J2];[K1,K2];[L1,L2]

For District 5:
        
        Sectors: N,M
        
        Beats: [N1,N2,N3] and [M1,M2,M3]

For District 6: 
        
        Sectors: P,R,S 
        
        Beats: [P1,P2];[R1,R2];[S1,S2]

## 2.2 Beats, Cities and Crimes per 100.000 habitants

It is possible to see that the crimes ratio per capita has its highest values (7374 crimes per 100.000 habitants) in the district 3 (Montgomery annual report) and that result agrees with what is found in the dataset. When analyzing each beat individualy, we found that the most of crimes of the Montgomery County occurs in the 3GI area following of the 3I1 one. It is strongly correlated with the city of Silver Spring, however this is just a small area of that city. The rest of the cities has numbers of crimes less than a half found in Silver Spring. Furthermore, districts D1,D2,D4 and D5 have a number of crimes per capita similar to each other. On the other hand, district D6 is the second most violent.

According to the dataset, the city of Silver Spring has approximately 37% of all crimes in the Montgomery county. Other significant values are found in Rockville, Gathersburg, Germantown and Bethesda. They represent 46% of the all crimes in the county.

# 3. Types of Crime

   The Class Description column has the information of different types of crime and the number of its occurencies. After separating the desired information, the set() function was used to allocate only valuable information in the array types_crime, which means only the different types of crime. In total, the database shows the occorencies of 285 different types of crimes.

## 3.1 Common Crimes

   With the column generated with the value_counts() function, the crime occurencies are obtained in the classd_column. The bar plot, making use of the matpltlib library, shows the 8 most common crimes, in which the following can be highlighted:
    - Driving under influence (1710);
    - Posession of marihuana (1334);
    - Not cooperating with police investigation (1191).
    
   A total of 31 crimes occured only one time, such as suicide attempt with firearm, animal offense by keeping it in the car, vandalysm for graffiti material posession and non fatal manual drug overdose. A bar plot shows all the least commum crime occurencies.


## 3.2 Violent and Non-violent Crimes

   In order to separate violent and non-violent crimes, an analysis of the crimes_column array resulted in the establishment of key-words for violent crimes, which are: ASSAULT, HOMICIDE , ABUSE, HARASSMENT, SEX, CUT, ASSLT and FORCE. With the str.constains() function, the classd_column was checked for the keywords. In case any of the selected keyword was found, the value in that position of the array would be allocated in the 'violent' vector. If not, the value would go to the 'nonviolent' array.
   The three most common violent crimes are:
   - Assault and battery to citizen (382);
   - Simple assault to citizen (311);
   - Assault and battery of spouse/partner (290);
   
   The three most common non-violent crimes are the most common overall, which are:
   - Driving under influence (1710);
   - posession of marihuana/hashish (1334);
   - Not cooperating with police investigation (1191).
   
Non-violent crimes represent 93,89% of the crime occurencies, with a total of 21942. Violent crimes, had a total of only 1427 occurencies. The three most commum crimes, which are all non-violent, account for 18.12% of the total crimes, while the 3 most current violent crimes accounted for only 4.2%.
