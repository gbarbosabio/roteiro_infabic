# roteiro_infabic
Roteiro aula prática II &amp; III

Download dataset de núcleo

https://bbbc.broadinstitute.org/BBBC039

Contagem de células manual

Intensidade de fluorescencia pixel (manual)

Plot profile (manual)

Area measurement (manual)


#Gambiarra

rename("image");

run("Duplicate...", " ");


#Segmentação

setOption("BlackBackground", false);

run("Convert to Mask");

run("Fill Holes");

run("Close-");

run("Open");

run("Watershed");

run("Analyze Particles...", "size=70-Infinity exclude add");


Medidas

close();

selectImage("image");

roiManager("multi-measure measure_all append");

roiManager("Delete");

selectImage("image");

close();



Plotting



Download dataset medida de fluorescência nuclear

https://bbbc.broadinstitute.org/BBBC013

Load Folder

Stack > Hiperstack
	XYZCT
	2channel
	96zstacks


Fazer tudo

Ver o dado

Data science Software de planilhas > R e Python


Download data:  https://zenodo.org/record/7246536/files/LifeAct__0001.oir%20-%20C%3D0.tif?download=1

Download tool:  https://zenodo.org/record/5787143/files/gbarbosabio/Cytoneme_dynamics-V1.0.zip?download=1


Macro citonemas

```
run("Z Project...", "projection=[Max Intensity] all");
run("Grays");
run("Invert LUT");
//run("Brightness/Contrast...");
run("Apply LUT", "stack");
```




Fazer um de cada vez

	
