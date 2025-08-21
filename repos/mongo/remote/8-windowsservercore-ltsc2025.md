## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:d87c612311958bf1b139505c919fdc04b3e279a6d9b7081ef89912cf10fe1efb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull mongo@sha256:ee911d38a94c375bb93bde321949a49ce93914561c6263765ff41059b8897380
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 GB (4280121658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e46750dfff5e141f14f82bad49ade8426bcdc5f3932b00f5232f1f121df97a8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Thu, 21 Aug 2025 19:01:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 21 Aug 2025 19:01:20 GMT
ENV MONGO_VERSION=8.0.13
# Thu, 21 Aug 2025 19:01:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.13-signed.msi
# Thu, 21 Aug 2025 19:01:22 GMT
ENV MONGO_DOWNLOAD_SHA256=f301e2272fb222bf53b76883bbf95d07c54b116ad1e9e694234f002ad9abd0c4
# Thu, 21 Aug 2025 19:02:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 21 Aug 2025 19:02:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 21 Aug 2025 19:02:50 GMT
EXPOSE 27017
# Thu, 21 Aug 2025 19:02:51 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6731ebade47b83d0456704ba060b05ecede0c7a869279fa61d549108479c09`  
		Last Modified: Thu, 21 Aug 2025 19:06:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368aa22bccd0dceda3731de39b933efe36bd67fdd1ef67df9e4f14479648f436`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dcca905f4846901fe5206b8232f494d4e782e58399ff6134a6fa0de09c70821`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e3cc73f048374c0b1393afc12e1a6c3c9f78670b46e74e5116ee215431368a`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8207d831e25b20bf47ada7f98da235ae497d18cc34f99cc2b45051ef206a1839`  
		Last Modified: Thu, 21 Aug 2025 22:08:34 GMT  
		Size: 781.3 MB (781282009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b6c1638c586fe492441f9b61d8b9afa8605500c71de6c683e1ee59b3f6fc423`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a361b2fb064475060eaeb228ad07c22d25a009e38442bec6faa49be0a4033a`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b25f0198fe276e448151796772c8875644dbf8ebd11c001c96ac6bd9ea1c0153`  
		Last Modified: Thu, 21 Aug 2025 19:06:46 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
