## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:efd76c9746d16dd02adb381f42064480ea06a7cf82c427dd9a4bec6d7e4d40ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull mongo@sha256:f2c00a042b03da90d188d425d498fa275b0f42c7941c0d82e57718e0d51977dd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3022547230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcf9d896da524cbde4a784ee41d38957fc583a3bca2093b94454a070513182d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:40:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:40:38 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 11 Dec 2024 20:40:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Wed, 11 Dec 2024 20:40:39 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Wed, 11 Dec 2024 20:42:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:42:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 20:42:20 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 20:42:21 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa1354a20b08321314328a22349be8c6b381ca7937baf1fee79b1e4dab251e9`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb309c146b69684819c4271931261234db47d884246c88648462f191dae7ab95`  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ddbad736a6f9fa78de3a34bd0410c4ee1808fe61c41a3f0373eba56cc60cf8`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41608e47826b91e5bcdcc4519ee9a0e5d3f01da93f01938b889348e17cabb84`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc21af67318cd0131ab8d2f5b3e6fc20345e647c5b90920caed945466a9751a8`  
		Last Modified: Wed, 11 Dec 2024 20:43:24 GMT  
		Size: 768.7 MB (768664577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e745f23685e3696bd553447da4a1ea2199e612ffd6e36ec188e6c03bb05b41b8`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80abb72d1e629e6beeeb25693cbd9a2fbc39eb72d5b1fb7c12d84a630be1e1dd`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0bc5d28e0a074146e5d47640dc0ddf9ad8e3b14e74411e67657bd50f9c7ee2`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull mongo@sha256:d8234cea18f659e07b7dd8a5528d7310afbcc7c53ebf7453bfbd6a3d51347416
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2783019949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d973617d5ef1961d3ba849b8a2cb83f51e93eac1c81baf59449f8da940a75f8b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:39:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:39:04 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 11 Dec 2024 20:39:05 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Wed, 11 Dec 2024 20:39:05 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Wed, 11 Dec 2024 20:41:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 20:41:45 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 20:41:45 GMT
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
	-	`sha256:41aa1f7e3d9d06860b43694e7e6840918a8b4dd9dd21de6f2fe9788fde76d247`  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb20e04fe6af42bfbd173691b8275c929574190857b59b99f9650c4dda51b396`  
		Last Modified: Wed, 11 Dec 2024 20:41:49 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1537ca113fe2b64a2865d7eb2c5089fbf2b586d8b7cbca621c78d084a082aa61`  
		Last Modified: Wed, 11 Dec 2024 20:41:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41777d8071d1494cbaa43873e0a0f5cbabc623aa04b21352676256567429be53`  
		Last Modified: Wed, 11 Dec 2024 20:41:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:772fe9176b91ee6ccf25822870075ad991ed89a0c1ef782725d604c0616c3626`  
		Size: 768.8 MB (768840696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e925aaa653a926aff64fb3bea76ddfa240756026c425e579414fccc52eb195a`  
		Last Modified: Wed, 11 Dec 2024 20:41:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44918adff540595cc9fe357ab12dec4ac1a79761484d9e1d4ace7af5aa7b3e99`  
		Last Modified: Wed, 11 Dec 2024 20:41:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a074703779dda8ccdf2f851d77899e8990c4643b90664d8f32a69ad39183db5f`  
		Last Modified: Wed, 11 Dec 2024 20:41:48 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
