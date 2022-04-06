Add Polygon programmatically

```
   var drawPolygon= new L.Draw.Polygon(map, {showArea:true});
   drawPolygon.enable();
```


Initialize Edit Layer

```
var  drawnItems = L.featureGroup().addTo(map);
var  editor= new L.EditToolbar.Edit(map, {
					featureGroup: drawnItems
				})
        
```

Edit layer
```
editor.enable();
```

Save After Edit
```
 editor.save();
 editor.disable();  
```
