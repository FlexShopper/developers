### FlexFeed Product Import

##### Filename

`*.csv` `*.tsv`

##### Fields
`id` unique id for product *REQUIRED*

`condition` - (new|refurbished) *REQUIRED*

`title` title of product *REQUIRED*

`description` description of product, can contain html

`images` semicolon-separated images

`price` *REQUIRED*

`path` - `Categories/Paths/Specific Path` *REQUIRED*

`mpn` - *REQUIRED*

`brand` - brand name with capitalization etc *REQUIRED*

`qty` - quantity *REQUIRED*

`weight` - weight, as a float in LBs (ex `9.99`) *REQUIRED if using API shipping*

`msrp`

`height` - height, as a float in inches

`depth` - depth, as a float in inches

`width` - width, as a float in inches

`attributes` - attributes and their values, double joined. Example: `amps^50~volts^120` 

`warranty` - warranty

`inTheBox` - what's in the box

`specs` - specifications

`pdfs` - semicolon separated pdf links

`marketingText` - marketing words, will be indexed for search

`features` - features

`categoryCode` - *Wholesale Vendors Only* type of item being sold (appliances|computers|electronics|furniture|jewelry|other|no-category)


##### Shipping

`handling` - int, number of handling days from PO to shipped

`UPS_API_GND` - boolean, offer Ground via UPS API. Source zip should be configured with your merchant account.

`UPS_API_2DA` - boolean, offer 2 Day Air via UPS API. Source zip should be configured with your merchant account.

`GND_SHIP_PRICE` - float, offer Ground flat-rate at this price

`2DA_SHIP_PRICE` - float, offer 2 Day Air flat-rate at this price

`CUSTOM_SHIP` - string, specify custom shipping options as `METHOD@PRICE`, e.g. `Drone Delivery@9.99`. `Method` will refer
to a shipping method configured with your merchant profile
