## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:16929fa1d88f0b257763de77d519b29d3c13a581073121198bc8bd67b884efb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `mongo:6-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull mongo@sha256:e3afaee86832b55092d42dcbe02635c3f0f883994c028a092c1698976db8a4ea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3922125986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce5798583456c8889414bbabf286bf72d2d7ed6f75457752affba05bbd96a169`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:21:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:21:10 GMT
ENV MONGO_VERSION=6.0.22
# Fri, 18 Apr 2025 03:21:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Fri, 18 Apr 2025 03:21:12 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Fri, 18 Apr 2025 03:22:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:22:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:22:20 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:22:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cd9da083830fb4c18af6d0f3809ad937c994aade29e5637a26b5fad741ed5b7`  
		Last Modified: Fri, 18 Apr 2025 03:22:27 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8bd2d9dd002edec4f1c0bde0704d373a23193bee68b0452deb99ff471bbd73`  
		Last Modified: Fri, 18 Apr 2025 03:22:27 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce2d2f03777c2b2f82ee07a1f6f68ed2d15f449124e573d2def84611121953a3`  
		Last Modified: Fri, 18 Apr 2025 03:22:27 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d215fe909701bacad265acd57f010adf7d45eaceef1e9d0adde47b3e3857fd`  
		Last Modified: Fri, 18 Apr 2025 03:22:26 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ede24185586fd267bf2ecb88b2f55a30613bdfe5a3bd3e889b5698be06f415`  
		Last Modified: Fri, 18 Apr 2025 03:23:18 GMT  
		Size: 527.0 MB (526955319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4d39311e0ebe74594d4c9edaa0aa516b3eec2d132f943b00fae0dece40571f`  
		Last Modified: Fri, 18 Apr 2025 03:22:26 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781bde9ec64115bc665aac255bf8a2dfd9359d625b4141a00e277f9c2911d0b8`  
		Last Modified: Fri, 18 Apr 2025 03:22:26 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa95f888ff4a9f05ea93f52daf3d4c0c810412c19549b1bf9256db11ff97143e`  
		Last Modified: Fri, 18 Apr 2025 03:22:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:eda3dc33f247b349437787359c0cd2044227b7995da21cfae7ff2981466567b6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2800504424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39dc5584ef234f0d5976da38d26be9890e81658859052e12cad21b1e24dd6554`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:29:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:29:53 GMT
ENV MONGO_VERSION=6.0.22
# Fri, 18 Apr 2025 03:29:54 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Fri, 18 Apr 2025 03:29:54 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Fri, 18 Apr 2025 03:30:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:30:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:30:55 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:30:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1336025661523a5b33a97af2ee5c66fa5bb4f5a12af4429b4981781b52a7871`  
		Last Modified: Fri, 18 Apr 2025 03:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:accf50c00327d534abe4a0b8eb30c898744f014ddbfb61bb865193283ffcc26b`  
		Last Modified: Fri, 18 Apr 2025 03:31:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f03fbff43091771a5f56731e19b3390d9fe63a3d4cb56ebc6a65d1d94a32dd6`  
		Last Modified: Fri, 18 Apr 2025 03:31:00 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f26741a0aced520208b506464e8222d35060c267607f07c8c66fc3823ddfea`  
		Last Modified: Fri, 18 Apr 2025 03:30:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1cb54ec349e3d7ef89c34c714d1b914fcaff7ffc1dae3b9a96328db08379cc2`  
		Last Modified: Fri, 18 Apr 2025 03:31:42 GMT  
		Size: 526.9 MB (526912884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:944ce34aec714564eba0676640e5a5fcacb737d08bf6497209050073b2b28426`  
		Last Modified: Fri, 18 Apr 2025 03:30:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93256fb42f6f29936fa8dcfbf30a17afa5e1febf6b73c72e60105158271112e0`  
		Last Modified: Fri, 18 Apr 2025 03:30:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1306c0c4d5c8d084a3ef24fe13cd3e05ec0871a06c7c8cf12e9a656783e046`  
		Last Modified: Fri, 18 Apr 2025 03:30:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:50c4b48b609176b7c7605d7170295a29041bc778f6452ce2796fb680547d5f42
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692505144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50813081dafa45c7acfa47ae018989a875903c102e889b5415d212dbf30fc6f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:27:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:27:46 GMT
ENV MONGO_VERSION=6.0.22
# Fri, 18 Apr 2025 03:27:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Fri, 18 Apr 2025 03:27:48 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Fri, 18 Apr 2025 03:29:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:29:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:29:30 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:29:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0b9f82b798295343b7f973fa953119c7658425bd05e8a59edbfb76ad7a1375`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac89e21e70a997c36bd204cadbb698595a5fd2b699d6736f5c584f90d3270dca`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4ab7c11aa52778ab5cb643a77822c22b2fe095f85c9b7d190bcc238ea16ac7`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9c64b8971dec10ebf4d5de8bf09819554f604405c3970efac75d7011fac2fa`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d316aea26790a987b4b93cbfb7834802d22f48537e98c202917c9b905f5ee1`  
		Last Modified: Fri, 18 Apr 2025 03:30:17 GMT  
		Size: 527.0 MB (526970272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b399594b5463df25bef9837a0c587697f43314a21179182d1b0baf1226b78e4`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48166358ffd0bd636f7ec971d79a276e78714f284a54563a02057bf471419553`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbdc83b6a1da48d21fc098df4f7a6e06ac0f8ef3a70736659fc36e3792556cb`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
