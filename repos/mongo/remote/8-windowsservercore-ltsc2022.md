## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:ac81c3c2dc35490e4d28036742b442a44ad3012c810035cc952694c27b5afe2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

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
