## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:006128297b84629f7d90a83f7ed2fd6884e93ab7109daabfce7f647b03c15abe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `mongo:7-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:a358fd691e57df7260907099dafca9a6f48c9d19c2cfe38fe168e9b760cc29d9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2731943587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3db7b1bdc913d96c7f5b7cddeab3ffdfb2f669fe65252ba054972f1de1173cdd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 29 May 2024 22:01:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 May 2024 22:01:09 GMT
ENV MONGO_VERSION=7.0.11
# Wed, 29 May 2024 22:01:10 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.11-signed.msi
# Wed, 29 May 2024 22:01:11 GMT
ENV MONGO_DOWNLOAD_SHA256=80e1e9806e02a95c0365509ec3a4e83b8771da09a1c4df9f7d1dfbe4516a07f5
# Wed, 29 May 2024 22:03:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 May 2024 22:03:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 May 2024 22:03:38 GMT
EXPOSE 27017
# Wed, 29 May 2024 22:03:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f2481bb8ef9089c8b84b8b20a23559787e02b6b44604a18cdf96732962ab00f`  
		Last Modified: Wed, 29 May 2024 22:03:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c3d3ce663ae3a73a7a70fff78f469b7180dcbbd99c9a0908311a15ec8d6013`  
		Last Modified: Wed, 29 May 2024 22:03:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa8416ea2ec6f53b75279714a7372f882867e1c8cb9a10f98cc47848e9b275a8`  
		Last Modified: Wed, 29 May 2024 22:03:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b63ca976d5fd3d9ad53893e649d700658c7ada785502783e354ed9617f2d123`  
		Last Modified: Wed, 29 May 2024 22:03:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:015a8bd651b7754a11ad05ea1c3abf039d280c3fc4c481c8e64d91499b574ab6`  
		Last Modified: Wed, 29 May 2024 22:04:35 GMT  
		Size: 619.3 MB (619263184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c09788e708805686d3c54b5502d737f89fd65b1d084cdcaf1f4984d24902f9a9`  
		Last Modified: Wed, 29 May 2024 22:03:43 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a78cd8807fece9b6e1226a01a332c19e561ac2b0f7e1dde602709b2b20bd16`  
		Last Modified: Wed, 29 May 2024 22:03:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f5f14afca08b032eff4b1aca74f178fddad79f248399a8cd5787e6195e2d77`  
		Last Modified: Wed, 29 May 2024 22:03:43 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull mongo@sha256:d9ed15145a4fcadf4a3c242f9389bb99c9ef048149e633e85d9117e99e24cb89
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2799136110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde5f86049f294580a357f0aac1298658af9c7f2f4d4532f129648862a906de`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 22:01:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 May 2024 22:01:12 GMT
ENV MONGO_VERSION=7.0.11
# Wed, 29 May 2024 22:01:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.11-signed.msi
# Wed, 29 May 2024 22:01:14 GMT
ENV MONGO_DOWNLOAD_SHA256=80e1e9806e02a95c0365509ec3a4e83b8771da09a1c4df9f7d1dfbe4516a07f5
# Wed, 29 May 2024 22:03:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 May 2024 22:03:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 May 2024 22:03:06 GMT
EXPOSE 27017
# Wed, 29 May 2024 22:03:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a780e6c23e6ae92b4fd9214e11ed536aedeecc361e970d5248d09b0860faaee`  
		Last Modified: Wed, 29 May 2024 22:03:14 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1abb0c09f5f56c7878d63838a7140362efbab23209e2f0ac68147c5cd35fe3`  
		Last Modified: Wed, 29 May 2024 22:03:13 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbd5883c82d99b68d5368f0275f13ccce469c40f4b86ba1c39633d5a3df7d5c`  
		Last Modified: Wed, 29 May 2024 22:03:14 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fc0bc24e137bb56efae91c1702b49f19fd5c7e7cb822517e9fc9c1b639755d`  
		Last Modified: Wed, 29 May 2024 22:03:11 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8b42888468bf2a7ae303ea734bc38f1d32299a1458f4612fde76039e2c5a28`  
		Last Modified: Wed, 29 May 2024 22:04:00 GMT  
		Size: 619.4 MB (619415197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03fb17b811306e64e3f43b800cd805af6c4b28facb6a823eeb729121e512018f`  
		Last Modified: Wed, 29 May 2024 22:03:12 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17514f1de68e1d285ad219a1b9962efa7e0a3a397e9e4181e71343c4b5f7d364`  
		Last Modified: Wed, 29 May 2024 22:03:11 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7707c608d433153ba6c521e51d354041651641af34bd9bf002d0d34f43ebfc9b`  
		Last Modified: Wed, 29 May 2024 22:03:11 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
