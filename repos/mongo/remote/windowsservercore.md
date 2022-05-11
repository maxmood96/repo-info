## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:7a2599ea9aca837022ba1c0744cd57ef58af22bd5b87b30b61f4c5c1aa3991d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.707; amd64
	-	windows version 10.0.17763.2928; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.707; amd64

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

### `mongo:windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull mongo@sha256:a46c02c60c13897af54df2251ebb149d50177d3fe8edac788ce68b0b8a79c05d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2811584652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75b1d8faf352efb8e8bcf3a0493f97b4cd9ed81b3f8d4b9ff0872f22102c48db`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 16:36:49 GMT
ENV MONGO_VERSION=5.0.8
# Wed, 11 May 2022 16:36:50 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.8-signed.msi
# Wed, 11 May 2022 16:36:51 GMT
ENV MONGO_DOWNLOAD_SHA256=bb8d6bf77df675ef3c89eeded536fc9dcc454f462ef728da53efee7a2c9eb80f
# Wed, 11 May 2022 16:38:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 May 2022 16:38:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 May 2022 16:38:55 GMT
EXPOSE 27017
# Wed, 11 May 2022 16:38:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed648abdccc0008be86dd7acc4b29fcb2b559a0ac7f5bcfd4d0a46765c4c0fad`  
		Last Modified: Wed, 11 May 2022 17:19:39 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94a5e34d591af17c80fc4a8993148ccf4407c5fd443eeef95e164c95b0e95ac`  
		Last Modified: Wed, 11 May 2022 17:19:39 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8009fd656396aa220eb4ee615063e5f79d1ec0cf60d0f7a03febfc578e8d4b75`  
		Last Modified: Wed, 11 May 2022 17:19:37 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf7a299045301e3ddf47b94cca39cc333c685463e4b39123a442cbd6c34351c`  
		Last Modified: Wed, 11 May 2022 17:20:35 GMT  
		Size: 307.5 MB (307519055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99cf82bce6dd3c1656182ac51e1ce713d935a5ef065f9b59b114d509fb1417a`  
		Last Modified: Wed, 11 May 2022 17:19:37 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4329af9f844d211897916dad41bfe7753864b40e210260ad4287339cb82b1352`  
		Last Modified: Wed, 11 May 2022 17:19:37 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c89bb3ca933a58854002c046d399fb735c26449a2471def1f9c080cc6f0fac65`  
		Last Modified: Wed, 11 May 2022 17:19:37 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
