# Spanish Translation A/B Test
On this project, I am going to work with data from an anonymous e-commerce site with localized versions of the site.
This e-commerce site has noticed that Spain-based users have much higher conversion rate than any other Spanish-speaking country. For this reason, they suggested that one reason might be translation, as all Spanish-speaking sites were translated by a Spaniard. They decided to test different translations for each country written by a local (Spanish will keep the translation made by a Spaniard, Mexicans will have a translation made by a Mexican, Colombians a translation made by a Colombian and so on).
My goal is going to be examining the reults of this experiment. We will see that surprisingly, the test was negative, locally translated versions performed worse than the previous global Spanish version in terms of conversion (the proportion of people making a purchase). I will analyze why this happened to come out with some interseting findings.   

# Data
We have 2 tables that can be found on this repo.
The 2 tables are:
## "test_table" - general information about the test results
### Columns:
**user_id** : the id of the user. Unique by user. Can be joined to user id in the other table.
For each user, we just check whether conversion happens the first time they land on the
site since the test started.  
**date** : when they came to the site for the first time since the test started         
**source** : marketing channel: Ads, SEO, Direct . Direct means everything except for ads
and SEO. Such as directly typing site URL on the browser, downloading the app w/o
coming from SEO or Ads, referral friend, etc.      
**device** : device used by the user. It can be mobile or web     
**browser_language** : in browser or app settings, the language chosen by the user. It can
be EN, ES, Other (Other means any language except for English and Spanish)      
**ads_channel** : if marketing channel is ads, this is the site where the ad was displayed. It
can be: Google, Facebook, Bing, Yahoo ,Other. If the user didn't come via an ad, this
field is NA     
**browser** : user browser. It can be: IE, Chrome, Android_App, FireFox, Iphone_App,
Safari, Opera     
**conversion** : whether the user converted (1) or not (0). This is our label. A test is
considered successful if it increases the proportion of users who convert.    
**test** : users are randomly split into test (1) and control (0). Test users see the new
translation and control the old one. For Spain-based users, this is obviously always 0
since there is no change there.    
## "user_table" - some information about the user
### Columns:
**user_id** : the id of the user. It can be joined to user id in the other table   
**sex** : user sex: Male or Female    
**age** : user age (self-reported)   
**country** : user country based on ip address