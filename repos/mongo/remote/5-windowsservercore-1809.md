## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:6540acbfdb487de4ec06f0025053dd53afb20a8d50f273d17ad6609751863d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

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
