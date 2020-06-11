## search hospital happy path
* greet
 - utter_greet
 - utter_how_can_i_help
* search_provider{"facility_type":"hospital","location":"kerala"}
 - action_facility_search
 - slot{"address":"avenue hill bridge,kerala"}
* thanks
 - utter_goodbye

## search hospital + location
* greet
 - utter_greet
* search_provider{"facility_type":"hospital"}
 - utter_ask_location
* inform{"location":"kerala"}
 - action_facility_search
 - slot{"address":"avenue hill bridge,kerala"}
* thanks
 - utter_goodbye

## story_thankyou
* thankyou
    - utter_noworries
    
## happy path
* greet
  - utter_greet
* mood_great
  - utter_happy

## sad path 1
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* affirm
  - utter_happy

## sad path 2
* greet
  - utter_greet
* mood_unhappy
  - utter_cheer_up
  - utter_did_that_help
* deny
  - utter_goodbye

## say goodbye
* goodbye
  - utter_goodbye

## bot challenge
* bot_challenge
  - utter_iamabot
