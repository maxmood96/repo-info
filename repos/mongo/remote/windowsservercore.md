## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:657448d818c85d99c44dc665bdfc5796ed1434a226e437dac7f46e74abf4318c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull mongo@sha256:7fa429881eb8d35500efb41ccfbf6f3b7fea6440755288db76b3e5d815e5f8c7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227212387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55f1fb75e7c0e04bb4f779d5c953cedc0171dd18435913e6ae1f6cb2fb077293`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 19 Sep 2024 18:57:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Sep 2024 18:57:30 GMT
ENV MONGO_VERSION=8.0.0
# Thu, 19 Sep 2024 18:57:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.0-signed.msi
# Thu, 19 Sep 2024 18:57:32 GMT
ENV MONGO_DOWNLOAD_SHA256=778f03552b6638822c18a9a2e8996d31cf12e4c9b87ffc73be8ce71e0a8465e9
# Thu, 19 Sep 2024 19:00:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 19:00:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Sep 2024 19:00:17 GMT
EXPOSE 27017
# Thu, 19 Sep 2024 19:00:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbc256b237a6e28c22f04564693f63cfa0f2060260ab54382bb4b656c8e49368`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449d832e3eee20ab426b6c85c9704bd7e621dc6b27bc41040328761d69517a70`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5a1fc04a3d3809ee94bb395eec8d781067b83ae5b7d956dd486cbecf5a0910f`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1171bb8ab5212218b0ac3be3e5d4fa8e98f0d1a2fa4b16917aa0c7e7014ef0b`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6408a9294c2da888498c3e5c90c2951be1c9c6c7fb15de86379d95c0478bb696`  
		Last Modified: Thu, 19 Sep 2024 19:01:17 GMT  
		Size: 765.0 MB (765010998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af615893a2fe9ef06c601cc1bc06e47c0c27822d1c122fd780f20f9ca89e539c`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aefb28914c3e0c610f914be046997b5918a67cf2295acc2facb714cb0b88fb9`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cae5ac6efc4f7187bc4eb8ffefcc218153c2956f4087f3231642be7967128d2`  
		Last Modified: Thu, 19 Sep 2024 19:00:20 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull mongo@sha256:9e43383e6ca1d3be2c128d5670b51977100e8c1ccd84a438fda2b0c603148012
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485285280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c36268ecd0496d2b6679c40c246a11137301cc7d674be17d4b1c3f709729fb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 18:57:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Sep 2024 18:57:22 GMT
ENV MONGO_VERSION=8.0.0
# Thu, 19 Sep 2024 18:57:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.0-signed.msi
# Thu, 19 Sep 2024 18:57:23 GMT
ENV MONGO_DOWNLOAD_SHA256=778f03552b6638822c18a9a2e8996d31cf12e4c9b87ffc73be8ce71e0a8465e9
# Thu, 19 Sep 2024 18:59:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 18:59:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Sep 2024 18:59:18 GMT
EXPOSE 27017
# Thu, 19 Sep 2024 18:59:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdd9502c4b68024084c88d0782929ee759f273a442011b2bcf833b576b6fa4e`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e243d7a17956bf9424e764cc4d3ab4f359cfd3c8643dfa3ac7ce8a0dd76485`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c28e73026a011b1c1e665a2e2f6f4ede28c39beaee51aea83a19cac01bb063`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caddb3e1dbaea7dbd32889ca53f8123d94ce1d02b49d569f5ce0211530f8685`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53023350b6c4c96532a470d5cbe3468d5127c46484dca0358ff81360ee552448`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 765.0 MB (765007868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f2ec306c60dc1b0e9d515dc0e6cfb63a3b0658ddd93e856d8c8325d2ec1563`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d3324a0b94a41ea65e391cbfb1fa48f604f3baa86f3c0b08175d1b097c8dd5`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1344664231c31c2007cc360a73163229ce210ef226379e6fda9fd10c56b0d2`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
