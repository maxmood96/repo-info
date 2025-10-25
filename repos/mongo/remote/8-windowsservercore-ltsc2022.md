## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:e9a808e204334ec1ae5a651e39d96bd9aa51c667dd9ac24cf911bb9039b9b0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4297; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.4297; amd64

```console
$ docker pull mongo@sha256:5f2800a523b826f9e100d11ea8b2f25267305c9f455ca201ce15510481b5df84
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2361589408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31893be0efec4ec926e00a77888520f6d1a9a719f51e4de7491199169fa1c10a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 22 Oct 2025 21:59:56 GMT
RUN Install update 10.0.20348.4297
# Fri, 24 Oct 2025 18:23:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 24 Oct 2025 18:23:55 GMT
ENV MONGO_VERSION=8.0.15
# Fri, 24 Oct 2025 18:23:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.15-signed.msi
# Fri, 24 Oct 2025 18:23:56 GMT
ENV MONGO_DOWNLOAD_SHA256=212be476297cf2b93e0d1279506780aaf5e67865e0ba342e740d1bc9ff772557
# Fri, 24 Oct 2025 18:28:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 24 Oct 2025 18:28:24 GMT
EXPOSE 27017
# Fri, 24 Oct 2025 18:28:25 GMT
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
	-	`sha256:7e21ff80f28d50c3e720440b5a498a812ecac750fe4e9f4150ec9ada7057bf75`  
		Last Modified: Fri, 24 Oct 2025 18:29:59 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:085ed518b5bc17f5d9342c659a0e0b546a6414dcf5c55943dc74adc95f27ac04`  
		Last Modified: Fri, 24 Oct 2025 18:29:59 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ece15bf05041946fe5fb5053526c3ddf3b8eabe18bea16ea44e67eaf1d368f`  
		Last Modified: Fri, 24 Oct 2025 18:29:59 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d83a4bf6da56541e966d08e9d99a962c14d70ee8731022c11186378ef10ae6`  
		Last Modified: Fri, 24 Oct 2025 18:29:59 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde2d32061383e449e414b1a94e8289b9ac6af5b7868e68bd142dc628d12ec60`  
		Last Modified: Fri, 24 Oct 2025 19:24:40 GMT  
		Size: 784.4 MB (784387278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6352d78754f662f6d6c3d88dbf2853b68452856000cd51846155f00a313789`  
		Last Modified: Fri, 24 Oct 2025 18:29:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34e2eeae54c6c0753738b597d7ee5904d97ebc24f61324f764ad481b21f544b`  
		Last Modified: Fri, 24 Oct 2025 18:29:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c58f35a7454925ffed37889b212d78a33fade229f9d95394139bcd3c86c4873`  
		Last Modified: Fri, 24 Oct 2025 18:29:59 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
