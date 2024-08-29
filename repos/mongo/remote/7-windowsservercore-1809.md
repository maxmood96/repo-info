## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:0932b122ac488f472064c34c834c13e6457081a00e9ebe0733f9b7529bbf8f56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:c6584152762d360ab13b913b295ad693edff979e34bf5456936b565c7c085aa5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2854895051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f8d806866164616a985372d65369ffa9a1a2a7554b80c5fe641428ff537ece`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Thu, 29 Aug 2024 20:59:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 29 Aug 2024 20:59:23 GMT
ENV MONGO_VERSION=7.0.14
# Thu, 29 Aug 2024 20:59:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.14-signed.msi
# Thu, 29 Aug 2024 20:59:24 GMT
ENV MONGO_DOWNLOAD_SHA256=2471a7919223aee2f14443a31c7a1cbfb14c5149b8ecaea05710286731908499
# Thu, 29 Aug 2024 21:02:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 29 Aug 2024 21:02:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 29 Aug 2024 21:02:48 GMT
EXPOSE 27017
# Thu, 29 Aug 2024 21:02:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60ef69cdea022197c499f325f737f0ca1ad8dad985f0b700b6a6a78241feee5`  
		Last Modified: Thu, 29 Aug 2024 21:02:52 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28fe047a32a2283ce7bb778357dc69f4d9e7275fe34d9ccbceee59941f1382d5`  
		Last Modified: Thu, 29 Aug 2024 21:02:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8035b114b1bda622939878ca065c0de73d720f129ce5065839ffdd20bc6b6f1c`  
		Last Modified: Thu, 29 Aug 2024 21:02:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5a2a4b35378bce53959ae1ec03761087d4157fd5aa64a70abb7c6bad9aad17`  
		Last Modified: Thu, 29 Aug 2024 21:02:51 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a66b4ed9b84662868c926c5ff3d3ceb81516d512ba728bb6e6107ba580c1c81f`  
		Last Modified: Thu, 29 Aug 2024 21:03:38 GMT  
		Size: 609.7 MB (609682773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a89552ab93ec6de58fc5f9c53d0d175a55971a8161f56f51ad6b64ae36ccc46`  
		Last Modified: Thu, 29 Aug 2024 21:02:51 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a1f492bfd17c37654a2d9e8972c142a51223d8d53f0f8f05d954aa431ae40`  
		Last Modified: Thu, 29 Aug 2024 21:02:51 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82891bf779b3f15a00b10f0e56aeb46285dbc8aeb079e9a05a645db5fd1dace5`  
		Last Modified: Thu, 29 Aug 2024 21:02:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
