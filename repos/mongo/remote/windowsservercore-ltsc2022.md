## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:983c15d3f05dcc7ded5059fc9149fbe3e6560184ac684c0d68aebd90d734a891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:93ce3b5baa83a3540431ea264d54fd3a3d0aa239e99337a4ed99402060d3364d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2651085957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93e6ae4bfa0cf66ee4be5875ff9ae90c6343cf8a31aa9e6dc8b6906007e93fb7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 23:01:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Jan 2026 23:08:57 GMT
ENV MONGO_VERSION=8.2.3
# Tue, 13 Jan 2026 23:08:58 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.3-signed.msi
# Tue, 13 Jan 2026 23:08:59 GMT
ENV MONGO_DOWNLOAD_SHA256=dbad91532fd5f5bb5b42818ce7a644dd603a388926303b306e23ef29a640e849
# Tue, 13 Jan 2026 23:10:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 23:10:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Jan 2026 23:10:40 GMT
EXPOSE 27017
# Tue, 13 Jan 2026 23:10:40 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0fce413876f886fb2250022b76f87a9e023cf582c638600a9fba8ca303bfd0`  
		Last Modified: Tue, 13 Jan 2026 23:02:17 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed1abd2a4a299d7ac78676b336899c0d5f82d3d058c2edad872c1eb1ef5d1`  
		Last Modified: Tue, 13 Jan 2026 23:10:51 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:923f341d81286bf509bf5a571863ded6e1f90cb6d4898147afae5059549f5ee6`  
		Last Modified: Tue, 13 Jan 2026 23:10:51 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e21bf43bc0fdc9427abe81ff4f1387f2f043a3d3693215e1285c270af04ae32`  
		Last Modified: Tue, 13 Jan 2026 23:10:50 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438cf0b92e60792107bfcc7cdaa7ec529fe7490ab9eab13dcf423e721ccd85ee`  
		Last Modified: Tue, 13 Jan 2026 23:12:04 GMT  
		Size: 815.4 MB (815417561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14293688d6163c0d8e82c30e9fef412146cdd07daf95c72bd5a54b2f829710dc`  
		Last Modified: Tue, 13 Jan 2026 23:10:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18d32e4c0de7c773be3cc9dc0097c7ee4ed66d7651e7e490e0e4e0aab39dab2`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b67ef6346c36bd59d48ae769839e6ad4d3cdb078d6575a51712246fb545a933c`  
		Last Modified: Tue, 13 Jan 2026 23:12:11 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
