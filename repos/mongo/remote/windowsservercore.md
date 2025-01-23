## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:2b7949ca80bd8e358eba675a27fba18f0584401c3027abea9669c8daf6f72535
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull mongo@sha256:8f7c9735624ddf9d5b67e51ecd831255ba579011c0af552ec96357854016515f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3268989100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956e2b03ce62058872e3e33f18069da7912ae04c1e1f996ab4110bac1bfa455d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 22 Jan 2025 20:35:37 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 22 Jan 2025 20:35:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Wed, 22 Jan 2025 20:35:39 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Wed, 22 Jan 2025 20:37:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 20:37:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 22 Jan 2025 20:37:22 GMT
EXPOSE 27017
# Wed, 22 Jan 2025 20:37:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b56c5fd6794c07fefaf0232dd4a4029649ef5aafad03b3d876da0984dc2df`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8c121d958eda51211881df659ba4a3c567827216e786eee9b1c6ff12a39fd5`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8092e5dd1bb09ad612b643d4055b4bb34fb7d25f6b4150e626569296662e79`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c392de1897e918f2a1056e13fcc94d9c6d1c66195da9e827c80d8589cc437c`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a895b6f681c6b079586ef7c6669574a6195e010cf7d5e63b7b0cc40557b0`  
		Last Modified: Wed, 22 Jan 2025 20:38:35 GMT  
		Size: 768.7 MB (768702153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d76470dc3e7660d9fa033ce776b68d4c7f3dd2170283cfba127e9d932f4a23`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3ff8753e952f28001ff9b3f6e88cd03cbac0e32a9832b2e9b41e15f4f12a7e`  
		Last Modified: Wed, 22 Jan 2025 20:37:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d3ab988655e45e1a4a8df1efc3d73ad38cf43c5899e5a4e00cbf8a78b856cd`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.3091; amd64

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
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b811b13196895d434b0021eac3ba0848581d05f40c892fae55fdef4a4205c3c1`  
		Last Modified: Tue, 14 Jan 2025 23:39:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f85529403c6487aa9c74e4ef02f980f9a8eb37cd257494efa02d632c84f54971`  
		Last Modified: Tue, 14 Jan 2025 23:39:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c2eeca3efb141bbc2d9ffe4d02cd0b4eb7911ab279afa79b49b3838adbd3a9`  
		Last Modified: Tue, 14 Jan 2025 23:39:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad06acdbb486d7e02eb1abdc69669a488115500efba00bfd12a7ea6a575660b`  
		Last Modified: Tue, 14 Jan 2025 23:39:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5f965c3427dbd1d13070b96cbc84a026e00ebefcf8712e2639aef97c43cf71`  
		Last Modified: Tue, 14 Jan 2025 23:40:04 GMT  
		Size: 768.7 MB (768696298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a38b2349764b80f4f39943572b155986b3a4d8ea9049716ffdb7edca1b8f0b`  
		Last Modified: Tue, 14 Jan 2025 23:39:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e780e3b7105b4c152e1ac90995d018f5da3007df496f5932c58122f32c247bb`  
		Last Modified: Tue, 14 Jan 2025 23:39:01 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec01b056d2b6806f2f99976f721f99789145bbf8db6a70fddd4556a8f04b6ae`  
		Last Modified: Tue, 14 Jan 2025 23:39:01 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:74c46acdca761fade0e50d579e02be91a2653630f7ebea0d4c9ad8351757ac2e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2890887956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee98e6e73a988c6dd5da283e18840436d10bab3f018090c4333518f5cdadb35e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:33:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Jan 2025 23:33:59 GMT
ENV MONGO_VERSION=8.0.4
# Tue, 14 Jan 2025 23:34:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Tue, 14 Jan 2025 23:34:01 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Tue, 14 Jan 2025 23:35:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:35:57 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Jan 2025 23:35:58 GMT
EXPOSE 27017
# Tue, 14 Jan 2025 23:35:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559f682ac88e7261e2c860568a87fa5edd34db7757830e17069d9360be0955f2`  
		Last Modified: Tue, 14 Jan 2025 23:36:05 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf2962007eb9f3bbebbff9d52ecf11d891bc77f7afe2ad4ae433a9798c6e1ee`  
		Last Modified: Tue, 14 Jan 2025 23:36:04 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd30abb6305eb0460bbf5d90ca19798627902014627360bd1439c2726aacc70`  
		Last Modified: Tue, 14 Jan 2025 23:36:04 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee558d7a7b106bac2574c25cfd29cc5d250767a8bc1ee53aaccf4b3a300bd0a0`  
		Last Modified: Tue, 14 Jan 2025 23:36:03 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c84f5da37343e439eec09c49f19177d4e8c288328cfe729f54434ca6de32774`  
		Last Modified: Tue, 14 Jan 2025 23:37:05 GMT  
		Size: 768.7 MB (768666284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc1f873685532035c7dc95f45dcaa8bd6a859fe02f681c8c11205c8baf821adf`  
		Last Modified: Tue, 14 Jan 2025 23:36:03 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a48412a76fae9d61663a45b8ae42551f61c8a38c20e2da79850d6c90033796d`  
		Last Modified: Tue, 14 Jan 2025 23:36:03 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d551c93e1df2b9dfe05c1ae87a6b233387dd65c569ddb375276a53dce7c187c0`  
		Last Modified: Tue, 14 Jan 2025 23:36:03 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
