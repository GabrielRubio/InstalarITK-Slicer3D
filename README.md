# Instalação:

##  Instalar nessa ordem:
	* VTK
	* ITK
	* 3D Slicer

## Instalado CMAKE
<p>
	sudo apt-get install cmake
</p>

## Instalado openGL
<p>
	sudo apt-get install freeglut3-dev
</p>

## Cria-se a pasta general_source
<p>
	mkdir general_source
	cd general_source
</p>

## Na pasta general_source cria-se a pasta VTK
<p>
	mkdir VTK
	cd VTK
</p>

## Criando as pastas de source e build
<p>
	mkdir source 
	mkdir build
</p>

## Na pasta de source clonando o vtk 7.1.1
<p>
	git clone git://vtk.org/VTK.git
</p>
Ou baixar os arquivos do site 

## Na pasta de build usando cmake cria os arquivos de build
<p>
	cmake ~/VTK/source/
	ou
	cmake gui
</p>

## No Cmake, limpa o cache;
Vá para a pasta 
<p>
	~/vtk/source e ~/vtk/build
	use configure e generate
</p>

## Na pasta build dar make
	O numero de cores que seu processador tem deve ser colocad nessa etapa, o nosso possui 4 cores então [-j4].
<p>
	make [-j4] 
</p>

## Na pasta general_source cria-se a pasta ITK
<p>
	mkdir ITK
	cd ITK
</p>

## Criando as pastas de source e build
<p>
	mkdir source 
	mkdir build
</p>

## Na pasta de source clonando o itk 4.12.1
* ou baixando os arquivos do site 

## Na pasta de build usando cmake cria os arquivos de build
<p>
	cmake ~/VTK/source/

	ou use o cmake gui
</p>

## No Cmake, limpa o cache;

Vá para a pasta ~/itk/source e ~/itk/build

Use configure e Adiciona as variáveis:
* ====> Module_ITKVtkGlue                ON

* ====> VTK_DIR                          /opt/compilation/paraview-git_build/VTK/

* configure novamente e generate

## Na pasta build dar make
<p>
	make [-j4]
</p>

## Na pasta build
<p>
	sudo make install 
</p>

## [Instalar 3D Slicer](https://www.slicer.org/wiki/Documentation/Nightly/Developers/Build_Instructions#Ubuntu)

