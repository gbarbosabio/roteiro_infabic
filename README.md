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

Fazer um de cada vez

	
