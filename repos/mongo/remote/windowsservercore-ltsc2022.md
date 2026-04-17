## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:ac10f9d09f46ddb8d8f867a27b50da557e067367ce14c2923fad87f7cfb9bfac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull mongo@sha256:9c974c9b094bafe41c798029fcfcd0b08400f1a466a2ca86c2549ad87ac6e892
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2888168162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:996c3e6accb962831cb1cea4f398f9e290f4e15d34d41cc33ccb45d0b27750c3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Thu, 16 Apr 2026 23:54:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Apr 2026 23:54:53 GMT
ENV MONGO_VERSION=8.2.7
# Thu, 16 Apr 2026 23:54:54 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.7-signed.msi
# Thu, 16 Apr 2026 23:54:55 GMT
ENV MONGO_DOWNLOAD_SHA256=6a326fa3ea7f2013ef28247ea4e68faddaeffc5f19cabed1059e23488986379b
# Thu, 16 Apr 2026 23:57:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Apr 2026 23:57:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Apr 2026 23:57:37 GMT
EXPOSE 27017
# Thu, 16 Apr 2026 23:57:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6070c905e4b6c5ce02c9bc84241b83cd29a3592ea2a9100ec4896563c33c00`  
		Last Modified: Thu, 16 Apr 2026 23:57:43 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd764adc6a3040299d3eea2c3c78c5dd992589298b1832e211c07fe672df0f7`  
		Last Modified: Thu, 16 Apr 2026 23:57:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:993a2d59dbdfd17e412c6de53be925d62308a3909762948ec5f45f5c06d9ab48`  
		Last Modified: Thu, 16 Apr 2026 23:57:43 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3768c71acc8ce4a6d389cf2dd0eb3655785f343f48ba8a5b97b16957b035625e`  
		Last Modified: Thu, 16 Apr 2026 23:57:41 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b808dceef12480e14158c5fc98f6713292329d59fdd3fe47b44f1ed711da0a28`  
		Last Modified: Thu, 16 Apr 2026 23:58:51 GMT  
		Size: 817.9 MB (817947749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:396659f03c46beef4b24221116240577b562b8b64ad7bfe79f6725ae3caa739f`  
		Last Modified: Thu, 16 Apr 2026 23:57:41 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b367441aa43113506e0f2f2b5068f9207f30211a7e0a7b762a494ae76241a44`  
		Last Modified: Thu, 16 Apr 2026 23:57:41 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73b7557c203505e9f7507f92d9c0e95ee783e19a8e74010a17e7f4959e4f0a8`  
		Last Modified: Thu, 16 Apr 2026 23:57:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
