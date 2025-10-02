## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:05131297115d05c02480ce84212e28a47b0eb3b299a0c28dc55c4214625ac796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull mongo@sha256:b4f2e5e231e957506cf610a5c90c8da8961db6c11ea32ef143db5c1a619a69f9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3066377808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4afc763bd80c23e6fd301a7b3be1873b14b17f72f5db47bfcbd7a0c1758e37ea`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Thu, 02 Oct 2025 18:12:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 02 Oct 2025 18:12:18 GMT
ENV MONGO_VERSION=8.0.15
# Thu, 02 Oct 2025 18:12:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.15-signed.msi
# Thu, 02 Oct 2025 18:12:21 GMT
ENV MONGO_DOWNLOAD_SHA256=212be476297cf2b93e0d1279506780aaf5e67865e0ba342e740d1bc9ff772557
# Thu, 02 Oct 2025 18:15:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 02 Oct 2025 18:15:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 02 Oct 2025 18:15:48 GMT
EXPOSE 27017
# Thu, 02 Oct 2025 18:15:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb64da0a79109191dc4f736743e008fc9f4e6c2f6b3a7678cacf5cb1638e3c05`  
		Last Modified: Thu, 02 Oct 2025 18:27:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc95eb9c355c082d895168316a7ef0743d81f53a765e2fd273c757f13896aba0`  
		Last Modified: Thu, 02 Oct 2025 18:27:11 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0ef2145368a591a3dad89fda3b6f7cada62314099e51291b40998710c4b09`  
		Last Modified: Thu, 02 Oct 2025 18:27:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7297bc15972d7654b9e3f3e160f7d53ab28c721ef5d2d2fdb9844664b175859d`  
		Last Modified: Thu, 02 Oct 2025 18:27:11 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cca5d1de5a5b519d8cd874599a6ed2c57212f66e36f09f131d9b78b5c964d26`  
		Last Modified: Thu, 02 Oct 2025 19:09:32 GMT  
		Size: 784.2 MB (784223623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3104ad25a3794e901cbc948b3b656c0e51a855594cb1aeb4ded131448ea6cb2`  
		Last Modified: Thu, 02 Oct 2025 18:27:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1267647be14b45e41a649369e7df118ff5aa5af7f6a113a7a71213fc759fb0a`  
		Last Modified: Thu, 02 Oct 2025 18:27:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345fdcddf18568ad688bb003360d9d8b1b2836a648123e49517c1c8d2636c1e7`  
		Last Modified: Thu, 02 Oct 2025 18:27:11 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
