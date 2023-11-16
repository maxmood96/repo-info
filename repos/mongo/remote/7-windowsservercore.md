## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:c211f16417c6de07ad7269921d29e2a70e4a4f753126a8a1bef278959423699a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2113; amd64
	-	windows version 10.0.17763.5122; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:8c7ba564396711cc66b78e7c88cb758b874c039f40bac59a64177b04b7d92116
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2499127236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684d8b8ee2ca70a5aa054c7e48a5e05ef6a2c93910699520cf71866d700bd379`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 03:18:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 03:28:06 GMT
ENV MONGO_VERSION=7.0.3
# Thu, 16 Nov 2023 03:28:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.3-signed.msi
# Thu, 16 Nov 2023 03:28:08 GMT
ENV MONGO_DOWNLOAD_SHA256=7ec97aa108c6af587e77a49479b4e7239da6ccac2903e163ae984797b3afea14
# Thu, 16 Nov 2023 03:30:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 03:30:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 03:30:28 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 03:30:29 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73dc3dec59ae25ff1232f5fdf2ab39df387f3bf86ba48717ff271d76c2feb`  
		Last Modified: Thu, 16 Nov 2023 04:19:26 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c78e661210df7e9eb5ab41db3aca66d8800d6617c3cf4178125ed3a99b433f`  
		Last Modified: Thu, 16 Nov 2023 04:26:20 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f641ede520e750d1c494a6c9b7222fae54bec5b73cc6c8c5b0bc1a38a911d3db`  
		Last Modified: Thu, 16 Nov 2023 04:26:20 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bee5e2ad383fb7ca0e114ad9dbfec41c4d37be5d9dd7e9081347d24581bc89f`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c54538a1ac7e0062cb8e2c9ddb6d5ab5accdc3b72a93c74f403ba007b60b200b`  
		Last Modified: Thu, 16 Nov 2023 04:27:51 GMT  
		Size: 612.3 MB (612336247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5052447881a901f21960dfe425b55725b550263b1d3c23864b551154ae4d987c`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f073aae9d8bdfa66feadd8697a216b14877c0b9ff347217f211a85746da0d5a`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e68026f2e761421e59e2cfb6162ffcce6a54d03ea9a269ea4fad3e26650fe542`  
		Last Modified: Thu, 16 Nov 2023 04:26:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:0b2bb6ec0fa973edecb1b71c63386866cf7e4701db5c2cb74a2309c165837dbd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2669756461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccc8524d7ee97ab4abf89f04d90a9e6d1b26451ee28f956888d6549c474de3d1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 03:30:49 GMT
ENV MONGO_VERSION=7.0.3
# Thu, 16 Nov 2023 03:30:51 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.3-signed.msi
# Thu, 16 Nov 2023 03:30:52 GMT
ENV MONGO_DOWNLOAD_SHA256=7ec97aa108c6af587e77a49479b4e7239da6ccac2903e163ae984797b3afea14
# Thu, 16 Nov 2023 03:33:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 03:33:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 03:33:59 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 03:34:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c273721fe0b05301e704fdd9d1606d47e4fe666ff0f05f71608ecc8401fa5b18`  
		Last Modified: Thu, 16 Nov 2023 04:28:11 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2b910b85a605191d57082623f86494133c0d19fce3d9e3e5aa2c8e39572c59a`  
		Last Modified: Thu, 16 Nov 2023 04:28:11 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f916242dbff0a3d501fe7d80ea2933ecc1c241c99a01a0854783a9d41fb77210`  
		Last Modified: Thu, 16 Nov 2023 04:28:09 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a3f92692d5283f8944ec68df34ed56efb1554e439f38d23ce52aa6953e0b9a`  
		Last Modified: Thu, 16 Nov 2023 04:29:43 GMT  
		Size: 612.3 MB (612315382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc4f24e60fb47b09e794a4b4c78f8a3341cf3d3bfcb22706763ea8dc8ba44ce3`  
		Last Modified: Thu, 16 Nov 2023 04:28:09 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492f36d6dc525bd24c4738240858d97ff4120a20e465482bd6e2536136c37eea`  
		Last Modified: Thu, 16 Nov 2023 04:28:09 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0c3d4605df2d7cbc830fafe2e41124be682729e179db533449642c01cc68765`  
		Last Modified: Thu, 16 Nov 2023 04:28:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
