## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:fa825c50eb0b316f40b6a0928e56b9a62ec13d4475901c3093f78d577a2ad3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:3a0da7660bf54eb615f68c4946d5f7cab6d005cf56ca0358d0354635d58bb08d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2273595031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d0dd023ac52efe6f911c455d8e0a1044e388d7126a15429ea1cdec2382e8a2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:06:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 00:06:33 GMT
ENV MONGO_VERSION=5.0.25
# Wed, 13 Mar 2024 00:06:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.25-signed.msi
# Wed, 13 Mar 2024 00:06:34 GMT
ENV MONGO_DOWNLOAD_SHA256=65f3fde2ddadbf61dc5895d54670bbbd6febf8b4f7c3a081d1012038452011b2
# Wed, 13 Mar 2024 00:07:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:07:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 00:07:32 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 00:07:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e067bd012d81a8b3ca5b457bf5e489340e1933e5dc0b90678db0e849034a81`  
		Last Modified: Wed, 13 Mar 2024 00:07:38 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79e62c7cb840f6acc07d3cec942a95a000a3dbaf812322a7580cd76eae69d2e`  
		Last Modified: Wed, 13 Mar 2024 00:07:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cae990d5e93e58969c84710e1a42ad029d09f623ebfd518ca5d017d1c74e704`  
		Last Modified: Wed, 13 Mar 2024 00:07:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a0beb6ae9b2d2c9fd6d615cabd0810c1472db223c7332dbfcc99691b6c393e`  
		Last Modified: Wed, 13 Mar 2024 00:07:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17f0b60555018db151505eef3bd5f329de8a7773aa8d96f2589bb8112327d40`  
		Last Modified: Wed, 13 Mar 2024 00:08:09 GMT  
		Size: 316.1 MB (316127003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255ed4f8506b36e4cdec89e71532b46429ac1c89273afd687eb20647ab769b2c`  
		Last Modified: Wed, 13 Mar 2024 00:07:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fb9e4e7851c7def5cdd0edde2d7c424a387eb7df08ea11dbd7124cd04e6dd9`  
		Last Modified: Wed, 13 Mar 2024 00:07:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e1ff22a2b683320fb362c320d53bfc2ec4b7df24764382b3804c111a972f0`  
		Last Modified: Wed, 13 Mar 2024 00:07:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:85020a7ecabbf94cea21021add34c8a532d506e8d4118d02fee1fc16edc1d262
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441277045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06c48b84154583c2dd113c26231b9ad241e26e806b6f6d9244f4a59bc1250e4b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:08:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 00:08:37 GMT
ENV MONGO_VERSION=5.0.25
# Wed, 13 Mar 2024 00:08:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.25-signed.msi
# Wed, 13 Mar 2024 00:08:38 GMT
ENV MONGO_DOWNLOAD_SHA256=65f3fde2ddadbf61dc5895d54670bbbd6febf8b4f7c3a081d1012038452011b2
# Wed, 13 Mar 2024 00:10:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:10:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 00:10:12 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 00:10:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6c17ac7461fb70682c6fc55e14e162887948ef82cb0caa0770a4f024431f39`  
		Last Modified: Wed, 13 Mar 2024 00:10:17 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4288ceb7e3fbfc4e861bd0a9f0ae1222776b4f8599db8f9fbbd99801fc5c0bcd`  
		Last Modified: Wed, 13 Mar 2024 00:10:17 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7a2422b308286a056b7378f7b61f37ef3b32547e477b6cd94d6fc68a6f81d01`  
		Last Modified: Wed, 13 Mar 2024 00:10:17 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:086a1cf14deaca8aadde8ac2ecf839b193263ee83c64d631602f3900625eba42`  
		Last Modified: Wed, 13 Mar 2024 00:10:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbcba0b954bcae2adb3574e123d7dff6cbdab5739c3e5ecb7fa3ec5e124d611`  
		Last Modified: Wed, 13 Mar 2024 00:10:48 GMT  
		Size: 316.2 MB (316168044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f645e82ee7dd6002f036794fdd88f68f32b7465289989e8a18310e67e53aeac7`  
		Last Modified: Wed, 13 Mar 2024 00:10:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ecb87817b0d7970650df4f298899cd92b1919d7e3e52fde4dcd5995d00a52b`  
		Last Modified: Wed, 13 Mar 2024 00:10:16 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767b74dbbff9921cae325030cca1d2a110de02d7aeb1793fd282203b6a67ca72`  
		Last Modified: Wed, 13 Mar 2024 00:10:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
