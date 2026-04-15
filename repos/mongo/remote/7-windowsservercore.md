## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:d599068512815d63b0ee77b15418b965e6247dd2c2677afe79f537cbfeaefcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull mongo@sha256:654c448134d453d2a0e2c2c4aa186ef83b2d3aa94d8786e70786e6d752331fbb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2748700107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b654a4278e71003b842eed8a11964841557244de921c6ca1785c2a07cd615fa3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:12:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:14:49 GMT
ENV MONGO_VERSION=7.0.31
# Tue, 14 Apr 2026 21:14:49 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.31-signed.msi
# Tue, 14 Apr 2026 21:14:50 GMT
ENV MONGO_DOWNLOAD_SHA256=8ac657caf629b67feb0bb338dac2dfdec0590901fe3b9bc2390cf94b1423abf1
# Tue, 14 Apr 2026 21:16:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:16:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Apr 2026 21:16:23 GMT
EXPOSE 27017
# Tue, 14 Apr 2026 21:16:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a845a3a06f2b91ca97dde894de6f2c997eeb111d04c2e9d013a1009397c2f9`  
		Last Modified: Tue, 14 Apr 2026 21:14:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b594b5293c012df7c1506ca5a44a629c3f310397b373d7470bfb629ae785cf9`  
		Last Modified: Tue, 14 Apr 2026 21:16:39 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ecbf1e45156a77eb794581251450e8ee69c778397383cdd32fadf53fc18618c`  
		Last Modified: Tue, 14 Apr 2026 21:16:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3343c4c7622e345a049b7af0e20f1783c84660daf2ca2e0eb440dd19e0e4744`  
		Last Modified: Tue, 14 Apr 2026 21:16:37 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfe717581f49869e741498dc02d015d5dbf87ee17aeaf2ec7e81ef0edc0f9041`  
		Last Modified: Tue, 14 Apr 2026 21:17:34 GMT  
		Size: 618.7 MB (618704992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16e8fc0ab3f2f66728bf6b217349375cbc7f0f769f0c4d1d30bcfcccd0d82f3b`  
		Last Modified: Tue, 14 Apr 2026 21:16:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19088276585e88cf34916b74e74b8bda9d753efe3bf31e959a4214eb377902b8`  
		Last Modified: Tue, 14 Apr 2026 21:16:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abe283f9653f58d6045d762c1cc197f1ef6c51eb3cf304687a36cc82e3a76911`  
		Last Modified: Tue, 14 Apr 2026 21:16:37 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull mongo@sha256:aaf9d4c2b82b72ba963b7c2543b98e9e4c2b8fb96effffadcceca9ad43350f93
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2688886036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0745ad5601116ed31dfa35fd77113f1f0b84da2bc67a872ff2d5f6e44778647`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:27:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:27:56 GMT
ENV MONGO_VERSION=7.0.31
# Tue, 14 Apr 2026 21:27:58 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.31-signed.msi
# Tue, 14 Apr 2026 21:27:59 GMT
ENV MONGO_DOWNLOAD_SHA256=8ac657caf629b67feb0bb338dac2dfdec0590901fe3b9bc2390cf94b1423abf1
# Tue, 14 Apr 2026 21:32:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:32:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Apr 2026 21:32:50 GMT
EXPOSE 27017
# Tue, 14 Apr 2026 21:32:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3a6d75a186be34cb412d57a2f9e07da91d0addd5b726694a18fd92fc1171`  
		Last Modified: Tue, 14 Apr 2026 21:32:57 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b531dc2c00483b159e5db54c69215a341454009c546bcfe4930bf9fa252a2a28`  
		Last Modified: Tue, 14 Apr 2026 21:32:57 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbc921b03bce330ed871f6cdb80886d5683f29b8d3626a5765238aa2c3b3a2d`  
		Last Modified: Tue, 14 Apr 2026 21:32:57 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab59ee1f8ca6ef357deccce956030c2b2931d5f96621d162917f645c46ee816`  
		Last Modified: Tue, 14 Apr 2026 21:32:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4337de8d6a30f4c1cb5587703871419a7ba1052f3ce64eea11a6a825466541`  
		Last Modified: Tue, 14 Apr 2026 21:33:50 GMT  
		Size: 618.7 MB (618665572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f3cef7edfe453994c6f4d20310dd94e1753477d95c1b2d1d1c9b02e441e93`  
		Last Modified: Tue, 14 Apr 2026 21:32:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a862ad98d1688907d37385b1639b73c6505fa41079ae0ef40ad192972777b7`  
		Last Modified: Tue, 14 Apr 2026 21:32:55 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c434cc3c2c438cc0ec3ed1326c87cc2a4d0251877882acf8f170d4fafbf0e9`  
		Last Modified: Tue, 14 Apr 2026 21:32:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
