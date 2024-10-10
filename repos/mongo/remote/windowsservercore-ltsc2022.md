## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:79d693fcde759cb7bfebb79891f276c5efbca068ba25e8c8244e8a160c53b49d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:17f60980165b7c7f7fef30274cb3c730382a72edb7ef075fb353cb3de36d20a7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565291661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24262c62867189489751d5239ff16d3698fb50cfbf335f10eb0afa441c9ceff2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:08:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:08:22 GMT
ENV MONGO_VERSION=8.0.1
# Wed, 09 Oct 2024 23:08:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.1-signed.msi
# Wed, 09 Oct 2024 23:08:23 GMT
ENV MONGO_DOWNLOAD_SHA256=303e766388b9965ce5ee40f01df921275fbd53da7ba3d729c8767c4d0de0ce8b
# Wed, 09 Oct 2024 23:10:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:10:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Oct 2024 23:10:15 GMT
EXPOSE 27017
# Wed, 09 Oct 2024 23:10:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c67852e8cb7bfcd025aabec978e2952a11c46530460b397ca7f0e0efdad8228`  
		Last Modified: Wed, 09 Oct 2024 23:10:19 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dcdf75367cc58581a9f2ff48695d15359604e99f6b65e2893fcdcc67bc4e20e`  
		Last Modified: Wed, 09 Oct 2024 23:10:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf2bbdfaac538e5d96b9ca30cb2962c076b384c474e0b8c61937878b0decb3`  
		Last Modified: Wed, 09 Oct 2024 23:10:19 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e730762337571d5315dc75e16e7b3c78bf3032fac7ac56204e1e00e98685149c`  
		Last Modified: Wed, 09 Oct 2024 23:10:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7e9b32e4d3e56bfa991f9051c636d3a1e2e435f52dbd1200c3fd1fdac777cd`  
		Last Modified: Wed, 09 Oct 2024 23:11:17 GMT  
		Size: 765.9 MB (765941151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7759e7f02dfa4994f17c9fd21a65d986e7be9ad6fb1f407cd56b8c13c20138`  
		Last Modified: Wed, 09 Oct 2024 23:10:18 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a36cd8241fa686b0309fa11e4cebbffe5b9b9a82b29505c9f3ba91f2b61728e`  
		Last Modified: Wed, 09 Oct 2024 23:10:18 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9b93cc89d0e88e4565926462539c41439075bcfa18bd1d59fbbe7d47975b6c`  
		Last Modified: Wed, 09 Oct 2024 23:10:18 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
