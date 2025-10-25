## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:bad433e58d7268ad3c273224c9cc8c13198d165b9d1054f4066b166ece3d7b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6905; amd64
	-	windows version 10.0.20348.4297; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.6905; amd64

```console
$ docker pull mongo@sha256:6d6864c061d53ce74f608fdb8d8eac797af8cda1bfa68aff2346e6ba1c54a0ba
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3838568623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15a0e7e73dfc12d9a60da9219982cb7120afb3101e517c49e7f82ef98501c90`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:24:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 24 Oct 2025 18:24:27 GMT
ENV MONGO_VERSION=7.0.25
# Fri, 24 Oct 2025 18:24:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.25-signed.msi
# Fri, 24 Oct 2025 18:24:28 GMT
ENV MONGO_DOWNLOAD_SHA256=a6e4b64f4130bd82642eafc83a3644ebb7425c0c26ce7d445ed95da4a9767613
# Fri, 24 Oct 2025 18:26:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:26:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 24 Oct 2025 18:26:02 GMT
EXPOSE 27017
# Fri, 24 Oct 2025 18:26:02 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe429043ba679f26f92aba4b7eb4c39f1471696f0f4094d5e3f35d9c2d49e690`  
		Last Modified: Fri, 24 Oct 2025 18:27:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e62bf50b605a6510d4376d46a3595bb97b75dd88c846d9c0bb891b4d69a8784`  
		Last Modified: Fri, 24 Oct 2025 18:27:20 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115ea080c23fca2d5cea35c75022decfa84c7cca43730266d5f989f8f03fd245`  
		Last Modified: Fri, 24 Oct 2025 18:27:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b94a7fec8594b4b8dbb4c6fc302935eabaae42f8a57fdf37e2d2868b643f59d`  
		Last Modified: Fri, 24 Oct 2025 18:27:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71ab8435b1482643fb3feeaeefb7a9e05dfa0c5227287eaf1daadd5d600e33d`  
		Last Modified: Fri, 24 Oct 2025 22:09:32 GMT  
		Size: 618.2 MB (618212538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3e100df46d7fe9803e71c5e5a531d86a1c3b0bac8a9225970692cd3f748fa0`  
		Last Modified: Fri, 24 Oct 2025 18:27:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8ecf3c90be5c6f779987b6221cb9961298a07acf7e7c821363c51368ff436b6`  
		Last Modified: Fri, 24 Oct 2025 18:27:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f6e8a1cfad61a5122062300143229a1f762e7025c04c5e6a5327f018880808`  
		Last Modified: Fri, 24 Oct 2025 18:27:20 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.4297; amd64

```console
$ docker pull mongo@sha256:c7a19e74803b1ffc60343a2b347e18f2a2ce3d1100b9eafce384839374717216
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2195505441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a4f7959ba9083427769b480dcc4ffe3d65e56d85a14ded3498f0485400cb10`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:11:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 24 Oct 2025 18:24:47 GMT
ENV MONGO_VERSION=7.0.25
# Fri, 24 Oct 2025 18:24:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.25-signed.msi
# Fri, 24 Oct 2025 18:24:48 GMT
ENV MONGO_DOWNLOAD_SHA256=a6e4b64f4130bd82642eafc83a3644ebb7425c0c26ce7d445ed95da4a9767613
# Fri, 24 Oct 2025 18:29:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:29:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 24 Oct 2025 18:29:44 GMT
EXPOSE 27017
# Fri, 24 Oct 2025 18:29:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130d5bf0bd040ed2a9354c6bb5dc8ff89b34e452980249bf817f0b7cb33a21ce`  
		Last Modified: Fri, 24 Oct 2025 02:37:38 GMT  
		Size: 88.2 MB (88173861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d7307306bfcd17eaeb00efbf6127b2df301ed63abbd9a720307ba2c78fe3cf`  
		Last Modified: Fri, 24 Oct 2025 18:20:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5475c8cc94b761d3a180071959f6da6b48b8a1d5bca6e6d54c915e16a3aec27`  
		Last Modified: Fri, 24 Oct 2025 18:30:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:169340171e0bb301eed7f1308278f51a2cea053196d1f8e88afed21850f7c86e`  
		Last Modified: Fri, 24 Oct 2025 18:30:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81d655a097b2bf2ceafda7beff923873b75cc22dbd62038f0727ff9f3020ec5`  
		Last Modified: Fri, 24 Oct 2025 18:30:55 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a533390ee0b010e1fc7358e43cf56b7efa2afbe75fb86dbf6662d19184a05e`  
		Last Modified: Fri, 24 Oct 2025 19:24:11 GMT  
		Size: 618.3 MB (618303409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f18e040fdbc9257dd1b1c37a117a95b2aa3a0bee3f72e5dbf0cc2f167533f0`  
		Last Modified: Fri, 24 Oct 2025 18:30:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f3d3f4783bd65df9e6115d6afd55b95034dba79fa929d64f61b8e9d1b40926`  
		Last Modified: Fri, 24 Oct 2025 18:30:55 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e859dea8dc0b12f8c0f1e0bb8915caf11f62f36a870b427ca5d8b9cc6e47903`  
		Last Modified: Fri, 24 Oct 2025 18:30:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
