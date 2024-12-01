# JavaScript
//JavaScript module 1 show options as per requirements

var FieldName1 = "Glass Type";
var FieldName2 = "InterLayer";
var FieldName3 = "CABLENET";
var FieldName4 = "PICKET";
var FieldName5 = "WIRE MESH";
var FieldName6 = "PERFORATED METAL";
var FieldName7 = "PMaterial";
var FieldName8 = "PFinish";
var FieldName9 = "PPassivation";
var FieldName10 = "LED COLOR";
var FieldName11 = "LED INTENSITY";
var FieldName12 = "LED ORIENTATION";
var FieldName13 = "LED LENS";
var FieldName14 = "WOODRAIL";


if (this.getField("INFILL").value==1 || this.getField("INFILL").value==2) {
this.getField(FieldName1).display = display.visible;
this.getField(FieldName2).display = display.visible;
this.getField(FieldName3).display = display.hidden;
this.getField(FieldName4).display = display.hidden;
this.getField(FieldName5).display = display.hidden;
this.getField(FieldName6).display = display.hidden;
this.getField(FieldName7).display = display.hidden;
this.getField(FieldName8).display = display.hidden;
this.getField(FieldName9).display = display.hidden;
} else if (this.getField("INFILL").value==3 || this.getField("INFILL").value==4) {
this.getField(FieldName1).display = display.hidden;
this.getField(FieldName2).display = display.hidden;
this.getField(FieldName3).display = display.hidden;
this.getField(FieldName4).display = display.hidden;
this.getField(FieldName5).display = display.hidden;
this.getField(FieldName6).display = display.visible;
this.getField(FieldName7).display = display.visible;
this.getField(FieldName8).display = display.visible;
this.getField(FieldName9).display = display.visible;
} else if (this.getField("INFILL").value==5 || this.getField("INFILL").value==6) {
this.getField(FieldName1).display = display.hidden;
this.getField(FieldName2).display = display.hidden;
this.getField(FieldName3).display = display.hidden;
this.getField(FieldName4).display = display.hidden;
this.getField(FieldName5).display = display.visible;
this.getField(FieldName6).display = display.hidden;
this.getField(FieldName7).display = display.visible;
this.getField(FieldName8).display = display.visible;
this.getField(FieldName9).display = display.visible;
} else if (this.getField("INFILL").value==7 || this.getField("INFILL").value==8) {
this.getField(FieldName1).display = display.hidden;
this.getField(FieldName2).display = display.hidden;
this.getField(FieldName3).display = display.hidden;
this.getField(FieldName4).display = display.hidden;
this.getField(FieldName5).display = display.hidden;
this.getField(FieldName6).display = display.hidden;
this.getField(FieldName7).display = display.hidden;
this.getField(FieldName8).display = display.hidden;
this.getField(FieldName9).display = display.hidden;
} else if (this.getField("INFILL").value==9) {
this.getField(FieldName1).display = display.hidden;
this.getField(FieldName2).display = display.hidden;
this.getField(FieldName3).display = display.hidden;
this.getField(FieldName4).display = display.visible;
this.getField(FieldName5).display = display.hidden;
this.getField(FieldName6).display = display.hidden;
this.getField(FieldName7).display = display.hidden;
this.getField(FieldName8).display = display.hidden;
this.getField(FieldName9).display = display.hidden;
} else if (this.getField("INFILL").value==10 || this.getField("INFILL").value==11) {
this.getField(FieldName1).display = display.hidden;
this.getField(FieldName2).display = display.hidden;
this.getField(FieldName3).display = display.visible;
this.getField(FieldName4).display = display.hidden;
this.getField(FieldName5).display = display.hidden;
this.getField(FieldName6).display = display.hidden;
this.getField(FieldName7).display = display.visible;
this.getField(FieldName8).display = display.visible;
this.getField(FieldName9).display = display.visible;
} 


if (this.getField("TOP RAIL").value==5 || this.getField("HAND RAIL").value==5) {
this.getField(FieldName10).display = display.visible;
this.getField(FieldName11).display = display.visible;
this.getField(FieldName12).display = display.visible;
this.getField(FieldName13).display = display.visible;
} else {
this.getField(FieldName10).display = display.hidden;
this.getField(FieldName11).display = display.hidden;
this.getField(FieldName12).display = display.hidden;
this.getField(FieldName13).display = display.hidden;
}

if (this.getField("HAND RAIL").value==3 || this.getField("HAND RAIL").value==4 || this.getField("TOP RAIL").value==4) {
this.getField(FieldName14).display = display.visible;
} else {
this.getField(FieldName14).display = display.hidden;
}


//JavaScript module 2 show content as per options selected

var layers = this.getOCGs();
for (var i in layers) {
if (layers[i].name!="0") {
layers[i].state = 0;
}
}
if (this.getField("MOUNTING").value==1) {
var layerName = "MOUNT TOP";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("MOUNTING").value==2) {
var layerName = "MOUNT FASCIA";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==1) {
var layerName = "INFILL - GLASS SPIDER";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==2) {
var layerName = "INFILL - GLASS CLAMP";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==3) {
var layerName = "INFILL - PERF SPIDER";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==4) {
var layerName = "INFILL - PERF CLAMP";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==5) {
var layerName = "INFILL - MESH SPIDER";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==6) {
var layerName = "INFILL - MESH CLAMP";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==7) {
var layerName = "INFILL - MULTILINE";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}

if (this.getField("INFILL").value==8) {
var layerName = "INFILL - CABLE";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}

if (this.getField("INFILL").value==9) {
var layerName = "INFILL - PICKET";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==10) {
var layerName = "INFILL - CABLENET PANEL";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("INFILL").value==11) {
var layerName = "INFILL - CABLENET CONTINUOUS";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("TOP RAIL").value==1) {
var layerName = "TOP RAIL - 2 DIA SS";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("TOP RAIL").value==2) {
var layerName = "TOP RAIL - 1.5 DIA SS";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("TOP RAIL").value==3) {
var layerName = "TOP RAIL - 1x2 SS";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("TOP RAIL").value==4) {
var layerName = "TOP RAIL - 2 DIA WOOD";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("TOP RAIL").value==5) {
var layerName = "TOP RAIL - iRAIL";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("HAND RAIL").value==1) {
var layerName = "HAND RAIL - 1.5 DIA SS";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("HAND RAIL").value==2) {
var layerName = "HAND RAIL - 2 DIA SS";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("HAND RAIL").value==3) {
var layerName = "HAND RAIL - 1.5 DIA WOOD";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("HAND RAIL").value==4) {
var layerName = "HAND RAIL - 2 DIA WOOD";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
if (this.getField("HAND RAIL").value==5) {
var layerName = "HAND RAIL - iRAIL";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}


//JavaScript module 3 show content as per options selected


var layers = this.getOCGs();

if (this.getField("INFILL").value==3 || this.getField("INFILL").value==4) {
if (this.getField("PERFORATED METAL").value==1) {
var layerName = "PP-PMRO-0610";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("PERFORATED METAL").value==2) {
var layerName = "PP-PMRO-1014";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("PERFORATED METAL").value==3) {
var layerName = "PP-PMRO-1217";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("PERFORATED METAL").value==4) {
var layerName = "PP-PMSQ-1013";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("PERFORATED METAL").value==5) {
var layerName = "PP-PMSL-0325";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("PERFORATED METAL").value==6) {
var layerName = "PP-PMSL-1122";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
}
}
}
}
}
}





if (this.getField("INFILL").value==5 || this.getField("INFILL").value==6) {
if (this.getField("WIRE MESH").value==1) {
var layerName = "WM-10";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==2) {
var layerName = "WM-11";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==3) {
var layerName = "WM-12";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==4) {
var layerName = "WM-13";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==5) {
var layerName = "WM-14";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==6) {
var layerName = "WM-15";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==7) {
var layerName = "WM-17";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==8) {
var layerName = "WM-19";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==9) {
var layerName = "WM-20";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
} else {
if (this.getField("WIRE MESH").value==10) {
var layerName = "WM-21";
for (var i in layers) {
if (layers[i].name==layerName) {
layers[i].state = 1;
}
}
}
}
}
}
}
}
}
}
}
}
}



//JavaScript module 4 Keep default layers state as per latest saves stage or selection

var layers = this.getOCGs();

for (var i in layers)
{
	if (layers[i].state = 0)
	{
	(layers[i].initState = 0);
	}

	else
	{
	(layers[i].initState = 1);
	}
}
