## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:cfa16950ac35264f5ca92ee267f8f14fa826de34d97ef5eb4e5b84e339aa69f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull mongo@sha256:fec2954b14996f7c052c11036774614ed30338cbad587634f488f6cf95f4c94b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2545148335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:355dd2ee241e1fb58e359c1b5ee3c3c8975ff73683ed6a4a0b4688cbde5ba908`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Wed, 11 May 2022 12:34:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 16:35:07 GMT
ENV MONGO_VERSION=5.0.8
# Wed, 11 May 2022 16:35:08 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.8-signed.msi
# Wed, 11 May 2022 16:35:09 GMT
ENV MONGO_DOWNLOAD_SHA256=bb8d6bf77df675ef3c89eeded536fc9dcc454f462ef728da53efee7a2c9eb80f
# Wed, 11 May 2022 16:36:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 May 2022 16:36:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 May 2022 16:36:33 GMT
EXPOSE 27017
# Wed, 11 May 2022 16:36:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:52d280e9bf32da92b07a144022b757d7e39ac8039e166551ad32f8ee416bb55f`  
		Last Modified: Wed, 11 May 2022 14:06:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d69949bf137a7a40710907aea6ad10bc1cba2318934604a97bf9ec8d5eedfbb`  
		Last Modified: Wed, 11 May 2022 17:13:58 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:975bdc7df87eaaec677c8594bb8b856ebadb43aab582ab1ea92e8c910d9c8550`  
		Last Modified: Wed, 11 May 2022 17:13:58 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:275ab655e61f196bcabcafd8cff3ce0ab2a001fcc3eaa9c8691ab7b52c09c025`  
		Last Modified: Wed, 11 May 2022 17:13:56 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28074096807789e501b06e108667808b02b42b6d9c61cb44636328d2c842d90`  
		Last Modified: Wed, 11 May 2022 17:19:19 GMT  
		Size: 307.6 MB (307603256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa9fade23ac9370e0c4cf1e61341873a7489e07a2d8eb7108e9e189bae94da3`  
		Last Modified: Wed, 11 May 2022 17:13:55 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d2ff547f5ee845f1916b8dc44e287d89cd3e91cbbe124b661c45efa809b029`  
		Last Modified: Wed, 11 May 2022 17:13:55 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35658930a9fccd0fdfd52a73146a98c14e432407a60f8cbf6ef2720477013cd9`  
		Last Modified: Wed, 11 May 2022 17:13:55 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
