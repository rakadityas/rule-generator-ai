# rule-generator-ai

## Demo
Demo: https://drive.google.com/file/d/1NSTAya85oXUSUV4lBTmra6W1pvlS69vs/view?usp=sharing

## Directories
- Source Data -> ER representation. This script will generate _transaction_rules_.
- main.ipynb -> main files complete with how to run. 

## Samples

**Input:**
SCENARIO calculate cashback to bitcoins for marketplace
GIVEN a total product price
THEN give a 10% cashback up to 25000 based on total product price

**Output:** 
[{"id":0,"rule_types_id":123,"data_type_id":14,"name":"With percentage amount 10% and maximum cashback amount Rp25.000,- based on Total Product Price Cashback To bitcoins","client_id":123,"json_rules":"{\"name\":\"cashback_points\",\"fields\":[{\"name\":\"cashback_topcash_type\",\"value\":\"2\",\"fields\":[{\"name\":\"cashback_topcash_value\",\"value\":\"10\"},{\"name\":\"cashback_topcash_maximum\",\"value\":\"25000\"}]},{\"name\":\"data_type\",\"value\":\"14\"},{\"name\":\"cashback_to\",\"value\":\"bitcoins\"}]}"}]


-——-

**Input:**
SCENARIO calculate cashback to bitcoins for digital
GIVEN a total recharge price
THEN give a 50% cashback up to 20000 based on total recharge price

**Output:** 
[{"id":0,"rule_types_id":123,"data_type_id":20,"name":"With percentage amount 50% and maximum cashback amount Rp20.000,- based on Total Recharge Price Cashback To bitcoins","client_id":124,"json_rules":"{\"name\":\"cashback_points\",\"fields\":[{\"name\":\"cashback_topcash_type\",\"value\":\"2\",\"fields\":[{\"name\":\"cashback_topcash_value\",\"value\":\"50\"},{\"name\":\"cashback_topcash_maximum\",\"value\":\"20000\"}]},{\"name\":\"data_type\",\"value\":\"20\"},{\"name\":\"cashback_to\",\"value\":\"bitcoins\"}]}"}]
In [ ]:

———

**Input:**
SCENARIO validate shipping courier for marketplace
GIVEN a courier fields 
WHEN courier is Courier Y
THEN return success

**Output:** 
[{"id":0,"rule_types_id":39,"data_type_id":36,"name":"Valid courier Courier Y","client_id":123,"json_rules":"{\"name\":\"valid_shipping_courier\",\"fields\":[{\"name\":\"valid_shipping_courier_list\",\"value\":\"2\"},{\"name\":\"valid_shipping_courier_description\",\"value\":\"Courier Y\"},{\"name\":\"data_type\",\"value\":\"36\"}]}"}]
