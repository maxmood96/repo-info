## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:dfd14327bb14622361b0a1cf0c72e94532c5488792b0b74018bc2ccfaf694690
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

```console
$ docker pull mongo@sha256:40ec032aab327e426ae042325b2bfe924492ff29ea49fe9d912460e2887806eb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2541055430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54c05d1172a810fca723fb20dacd910b3cd6aedb6a2b181fdbcb91e8da4bd55`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:41:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:41:24 GMT
ENV MONGO_VERSION=6.0.19
# Wed, 11 Dec 2024 20:41:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.19-signed.msi
# Wed, 11 Dec 2024 20:41:25 GMT
ENV MONGO_DOWNLOAD_SHA256=2d9f5555d820c1b6a3f3177f0a73a4f9e9b3a7f1275d2aa3122a2ecc3a1b31a2
# Wed, 11 Dec 2024 20:43:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 20:43:04 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 20:43:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cfee8d18c5b0841b7d31875eef5b441d6671b5b7cef8b02ec5c9939d3318e63`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e37729ce720608538fa1c06294e57c332252a17de53153e190e0ee83c5a771b`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4bced74a0d23cb86a944506a2ac122ac1ca8a63ccc5300f1c5176c8653c9f7`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1b6245682d9a541bf398a82438039430609551c5129bea5507c2a6c069baa77`  
		Last Modified: Wed, 11 Dec 2024 20:43:08 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1195fd5036a319f84861eb890616a58303e86038f5d36a6977decc768fe395e7`  
		Last Modified: Wed, 11 Dec 2024 20:43:50 GMT  
		Size: 526.9 MB (526876108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feeac66e9058255dfbaa22bed0b75e687805b3e2b336aae807f19524f2add566`  
		Last Modified: Wed, 11 Dec 2024 20:43:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ed9cbd343345b659a6de64480141826c37ec75a01cb998b72dc9a1e427b24f0`  
		Last Modified: Wed, 11 Dec 2024 20:43:08 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1842d5cb7957633046c2fcf96400c856b2fa00bf05622b32ed710035cc905020`  
		Last Modified: Wed, 11 Dec 2024 20:43:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
