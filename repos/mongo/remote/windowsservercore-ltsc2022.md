## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:2e9ad6d3453f591b691c25f4fbc5de90956816433cf7430b49b6414b1f660737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull mongo@sha256:a3bfe898aab43ea1433e77791baf561d1a2826bf4e0191082895bf9bc97c92b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3031090538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9de2df11b6de4b70ffc3e98b14e1ea1d52a0cd3827c31a1cea9929d09fe7ced5`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:37:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Jan 2025 23:37:18 GMT
ENV MONGO_VERSION=8.0.4
# Tue, 14 Jan 2025 23:37:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Tue, 14 Jan 2025 23:37:20 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Tue, 14 Jan 2025 23:38:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:38:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Jan 2025 23:38:58 GMT
EXPOSE 27017
# Tue, 14 Jan 2025 23:38:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 21:54:27 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b811b13196895d434b0021eac3ba0848581d05f40c892fae55fdef4a4205c3c1`  
		Last Modified: Tue, 04 Feb 2025 17:46:40 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85529403c6487aa9c74e4ef02f980f9a8eb37cd257494efa02d632c84f54971`  
		Last Modified: Wed, 05 Feb 2025 00:46:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c2eeca3efb141bbc2d9ffe4d02cd0b4eb7911ab279afa79b49b3838adbd3a9`  
		Last Modified: Wed, 05 Feb 2025 00:46:18 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad06acdbb486d7e02eb1abdc69669a488115500efba00bfd12a7ea6a575660b`  
		Last Modified: Tue, 04 Feb 2025 06:02:17 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5f965c3427dbd1d13070b96cbc84a026e00ebefcf8712e2639aef97c43cf71`  
		Last Modified: Tue, 04 Feb 2025 03:43:40 GMT  
		Size: 768.7 MB (768696298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a38b2349764b80f4f39943572b155986b3a4d8ea9049716ffdb7edca1b8f0b`  
		Last Modified: Tue, 04 Feb 2025 01:00:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e780e3b7105b4c152e1ac90995d018f5da3007df496f5932c58122f32c247bb`  
		Last Modified: Tue, 04 Feb 2025 08:56:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec01b056d2b6806f2f99976f721f99789145bbf8db6a70fddd4556a8f04b6ae`  
		Last Modified: Mon, 03 Feb 2025 21:30:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
