# DArT-Activities
Standart operation procedures of bioinformatics activities for DArT markers

To download all the raw reads from Diversity Array Technology website (DArT).
Here we are going to show an efficient and easy download by linux OS.
To download the raw reads you will have to follow the steps:
1. Login the user that submitted the DArT genotyping order;
2. Click at the **List Authetication Tokens** section, and look for a validy token,
![List Authentication Tokens Setion](https://user-images.githubusercontent.com/42940692/126247258-3a089a15-a500-4d59-ae94-3387391674f5.png)

 you can create a new token at the **New Authetication Token** if you needed it.
![New Authentication Token Setion](https://user-images.githubusercontent.com/42940692/126247048-befb989c-74d1-476e-bf38-5c591d67f2e4.png)

> Obs.: Do not worry with the ip linked to the token, you could use a token generated from a different ip.
3. Look forward for the link from the ordering site, it will be similar to the following one:
> *https://ordering.diversityarrays.com/clients/xxx/yyy/Raw_Data_Index.htmlData_Index.html*
 >     
> You can access this link at the **List Orders** section, then click at the download button of the respective **Service Number**,
> then click on "Extra Files" and at the **Raw Data Download - Download** button. This should open an html website,
> this website is the link that you will need to download the DArT raw data.
![DArT Website](https://user-images.githubusercontent.com/42940692/126247761-d55e4e6a-1a13-412e-8dda-2dd796a6f43a.jpg)

4. Finally you will add this information at the following linux command:
> 
> wget -r -nH --cut-dirs=3 --header 'Authorization: COPIED_AUTH_TOKEN' *https://ordering.diversityarrays.com/clients/xxx/yyy/Raw_Data_Index.html*
 

> You just need to change **COPIED_AUTH_TOKEN** for the validy token, and the respective link to the service number. 
