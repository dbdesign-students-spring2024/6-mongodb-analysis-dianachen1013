# AirBnB MongoDB Analysis

## Data Information  
The data set that I'm using is the information of Airbnb that are located in Boston, Massachusetts, United States from this website [AirBnB listings data](http://insideairbnb.com/get-the-data.html)  

I unzip the file [listings.csv.gz](data/listings.csv.gz) and save it in the folder [data](data) as a csv data file [listings.csv](data/listings.csv)  

## Data Display 
The following form shows the first 3 rows of my data set. I've clipped text in the name and neighborhood_overview fields and replaced the listing URLs with markdown links for compactness.  

| id | listing_url | scrape_id | last_scraped | source | name | description | neighborhood_overview | picture_url | host_id | host_url | host_name | host_since | host_location | host_about | host_response_time | host_response_rate | host_acceptance_rate | host_is_superhost | host_thumbnail_url | host_picture_url | host_neighbourhood | host_listings_count | host_total_listings_count | host_verifications | host_has_profile_pic | host_identity_verified | street | neighbourhood | neighbourhood_cleansed | neighbourhood_group_cleansed | city | state | zipcode | market | smart_location | country_code | country | latitude | longitude | is_location_exact | property_type | room_type | accommodates | bathrooms | bathrooms_text | bedrooms | beds | amenities | price | minimum_nights | maximum_nights | minimum_minimum_nights | maximum_minimum_nights | minimum_maximum_nights | maximum_maximum_nights | minimum_nights_avg_ntm | maximum_nights_avg_ntm | calendar_updated | has_availability | availability_30 | availability_60 | availability_90 | availability_365 | calendar_last_scraped | number_of_reviews | number_of_reviews_ltm | number_of_reviews_l30d | first_review | last_review | review_scores_rating | review_scores_accuracy | review_scores_cleanliness | review_scores_checkin | review_scores_communication | review_scores_location | review_scores_value | license | instant_bookable | calculated_host_listings_count | calculated_host_listings_count_entire_homes | calculated_host_listings_count_private_rooms | calculated_host_listings_count_shared_rooms | reviews_per_month |
|----|-------------|-----------|--------------|--------|------|-------------|-----------------------|-------------|---------|----------|-----------|------------|---------------|------------|---------------------|---------------------|----------------------|-------------------|---------------------|------------------|--------------------|---------------------|--------------------------|---------------------|----------------------|------------------------|--------|----------------|-------------------------|-------------------------------|------|-------|---------|--------|----------------|--------------|---------|----------|-----------|-------------------|----------------|----------|--------------|-----------|----------------|----------|------|-----------|-------|----------------|----------------|-------------------------|-------------------------|-------------------------|-------------------------|-----------------------|-----------------------|-----------------|-----------------|----------------|----------------|----------------|-----------------|----------------------|-------------------|-----------------------|-----------------------|--------------|------------|----------------------|-------------------------|---------------------------|------------------------|-----------------------------|------------------------|----------------------|---------|------------------|----------------------------------|-----------------------------------------------|-----------------------------------------------|--------------------------------------------|-------------------|
| 3781 | https://www.airbnb.com/rooms/3781 | 20231218233145 | 2023-12-19 | city scrape | Rental unit in Boston · ★4.96 · 1 bedroom · 1 ... | NaN | Mostly quiet ( no loud music, no crowed sidewa... | https://a0.muscache.com/pictures/24670/b2de044... | 4804 | https://www.airbnb.com/users/show/4804 | Frank | 2008-11-11 | Boston, Massachusetts, United States | From Boston, love to travel (45 countries and... | within an hour | 100% | 88% | t | https://a0.muscache.com/im/pictures/user/2cde8f2a-5a19-4c8c-a... | https://a0.muscache.com/im/pictures/user/2cde8f2a-5a19-4c8c-a... | Roslindale | 1 | 1 | ['email', 'phone', 'reviews', 'jumio', 'offline_government_id', 'selfie', 'government_id'] | t | t | Boston, MA, United States | Roslindale, Boston, MA | Roslindale | NaN | Boston | MA | 02131 | Boston | Boston, MA | US | United States | 42.286241 | -71.134374 | t | Entire rental unit | Entire home/apt | 2 | NaN | 1 bath | 1 | 1 | ["Air conditioning","Free parking on premises","TV","Wifi","Dedicated workspace","Kitchen","Heating","Essentials","Washer","Dryer","Iron","Hangers","Hair dryer","Shampoo","Carbon monoxide alarm","Smoke alarm","Private entrance","First aid kit","Fire extinguisher","Self check-in","Keypad"] | $125.00 | 
| 5506 | https://www.airbnb.com/rooms/5506 | 20231218233145 | 2023-12-19 | city scrape | Guest suite in Boston · ★4.79 · 1 bedroom · 1 ... | NaN | Peaceful, Architecturally interesting, historic... | https://a0.muscache.com/pictures/miso/Hosting-... | 8229 | https://www.airbnb.com/users/show/8229 | Terry | 2009-02-19 | Boston, Massachusetts, United States | Your hosts are a semi-retired architect and a ... | within a few hours | 100% | 100% | f | https://a0.muscache.com/im/pictures/user/d3b68c6e-7323-4b5e-a... | https://a0.muscache.com/im/pictures/user/d3b68c6e-7323-4b5e-a... | Roxbury | 4 | 4 | ['email', 'phone', 'reviews', 'jumio', 'offline_government_id', 'selfie', 'government_id'] | t | t | Boston, MA, United States | Fort Hill, Boston, MA | Fort Hill | NaN | Boston | MA | 02119 | Boston | Boston, MA | US | United States | 42.329809 | -71.095595 | t | Entire guest suite | Entire home/apt | 2 | 1 | 1 bath | 1 | 1 | ["Air conditioning","Free parking on premises","TV","Cable TV","Wifi","Dedicated workspace","Kitchen","Pets live on this property","Dog(s)","Heating","Family/kid friendly","Washer","Dryer","Smoke detector","Carbon monoxide detector","First aid kit","Safety card","Fire extinguisher","Essentials","Shampoo","24-hour check-in","Hangers","Hair dryer","Iron","Laptop friendly workspace"] | $145.00 | 32 | 1125 | 32 | 32 | 1125 | 1125 | 32.0 | 1125.0 | NaN | t | 16 | 34 | 59 |
| 6695 | https://www.airbnb.com/rooms/6695 | 20231218233145 | 2023-12-19 | city scrape | Condo in Boston · ★4.81 · Studio · 2 beds · 1 ... | NaN | Peaceful, Architecturally interesting, historic... | https://a0.muscache.com/pictures/38ac4797-e7a4... | 8229 | https://www.airbnb.com/users/show/8229 | Terry | 2009-02-19 | Boston, Massachusetts, United States | Your hosts are a semi-retired architect and a ... | within a few hours | 100% | 100% | f | https://a0.muscache.com/im/pictures/user/d3b68c6e-7323-4b5e-a... | https://a0.muscache.com/im/pictures/user/d3b68c6e-7323-4b5e-a... | Roxbury | 4 | 4 | ['email', 'phone', 'reviews', 'jumio', 'offline_government_id', 'selfie', 'government_id'] | t | t | Boston, MA, United States | Fort Hill, Boston, MA | Fort Hill | NaN | Boston | MA | 02119 | Boston | Boston, MA | US | United States | 42.329941 | -71.093168 | t | Entire condominium (condo) | Entire home/apt | 4 | 1 | 1 bath | 1 | 2 | ["TV","Cable TV","Wifi","Kitchen","Free parking on premises","Pets live on this property","Dog(s)","Heating","Family/kid friendly","Washer","Dryer","Smoke detector","Carbon monoxide detector","First aid kit","Safety card","Fire extinguisher","Essentials","Shampoo","24-hour check-in","Hangers","Hair dryer","Iron","Laptop friendly workspace"] | $225.00 | 29 | 1125 | 29 | 29 | 1125 | 1125 | 29.0 | 1125.0 | NaN | t | 14 | 34 | 64 | 

Problems: Noticed that there are many columns that are empty, and some rows include empty datas
Data Munging: I use mongoDB Compass import the original csv to mongoDB, mongoDB Compass automatically helps me deal with the empty data. If we are not using mongoDB Compass, we can also use python to delete empty columns and rows.   
![image](./images/data%20munging.png)  
The new saved file after data munging is [dc4829.airbnb](data/dc4829.airbnb.csv)

## Data Analysis

1. show exactly two documents from the `listings` collection in any order.  
Code:  
```
db.listings.find().limit(2)
```
Output:  
```
[
  {
    _id: ObjectId('6610d78facb2cce54b6a810f'),
    id: 3781,
    listing_url: 'https://www.airbnb.com/rooms/3781',
    scrape_id: Long('20231218233145'),
    last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    source: 'city scrape',
    name: 'Rental unit in Boston · ★4.96 · 1 bedroom · 1 bed · 1 bath',
    description: '',
    neighborhood_overview: 'Mostly quiet ( no loud music, no crowed sidewalks)  area with residential 3 story buildings, some 4 and 5 story newer buildings. Though not in an "entertainment" area there are local food shops and supermarket with a mix of restaurants.  Area is in transition--East Boston has a great waterfront with gentrification evident everywhere!',
    picture_url: 'https://a0.muscache.com/pictures/24670/b2de0442_original.jpg',
    host_id: 4804,
    host_url: 'https://www.airbnb.com/users/show/4804',
    host_name: 'Frank',
    host_since: ISODate('2008-12-03T00:00:00.000Z'),
    host_location: 'Massachusetts, United States',
    host_about: 'My wife and I and grown children frequently occupy the spaces that we rent and as such try to make the spaces pleasant and appealing to ourselves as well as guests.   We have been subletting for over 15 years and consider ourselves helpful and organized hosts who provide clean, attractive and comfortable apartments',
    host_response_time: 'within a day',
    host_response_rate: '90%',
    host_acceptance_rate: '29%',
    host_is_superhost: true,
    host_thumbnail_url: 'https://a0.muscache.com/im/users/4804/profile_pic/1327953150/original.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/users/4804/profile_pic/1327953150/original.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: 'East Boston',
    host_listings_count: 4,
    host_total_listings_count: 5,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: true,
    host_identity_verified: false,
    neighbourhood: 'Boston, Massachusetts, United States',
    neighbourhood_cleansed: 'East Boston',
    neighbourhood_group_cleansed: '',
    latitude: 42.36413,
    longitude: -71.02991,
    property_type: 'Entire rental unit',
    room_type: 'Entire home/apt',
    accommodates: 2,
    bathrooms: '',
    bathrooms_text: '1 bath',
    bedrooms: '',
    beds: 1,
    amenities: [],
    price: '$125.00',
    minimum_nights: 29,
    maximum_nights: 1125,
    minimum_minimum_nights: 29,
    maximum_minimum_nights: 29,
    minimum_maximum_nights: 1125,
    maximum_maximum_nights: 1125,
    minimum_nights_avg_ntm: 29,
    maximum_nights_avg_ntm: 1125,
    calendar_updated: '',
    has_availability: true,
    availability_30: 17,
    availability_60: 17,
    availability_90: 17,
    availability_365: 271,
    calendar_last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    number_of_reviews: 24,
    number_of_reviews_ltm: 0,
    number_of_reviews_l30d: 0,
    first_review: ISODate('2015-07-10T00:00:00.000Z'),
    last_review: ISODate('2022-09-05T00:00:00.000Z'),
    review_scores_rating: 4.96,
    review_scores_accuracy: 5,
    review_scores_cleanliness: 4.96,
    review_scores_checkin: 5,
    review_scores_communication: 4.96,
    review_scores_location: 4.88,
    review_scores_value: 4.92,
    license: '',
    instant_bookable: false,
    calculated_host_listings_count: 1,
    calculated_host_listings_count_entire_homes: 1,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.23
  },
  {
    _id: ObjectId('6610d78facb2cce54b6a8110'),
    id: 5506,
    listing_url: 'https://www.airbnb.com/rooms/5506',
    scrape_id: Long('20231218233145'),
    last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    source: 'city scrape',
    name: 'Guest suite in Boston · ★4.79 · 1 bedroom · 1 bed · 1 bath',
    description: '',
    neighborhood_overview: 'Peaceful, Architecturally interesting, historic, diverse, and quiet residential. <br /><br />Culturally,  ethnically, and economically diverse.',
    picture_url: 'https://a0.muscache.com/pictures/miso/Hosting-5506/original/5c9789c7-abff-49e4-b0de-1ba8b77a9597.jpeg',
    host_id: 8229,
    host_url: 'https://www.airbnb.com/users/show/8229',
    host_name: 'Terry',
    host_since: ISODate('2009-02-19T00:00:00.000Z'),
    host_location: 'Boston, MA',
    host_about: 'Relaxed,  Easy going, Accommodating. ',
    host_response_time: 'within an hour',
    host_response_rate: '100%',
    host_acceptance_rate: '100%',
    host_is_superhost: true,
    host_thumbnail_url: 'https://a0.muscache.com/im/users/8229/profile_pic/1259099341/original.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/users/8229/profile_pic/1259099341/original.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: 'Roxbury',
    host_listings_count: 11,
    host_total_listings_count: 14,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: true,
    host_identity_verified: true,
    neighbourhood: 'Boston, Massachusetts, United States',
    neighbourhood_cleansed: 'Roxbury',
    neighbourhood_group_cleansed: '',
    latitude: 42.32844,
    longitude: -71.09581,
    property_type: 'Entire guest suite',
    room_type: 'Entire home/apt',
    accommodates: 2,
    bathrooms: '',
    bathrooms_text: '1 bath',
    bedrooms: '',
    beds: 1,
    amenities: [],
    price: '$135.00',
    minimum_nights: 3,
    maximum_nights: 90,
    minimum_minimum_nights: 3,
    maximum_minimum_nights: 5,
    minimum_maximum_nights: 1125,
    maximum_maximum_nights: 1125,
    minimum_nights_avg_ntm: 3,
    maximum_nights_avg_ntm: 1125,
    calendar_updated: '',
    has_availability: true,
    availability_30: 0,
    availability_60: 0,
    availability_90: 0,
    availability_365: 87,
    calendar_last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    number_of_reviews: 122,
    number_of_reviews_ltm: 4,
    number_of_reviews_l30d: 0,
    first_review: ISODate('2009-03-21T00:00:00.000Z'),
    last_review: ISODate('2023-11-18T00:00:00.000Z'),
    review_scores_rating: 4.79,
    review_scores_accuracy: 4.88,
    review_scores_cleanliness: 4.9,
    review_scores_checkin: 4.95,
    review_scores_communication: 4.89,
    review_scores_location: 4.55,
    review_scores_value: 4.75,
    license: 'STR-490093',
    instant_bookable: false,
    calculated_host_listings_count: 10,
    calculated_host_listings_count_entire_homes: 10,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.68
  }
]
```

2. show exactly 10 documents in any order, but "prettyprint" in easier to read format, using the `pretty()` function.  
Code:
```
db.listings.find().limit(10).pretty()
```  
Output:  Since 10 documents contain too much details, I just display 3 of them to show the format
```
[
  {
    _id: ObjectId('6610d78facb2cce54b6a810f'),
    id: 3781,
    listing_url: 'https://www.airbnb.com/rooms/3781',
    scrape_id: Long('20231218233145'),
    last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    source: 'city scrape',
    name: 'Rental unit in Boston · ★4.96 · 1 bedroom · 1 bed · 1 bath',
    description: '',
    neighborhood_overview: 'Mostly quiet ( no loud music, no crowed sidewalks)  area with residential 3 story buildings, some 4 and 5 story newer buildings. Though not in an "entertainment" area there are local food shops and supermarket with a mix of restaurants.  Area is in transition--East Boston has a great waterfront with gentrification evident everywhere!',
    picture_url: 'https://a0.muscache.com/pictures/24670/b2de0442_original.jpg',
    host_id: 4804,
    host_url: 'https://www.airbnb.com/users/show/4804',
    host_name: 'Frank',
    host_since: ISODate('2008-12-03T00:00:00.000Z'),
    host_location: 'Massachusetts, United States',
    host_about: 'My wife and I and grown children frequently occupy the spaces that we rent and as such try to make the spaces pleasant and appealing to ourselves as well as guests.   We have been subletting for over 15 years and consider ourselves helpful and organized hosts who provide clean, attractive and comfortable apartments',
    host_response_time: 'within a day',
    host_response_rate: '90%',
    host_acceptance_rate: '29%',
    host_is_superhost: true,
    host_thumbnail_url: 'https://a0.muscache.com/im/users/4804/profile_pic/1327953150/original.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/users/4804/profile_pic/1327953150/original.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: 'East Boston',
    host_listings_count: 4,
    host_total_listings_count: 5,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: true,
    host_identity_verified: false,
    neighbourhood: 'Boston, Massachusetts, United States',
    neighbourhood_cleansed: 'East Boston',
    neighbourhood_group_cleansed: '',
    latitude: 42.36413,
    longitude: -71.02991,
    property_type: 'Entire rental unit',
    room_type: 'Entire home/apt',
    accommodates: 2,
    bathrooms: '',
    bathrooms_text: '1 bath',
    bedrooms: '',
    beds: 1,
    amenities: [],
    price: '$125.00',
    minimum_nights: 29,
    maximum_nights: 1125,
    minimum_minimum_nights: 29,
    maximum_minimum_nights: 29,
    minimum_maximum_nights: 1125,
    maximum_maximum_nights: 1125,
    minimum_nights_avg_ntm: 29,
    maximum_nights_avg_ntm: 1125,
    calendar_updated: '',
    has_availability: true,
    availability_30: 17,
    availability_60: 17,
    availability_90: 17,
    availability_365: 271,
    calendar_last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    number_of_reviews: 24,
    number_of_reviews_ltm: 0,
    number_of_reviews_l30d: 0,
    first_review: ISODate('2015-07-10T00:00:00.000Z'),
    last_review: ISODate('2022-09-05T00:00:00.000Z'),
    review_scores_rating: 4.96,
    review_scores_accuracy: 5,
    review_scores_cleanliness: 4.96,
    review_scores_checkin: 5,
    review_scores_communication: 4.96,
    review_scores_location: 4.88,
    review_scores_value: 4.92,
    license: '',
    instant_bookable: false,
    calculated_host_listings_count: 1,
    calculated_host_listings_count_entire_homes: 1,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.23
  },
  {
    _id: ObjectId('6610d78facb2cce54b6a8110'),
    id: 5506,
    listing_url: 'https://www.airbnb.com/rooms/5506',
    scrape_id: Long('20231218233145'),
    last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    source: 'city scrape',
    name: 'Guest suite in Boston · ★4.79 · 1 bedroom · 1 bed · 1 bath',
    description: '',
    neighborhood_overview: 'Peaceful, Architecturally interesting, historic, diverse, and quiet residential. <br /><br />Culturally,  ethnically, and economically diverse.',
    picture_url: 'https://a0.muscache.com/pictures/miso/Hosting-5506/original/5c9789c7-abff-49e4-b0de-1ba8b77a9597.jpeg',
    host_id: 8229,
    host_url: 'https://www.airbnb.com/users/show/8229',
    host_name: 'Terry',
    host_since: ISODate('2009-02-19T00:00:00.000Z'),
    host_location: 'Boston, MA',
    host_about: 'Relaxed,  Easy going, Accommodating. ',
    host_response_time: 'within an hour',
    host_response_rate: '100%',
    host_acceptance_rate: '100%',
    host_is_superhost: true,
    host_thumbnail_url: 'https://a0.muscache.com/im/users/8229/profile_pic/1259099341/original.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/users/8229/profile_pic/1259099341/original.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: 'Roxbury',
    host_listings_count: 11,
    host_total_listings_count: 14,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: true,
    host_identity_verified: true,
    neighbourhood: 'Boston, Massachusetts, United States',
    neighbourhood_cleansed: 'Roxbury',
    neighbourhood_group_cleansed: '',
    latitude: 42.32844,
    longitude: -71.09581,
    property_type: 'Entire guest suite',
    room_type: 'Entire home/apt',
    accommodates: 2,
    bathrooms: '',
    bathrooms_text: '1 bath',
    bedrooms: '',
    beds: 1,
    amenities: [],
    price: '$135.00',
    minimum_nights: 3,
    maximum_nights: 90,
    minimum_minimum_nights: 3,
    maximum_minimum_nights: 5,
    minimum_maximum_nights: 1125,
    maximum_maximum_nights: 1125,
    minimum_nights_avg_ntm: 3,
    maximum_nights_avg_ntm: 1125,
    calendar_updated: '',
    has_availability: true,
    availability_30: 0,
    availability_60: 0,
    availability_90: 0,
    availability_365: 87,
    calendar_last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    number_of_reviews: 122,
    number_of_reviews_ltm: 4,
    number_of_reviews_l30d: 0,
    first_review: ISODate('2009-03-21T00:00:00.000Z'),
    last_review: ISODate('2023-11-18T00:00:00.000Z'),
    review_scores_rating: 4.79,
    review_scores_accuracy: 4.88,
    review_scores_cleanliness: 4.9,
    review_scores_checkin: 4.95,
    review_scores_communication: 4.89,
    review_scores_location: 4.55,
    review_scores_value: 4.75,
    license: 'STR-490093',
    instant_bookable: false,
    calculated_host_listings_count: 10,
    calculated_host_listings_count_entire_homes: 10,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.68
  },
  {
    _id: ObjectId('6610d78facb2cce54b6a8111'),
    id: 6695,
    listing_url: 'https://www.airbnb.com/rooms/6695',
    scrape_id: Long('20231218233145'),
    last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    source: 'city scrape',
    name: 'Condo in Boston · ★4.81 · Studio · 2 beds · 1 bath',
    description: '',
    neighborhood_overview: 'Peaceful, Architecturally interesting, historic, diverse, and quiet. Racially, culturally,  ethnic, and economically diverse.',
    picture_url: 'https://a0.muscache.com/pictures/38ac4797-e7a4-48d8-84a5-e1f724f4282b.jpg',
    host_id: 8229,
    host_url: 'https://www.airbnb.com/users/show/8229',
    host_name: 'Terry',
    host_since: ISODate('2009-02-19T00:00:00.000Z'),
    host_location: 'Boston, MA',
    host_about: 'Relaxed,  Easy going, Accommodating. ',
    host_response_time: 'within an hour',
    host_response_rate: '100%',
    host_acceptance_rate: '100%',
    host_is_superhost: true,
    host_thumbnail_url: 'https://a0.muscache.com/im/users/8229/profile_pic/1259099341/original.jpg?aki_policy=profile_small',
    host_picture_url: 'https://a0.muscache.com/im/users/8229/profile_pic/1259099341/original.jpg?aki_policy=profile_x_medium',
    host_neighbourhood: 'Roxbury',
    host_listings_count: 11,
    host_total_listings_count: 14,
    host_verifications: "['email', 'phone']",
    host_has_profile_pic: true,
    host_identity_verified: true,
    neighbourhood: 'Boston, Massachusetts, United States',
    neighbourhood_cleansed: 'Roxbury',
    neighbourhood_group_cleansed: '',
    latitude: 42.32802,
    longitude: -71.09387,
    property_type: 'Entire condo',
    room_type: 'Entire home/apt',
    accommodates: 4,
    bathrooms: '',
    bathrooms_text: '1 bath',
    bedrooms: '',
    beds: 2,
    amenities: [],
    price: '$179.00',
    minimum_nights: 3,
    maximum_nights: 730,
    minimum_minimum_nights: 3,
    maximum_minimum_nights: 3,
    minimum_maximum_nights: 730,
    maximum_maximum_nights: 730,
    minimum_nights_avg_ntm: 3,
    maximum_nights_avg_ntm: 730,
    calendar_updated: '',
    has_availability: true,
    availability_30: 0,
    availability_60: 0,
    availability_90: 18,
    availability_365: 107,
    calendar_last_scraped: ISODate('2023-12-19T00:00:00.000Z'),
    number_of_reviews: 127,
    number_of_reviews_ltm: 4,
    number_of_reviews_l30d: 0,
    first_review: ISODate('2009-08-06T00:00:00.000Z'),
    last_review: ISODate('2023-10-28T00:00:00.000Z'),
    review_scores_rating: 4.81,
    review_scores_accuracy: 4.82,
    review_scores_cleanliness: 4.87,
    review_scores_checkin: 4.9,
    review_scores_communication: 4.95,
    review_scores_location: 4.51,
    review_scores_value: 4.71,
    license: 'STR-491702',
    instant_bookable: false,
    calculated_host_listings_count: 10,
    calculated_host_listings_count_entire_homes: 10,
    calculated_host_listings_count_private_rooms: 0,
    calculated_host_listings_count_shared_rooms: 0,
    reviews_per_month: 0.73
  }
]
```
3. choose two hosts (by reffering to their `host_id` values) who are superhosts (available in the `host_is_superhost` field), and show all of the listings offered by both of the two hosts
   - only show the `name`, `price`, `neighbourhood`, `host_name`, and `host_is_superhost` for each result
Code:
```
db.listings.find({ $or: [{ host_id: 4804 }, { host_id: 49383 }] }, { name: 1, price: 1, neighbourhood: 1, host_name: 1, host_is_superhost: 1 })
```
Output:  
```
[
  {
    _id: ObjectId('6610d78facb2cce54b6a810f'),
    name: 'Rental unit in Boston · ★4.96 · 1 bedroom · 1 bed · 1 bath',
    host_name: 'Frank',
    host_is_superhost: true,
    neighbourhood: 'Boston, Massachusetts, United States',
    price: '$125.00'
  },
  {
    _id: ObjectId('6610d790acb2cce54b6a8a62'),
    name: 'Rental unit in Boston · 3 bedrooms · 3 beds · 1.5 baths',
    host_name: 'Tom',
    host_is_superhost: true,
    neighbourhood: 'Boston, Massachusetts, United States',
    price: '$198.00'
  }
]
```
Insight:  
This query helps us just focus on 2 specific superhosts, which can show detailed information of one individuals. If the superhosts own more than one room, we can also see all the rooms in a collection.  

4. find all the unique `host_name` values (see [the docs](https://docs.mongodb.com/manual/reference/method/db.collection.distinct/))
Code:
```
db.listings.distinct("host_name")
```
Output:  
```
[
  'A Delightful Hotel', 'Aanchal',     'Aaron',
  ... 738 more items
]
```
Insights: This code selects only distinct hosts' name, and show the total numbers of distinct hosts as well.

5. find all of the places that have more than 2 `beds` in a neighborhood of your choice (referred to as either the `neighborhood` or `neighbourhood_group_cleansed` fields in the data file), ordered by `review_scores_rating` descending
   - only show the `name`, `beds`, `review_scores_rating`, and `price`
   - if your data set only has blanks for all the neighborhood-related fields, or only one neighborhood value in all documents, you may pick another field to filter by - include an explanation and justification for this in your report.
   - if you run out of memory for this query, try filtering `review_scores_rating` that aren't empty (`$ne`); and lastly, if there's still an issue, you can set the `beds` to match exactly 2.
  
Code:   
```
db.listings.find(
  {"beds": { "$gt": 2 }, "neighbourhood": "Boston, Massachusetts, United States", "review_scores_rating": { "$ne": null }},{ "name": 1, "beds": 1, "review_scores_rating": 1, "price": 1 }).sort({ "review_scores_rating": -1 })
```
Output:  
```
[
  {
    _id: ObjectId('6610d78facb2cce54b6a81c0'),
    name: 'Townhouse in Boston · ★5.0 · 3 bedrooms · 4 beds · 2.5 baths',
    beds: 4,
    price: '$900.00',
    review_scores_rating: 5
  },
  {
    _id: ObjectId('6610d78facb2cce54b6a81d1'),
    name: 'Home in Boston · 2 bedrooms · 3 beds · 2 baths',
    beds: 3,
    price: '',
    review_scores_rating: 5
  },
  {
    _id: ObjectId('6610d78facb2cce54b6a81d8'),
    name: 'Rental unit in Boston · ★5.0 · 1 bedroom · 3 beds · 1 bath',
    beds: 3,
    price: '$136.00',
    review_scores_rating: 5
  }
]
```
Insights: This sorts the airbnb in a specific neighborhood, but with a broad limitations (eqaul or greater than 2 beds), this provides us with multiple options.

6. show the number of listings per host
Code:
```
 db.listings.aggregate([ { "$group": { "_id": "$host_id", "count": { "$sum": 1 } } } ])
```
Output:
```
[
  { _id: 127551415, count: 1 },
  { _id: 142029634, count: 1 },
  { _id: 69267172, count: 9 },

]
```
Insights: We can know how many airbnb does one host own, if the customer prefer one host's room, we can check if the host has more options to choose.

7. find the average `review_scores_rating` per neighborhood, and only show those that are `4` or above, sorted in descending order of rating.

Code:
```
db.listings.aggregate([ { "$match": { "review_scores_rating": { "$gte": 4 } } },{ "$group": { "_id": "$neighbourhood", "averageRating": { "$avg": "$review_scores_rating" } } }, { "$match": { "averageRating": { "$gte": 4 } } }, { "$sort": { "averageRating": -1 } } ])
```
Output:  
```
[
  { _id: 'Boston, , Massachusetts, United States', averageRating: 5 },
  {
    _id: 'Boston/Charlestown , Massachusetts, United States',
    averageRating: 5
  },
  { _id: 'Boston, Ma , United States', averageRating: 5 },
  { _id: 'Boston, Allston, Ma, United States', averageRating: 5 },
  { _id: ' Boston, Massachusetts, United States', averageRating: 4.97 },
  { _id: 'Dedham, Massachusetts, United States', averageRating: 4.95 },
]
```
Insights: Based on all the results, noticed that the last one who gets a score is '4' or above gets 4.695, which means that there is a huge gap between 4 to 4.695.   
A minimum average rating of 4.695 suggests that the majority of listings (or at least those above the lowest average score considered) maintain a high standard of quality. This could indicate that hosts are generally providing excellent service, cleanliness, accuracy in listings, and overall guest satisfaction.
