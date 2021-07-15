## `mongo:windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:21f134dd0989b1e1b734224b2c210d7573e11176f01b8fa51180b9e34f67a62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4530; amd64

### `mongo:windowsservercore-ltsc2016` - windows version 10.0.14393.4530; amd64

```console
$ docker pull mongo@sha256:6482b51d0de718dc17aa087e321057559eafdcdf986f8d8e41446ec8b41c0fc5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 GB (6564408948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25effbe6d69101bd7f3cb25be8c091f4403364440a2298c8ccb133dd9c410f58`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 09 Jul 2021 05:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Jul 2021 01:14:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 01:14:28 GMT
ENV MONGO_VERSION=5.0.0
# Wed, 14 Jul 2021 01:14:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.0-signed.msi
# Wed, 14 Jul 2021 01:14:35 GMT
ENV MONGO_DOWNLOAD_SHA256=26920cf86cf1eea8acbf395ad12b0b94631ca4175dc47588a5dc4d9221f014cd
# Wed, 14 Jul 2021 01:23:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Jul 2021 01:23:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jul 2021 01:23:20 GMT
EXPOSE 27017
# Wed, 14 Jul 2021 01:23:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a567de41cc349380b25967f180fb1b6b2431bda61ccaaf69d78a33bc9523614a`  
		Size: 2.2 GB (2199646155 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fed351b78c876c55ec9c7e75d3b9d1b146c5c5dfeb4b5480c0a7c384322df98c`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f267a6cc1ee766b749b19baff8f6e0875ea6918b5b0720836082d434a7f42632`  
		Last Modified: Wed, 14 Jul 2021 02:03:37 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c26de76b84a77e2e80235a036fda1baee78da3428eb9d63ef4c14b72feaf7d`  
		Last Modified: Wed, 14 Jul 2021 02:03:36 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7128f1fc594e3a7d5941b91a5f94a305bdefb4b18cd9a5e49dcb131ee57e1c0d`  
		Last Modified: Wed, 14 Jul 2021 02:03:34 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af26b0815d8544dc762b63891d76215bb55b0978c289d568ab58afa1fc5cbd96`  
		Last Modified: Wed, 14 Jul 2021 02:04:37 GMT  
		Size: 294.8 MB (294766930 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766b54dba8ac38cfe817a8bcb2e6a99b8b9fbf512452b5ccb2769e1bfa944be8`  
		Last Modified: Wed, 14 Jul 2021 02:03:34 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278ac62d7576fdc7b729ea001e754038fa36669acff5291a75fd247d5d36337e`  
		Last Modified: Wed, 14 Jul 2021 02:03:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518d2932317a6fce3a384a0a2938c64345cc03b5f0e3b117e27ab20a2d6b9a64`  
		Last Modified: Wed, 14 Jul 2021 02:03:34 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
