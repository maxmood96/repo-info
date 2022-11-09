## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:2a688be3e08babab09850f11bfe138420f716062b10dc927f4daa7d6e7cfb842
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1249; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.1249; amd64

```console
$ docker pull mongo@sha256:f20d16873d30d388e0f162eaf6ce0f5dd6cebf05e7c209c6b84801a75307c2cd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2793054597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec73691574d2aa48d48c4ece9a538908ce6332b2be03143f37d66db622b76bac`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 05 Nov 2022 07:49:25 GMT
RUN Install update 10.0.20348.1249
# Wed, 09 Nov 2022 14:41:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 18:31:44 GMT
ENV MONGO_VERSION=5.0.13
# Wed, 09 Nov 2022 18:31:45 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.13-signed.msi
# Wed, 09 Nov 2022 18:31:46 GMT
ENV MONGO_DOWNLOAD_SHA256=f9b1e144822887bb361ad218967f4cbfdedb6d59e70b12b564b4b63a4d5cbf6f
# Wed, 09 Nov 2022 18:33:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 18:33:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:33:26 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:33:27 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a4aee932fccc1ec8135f290aca03a7c93dcc2536fc84723813ef9b95f6fd13ea`  
		Last Modified: Wed, 18 May 2022 07:59:24 GMT  
		Size: 1.5 GB (1473997635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e276673195ed11807395b0da51ac20ef31c925ce955c29ad1bab54f14617c25b`  
		Last Modified: Tue, 08 Nov 2022 19:41:53 GMT  
		Size: 1.0 GB (1007770983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edcc0cd10e58716558145d847bcea390e3840d172df19b8d0f08a57dd985262d`  
		Last Modified: Wed, 09 Nov 2022 19:02:46 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f1ed794ca633dd3043489f04b65634163d54fe127015eded0dc6ffe0e1490c`  
		Last Modified: Wed, 09 Nov 2022 19:09:46 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e00d6958353eb71d950d38e1fe80a6a4236ee641e131fb8e615b38d69121cb1`  
		Last Modified: Wed, 09 Nov 2022 19:09:46 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c28910c0531e0c624b16943a64f431680c4fb384fcb7325851d7a5782988d937`  
		Last Modified: Wed, 09 Nov 2022 19:09:44 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc349fd8a2b21ee0480cf833a93236890c8ef8387b5bd9756f33c98014a6dae7`  
		Last Modified: Wed, 09 Nov 2022 19:10:44 GMT  
		Size: 311.3 MB (311276435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2206b677867745ce6697867b5d067a6ad96d22879e1b778f08e451d0b4917dd2`  
		Last Modified: Wed, 09 Nov 2022 19:09:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e150b31fe9fe1abe3df85f31a3cd7d4952911ef00e207273c0a423d4c8f171`  
		Last Modified: Wed, 09 Nov 2022 19:09:44 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39425af5df292019f9e337102c5867b179751d20e4d60b30b861f6bbf5125b62`  
		Last Modified: Wed, 09 Nov 2022 19:09:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
