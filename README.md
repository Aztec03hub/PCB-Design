# PCB Design Repo

#### Layer-Sets

I've only included a 4-layer set. Some rules reference specific layer names.

Go to `Design > Manage Layer Sets > Board Layer Sets` and select `Import Layer Sets From File...`

#### Libraries

I've included a few libraries for anyone to use. I *think* I included everything needed. To install, just double-click the appropriate `.IntLib` file in `Project Outputs`

I created `tm4cv006lib` around 3.5 years ago, and `Conscious_IntLib` much more recently. The Conscious one should be pretty tight.

#### Open Source Projects

That directory has its own README, so go check it out.

#### Rules

Go to `Design > Rules... > Right-click 'Design Rules' at the top-left, choose 'Import Rules...'` and import them. MAKE SURE YOU BACK YOUR OWN RULES UP FIRST!!!

#### Stackup(s)

Go to `Design > Layer Stack Manager > Load... > Load from File...`

#### Templates

Copy into `C:\Users\Public\Documents\Altium\AD17\Templates` or wherever your path is. This is for starting new projects!

#### Notes on the rules file:

I use a LOT of Altium's Query Language. I *have* had issues before trying to import Query Syntax Rules which point toward identifiers/labels which don't exist. Be aware.

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

Finally, all rules and clearances were originally calculated for OSHPark's 4-layer service, and honed/refined overtime for some *VERY* tight (**Read as:** close to manufacturing tolerances) values. I've not had any issues yet.

## Check these guys out

[OSH Park](https://www.oshpark.com/) - for those "Perfect Purple PCB's!"

[Imagineering Inc.](http://www.pcbnet.com/) - I use these guys for production runs. They are VERY competitive, offer full-turnkey, and the quality is AMAZING!
