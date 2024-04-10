## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:3bee21079627db6ae9afcb738dfa4294dbd027371370bab18afefa1dd46a4282
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:a3d79ba4b4825667aebf0b0c74e4110bc9bab570ef88f6c7c4be7098e2f77ac9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2617168959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e910b6bfda70ce14648f95e0e47c243c6515ba001aafb665bf2c28ec10a2a33`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:58:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Apr 2024 23:58:22 GMT
ENV MONGO_VERSION=7.0.8
# Tue, 09 Apr 2024 23:58:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.8-signed.msi
# Tue, 09 Apr 2024 23:58:23 GMT
ENV MONGO_DOWNLOAD_SHA256=30b8b6a96c5887a49e671ba72a7995279be7f232a666acd6717a59f7c68295f3
# Tue, 09 Apr 2024 23:59:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Apr 2024 23:59:44 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Apr 2024 23:59:44 GMT
EXPOSE 27017
# Tue, 09 Apr 2024 23:59:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e363ba6a755e9556d5e94cb373716cfe3ff7e1e07682d041f68bcc52676647de`  
		Last Modified: Tue, 09 Apr 2024 23:59:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b654ab8132f5c57c09fe8e6342c7fa1076d173ebb5648b2767d049d7ae4f909a`  
		Last Modified: Tue, 09 Apr 2024 23:59:51 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a2d8aa5ac3b2ab91e5cdb477de0efff42e2306000f84aa44ad7f81a4b68aaec`  
		Last Modified: Tue, 09 Apr 2024 23:59:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aee2025185e5515300e0232b5fa627f90957ae9cfaf3956ac13d1a45aa7f747e`  
		Last Modified: Tue, 09 Apr 2024 23:59:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ff93885c0ab6bcbd76f3a52d62d2ee013ebadcf8846aaf1c587666689a937f`  
		Last Modified: Wed, 10 Apr 2024 00:00:44 GMT  
		Size: 617.8 MB (617786289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:263d20d5e2d5560401ea3c7317cff3b9a5f95feee3a3844025b9660488e8c2ea`  
		Last Modified: Tue, 09 Apr 2024 23:59:49 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c1de625cc31c7dcd5a7eff11b2cffc138889bae52c02ca49f7c59166869877`  
		Last Modified: Tue, 09 Apr 2024 23:59:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4893d12a47e448c9a58f8fb5e8744336d8e975ac0e05b5bfc60e5d88939a2f45`  
		Last Modified: Tue, 09 Apr 2024 23:59:49 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:c5c7810551db18d9139a18217bf9686ef24fb9aa4ea94c67494eb6b8ef828a01
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2782242027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82d10663513160181e3e33ab6aad166870460628358f2db8bd59ec23a77c9e9d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:55:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 09 Apr 2024 23:55:35 GMT
ENV MONGO_VERSION=7.0.8
# Tue, 09 Apr 2024 23:55:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.8-signed.msi
# Tue, 09 Apr 2024 23:55:36 GMT
ENV MONGO_DOWNLOAD_SHA256=30b8b6a96c5887a49e671ba72a7995279be7f232a666acd6717a59f7c68295f3
# Tue, 09 Apr 2024 23:57:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 09 Apr 2024 23:57:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 09 Apr 2024 23:57:46 GMT
EXPOSE 27017
# Tue, 09 Apr 2024 23:57:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb03856aa02b25ea345552422faf6679ec617be786f320ea02bb6db9aebdad1c`  
		Last Modified: Tue, 09 Apr 2024 23:57:53 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6fb1ebb7faf84bf58c74310b5b6af8643a5d110a081d3760c03d2a59cd012a`  
		Last Modified: Tue, 09 Apr 2024 23:57:53 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5f4d141e21ea4a0736f360a604a9c496e67d54ad743f874368c3eb68c0334e`  
		Last Modified: Tue, 09 Apr 2024 23:57:53 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddeec4f18bc6c6f54193d31873a7abeb49523e4babcbfeb664d9ff821ee6535c`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea22064598a4516497927f12aec6e374bde3737213865e5171c73c1ed7b6bb82`  
		Last Modified: Tue, 09 Apr 2024 23:58:44 GMT  
		Size: 617.8 MB (617804988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b84ab6bd22a2f053b7d48f8872ce9d761e436c8aa6a0ec6ce60e64de4da1072`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c089f9af27e5f3273765ddbbe23f79d6a783a83a5b59e09fc8202118a33933b`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5659c97dfcab63f6bde47f8cbdbc929c4c66d6a1fb89bebaeb879b78a753a92a`  
		Last Modified: Tue, 09 Apr 2024 23:57:51 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
