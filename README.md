<p align="center">

  <img src="https://jdleongomez.info/es/post/obs/featured_hudf232787d052df25f3930e83087b41d6_448033_720x0_resize_lanczos_2.png" height="100" />
</p>


## Configuración y aplicación de perfiles para OBS Studio

Este batch fue hecho para las personas que juegan y quieren hacer transmisiones de video, grabar o tomar clips sin ninguna interrupción dentro de su juego, para eso he creado este batch que descarga OBS Studio, configura de acuerdo a tus gráficos y deja todo listo.

   Para que este lote funcione, debe colocar todo el comando de instalación en CMD, si está utilizando __Powershell 2.0__, no podrá usarlo porque no hay WebRequest o DownloadFile, que es la forma que utiliza para descargar los archivos necesarios. .

### Instalación  🤖
Para ejecutar este script es tan sencillo como abrir el CMD y poner lo siguiente:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/wyalexz/OBS-Studio/releases/download/Complements/OBS.Studio.US.bat" -OutFile "$env:temp\OBS.bat"; Start-process $env:temp\OBS.bat
```

### Instalación Manual 🔧
Para la instalación y configuración manual tendremos que instalar [OBS Studio](https://cdn-fastly.obsproject.com/downloads/OBS-Studio-27.2.4-Full-Installer-x64.exe) y realizar los siguientes pasos después de la instalación de OBS y ejecutarlo solo una vez. 
Descargaremos los complementos necesarios:

* [AmdOBS](https://github.com/wyalexzz/OBS/releases/download/Complements/AmdOBS.7z) Todo el contenido debe ser reemplazado en %appdata%\obs-studio
* [NvidiaOBS](https://github.com/wyalexzz/OBS/releases/download/Complements/NvidaOBS.7z) Todo el contenido debe ser reemplazado en %appdata%\obs-studio
* [FilesOBS](https://github.com/wyalexzz/OBS/releases/download/Complements/FilesOBS.7z) Todo el contenido debe ser reemplazado en %programfiles%\obs-studio\data\obs-studio

### Custom LUTs filters creados by [Gaming Careers](https://www.youtube.com/channel/UClx4eJ_EP9MJdz19JUjKD1w) & [Jordan Wages](https://obsproject.com/forum/threads/free-lut-filter-pack.78307/#post-330293) 🎲
Descargue y aplique filtros personalizados de LUT para la cámara:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/wyalexz/OBS-Studio/releases/download/Complements/InstallLUTs.bat"; Start-process $env:temp\InstallLUTs.bat.bat
```

### ReplayBuffer AutoStart 🔗
Para que OBS Studio ReplayBuffer se inicie automáticamente cuando encienda su PC, deberá ejecutar este script a través de CMD:
```
powershell Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; Invoke-WebRequest "https://github.com/wyalexzz/OBS/releases/download/Complements/ReplayBuffer.bat" -OutFile '%appdata%\Microsoft\Windows\Start Menu\Programs\Startup\ReplayBuffer.bat'
```
