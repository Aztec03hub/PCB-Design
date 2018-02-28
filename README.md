## PCB Design Repo

###### Templates 

For these, go into `C:\Users\Public\Documents\Altium\AD17\Templates` or wherever your path is.

###### Rules 

For these, go to `Design > Rules... > Right-click 'Design Rules' at the top-left, choose 'Import Rules...'` and import them. MAKE SURE YOU BACK YOUR OWN RULES UP FIRST!!!

###### Stackup(s)

For these, go to `Design > Layer Stack Manager > Load... > Load from File...`

###### Notes on the rules file:

I use a LOT of Altium's Query Language. I *have* had issues before trying to import Rules using Query Syntax which points towards identifiers which don't exist.

So, let me know if this is an issue!

Things to look at: (I'll use my actual rule names)

* ThermalViasShrtCkt

* UnRoutedNet (You'll probably want to enable 'Check for incomplete connections')

* RoutingCorners

* All 'Fanout' Rules

* ThermalVias

* PolygonConnect


For ThermalVias:

First Object Matches: `(OnLayer('Ground Plane') OR OnLayer('Power Plane'))`

You'll need to have your layers named `Ground Plane` and `Power Plane` for this to work!

Second Object Matches: `(IsVia) OR (PadViaLibraryTemplate = 'c150h90')`

You'll have to determine the Pad Template identifier. (You can simply do this by double clicking the middle of your most-used vias)

Finally, all rules and clearances were originally calculated for OSHPark's 4-layer service, and honed/refined overtime for some VERY tight (Read as: close to manufacturing tolerances) values. I've not had any issues yet.

## Check these guys out

[OSH Park](https://www.oshpark.com/) - for those "Perfect Purple PCB's!"

[Imagineering Inc.](http://www.pcbnet.com/) - I use these guys for production runs. They are VERY competitive, offer full-turnkey, and the quality is AMAZING!