## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:71b6e26ca1385dc73f916c2c71f6966b614e05f46b11333493d5ef73b50a2632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull julia@sha256:f2e460fe268c466fc4e21fae889fcdb344e346320f87fea61ce9df9c9d3b5395
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2149053289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdf76a844b45471e1d3ded5c52e66f6f2c0d28fd4fce94e383ad39c773df3c8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Wed, 11 Feb 2026 01:10:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Feb 2026 01:10:16 GMT
ENV JULIA_VERSION=1.12.5
# Wed, 11 Feb 2026 01:10:17 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.5-win64.exe
# Wed, 11 Feb 2026 01:10:18 GMT
ENV JULIA_SHA256=97c0cff9770baa823d40eb6f4f47fdfdcc3c48c609882354c01734f8abcd14f8
# Wed, 11 Feb 2026 01:12:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Feb 2026 01:12:46 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71099ac0ee59fcbe5d2e13acf798c85403706838f4e92d96421ae09af5314edb`  
		Last Modified: Wed, 11 Feb 2026 01:13:01 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdb2fc2e8cbf0388dcd0ab151b24f61762379f76dfad3e5d9b7bb41d8eef1339`  
		Last Modified: Wed, 11 Feb 2026 01:13:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f2c57a54db8e955178464d8bc54373a734f9641c2d3040d8767aefa529b9f07`  
		Last Modified: Wed, 11 Feb 2026 01:12:59 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52cc26f587094b6ac3dadd7234041b439a7892962cde9ddae2f9ec92fae838bd`  
		Last Modified: Wed, 11 Feb 2026 01:12:59 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c7c42ef1d5669ff8cf667c14eb8c829b6fe594b544967ca2c6fcc241ca379c`  
		Last Modified: Wed, 11 Feb 2026 01:13:44 GMT  
		Size: 286.4 MB (286389499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b56ebed73d303b518cb2bc53b143feb54fc045bc41950f109ce27f987eae89d`  
		Last Modified: Wed, 11 Feb 2026 01:13:00 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
