## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:035d1e7c40e9d977df865073efcfdb98d78d27e4b62c05d7f5fe32886f1cd37c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull mongo@sha256:a2aba6cdaf6f88889ffc2401cbbb9ecc93b01f3d074b7c054986856114c5903b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2950137122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a009c8862931a2607536940d46a59fe97f49693f6d5b12b0211c85b05a852f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 12 Jun 2026 19:14:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 12 Jun 2026 19:14:59 GMT
ENV MONGO_VERSION=8.2.11
# Fri, 12 Jun 2026 19:15:00 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.11-signed.msi
# Fri, 12 Jun 2026 19:15:01 GMT
ENV MONGO_DOWNLOAD_SHA256=564477a3abee2720e78714dd6d2d9757a2d8e5cf24ecd6665cb788be95626c36
# Fri, 12 Jun 2026 19:17:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 12 Jun 2026 19:17:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 12 Jun 2026 19:17:56 GMT
EXPOSE 27017
# Fri, 12 Jun 2026 19:17:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52fec8226f0d1c7493bba44ba0fee194ad800249d4d4f21d0e26ac06fef2fcc7`  
		Last Modified: Fri, 12 Jun 2026 19:18:03 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44343a0283267e872253da58810b724a8458284c7901b76ed0665788f392e49a`  
		Last Modified: Fri, 12 Jun 2026 19:18:03 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd066a69638c5e1eaf5c252c6334bca6ce42e1d94fd09307482a89f232e36cf`  
		Last Modified: Fri, 12 Jun 2026 19:18:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738dfc2bc709d2346a04baf7da918ab82135f14c926d69deb76b472692fd4e56`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17eb2eb8806f34be1943286035595996748767d2a6892c1e3599505db1f88b7`  
		Last Modified: Fri, 12 Jun 2026 19:19:18 GMT  
		Size: 818.0 MB (818002369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00608cdafe6f4565621dda9f4f4c07aa5243b8ee846d6e20e1976a3348465ea7`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eea30a18b0bf54040ad2da6711acaa2076ad29bf91d4d92d2131d0c6a10fd1c`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cb2e8198a0034686ed25dd2774137e7a6295f2953b475519604d787ff59585`  
		Last Modified: Fri, 12 Jun 2026 19:18:01 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
