Initialization Drawer for Polygon

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

Simulation, load polygon from database, and edit

```
 function addPolygon(){
        // from database
        var latlngs = [
            [17.385044, 78.486671],
            [16.506174, 80.648015],
            [17.686816, 83.218482]
            ];
            var polygon = L.polygon(latlngs, {color: 'red'});
            polygon.addTo(drawnItems);
            editor.enable();  
    }
```    
