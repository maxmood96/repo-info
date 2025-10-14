## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:1b3b3d1a48975a04bc7e31c78b12e3a4aa4c80eff2e62db4272a0bec80d15077
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `mongo:6-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull mongo@sha256:97d9baa8df53e1175414a70410ce392cb61c01417b481ade079c183d6ddd9f06
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3747522411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b664dc1e589e44f88b21230c16faa8022674dfbf51f14a328337afd4453dfc56`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:54:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 20:54:10 GMT
ENV MONGO_VERSION=6.0.26
# Tue, 14 Oct 2025 20:54:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.26-signed.msi
# Tue, 14 Oct 2025 20:54:12 GMT
ENV MONGO_DOWNLOAD_SHA256=b32578a8d982810c6a9a0b2f962bd45053701d97415f901030b796ec93dea75a
# Tue, 14 Oct 2025 20:55:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:55:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 20:55:42 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 20:55:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5afc04d28b7740eb9588b786f0016a78adc65119b0032f1e71b34b6bdaecd7f`  
		Last Modified: Tue, 14 Oct 2025 21:08:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:613e27b67744da28731e64dd6546df3be1af6fa6cdc76373045782e410f3e0c2`  
		Last Modified: Tue, 14 Oct 2025 21:08:31 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b27fa46ef0a0ac53db8a1bc550914b4388ca696c03da136364e82fa6559805`  
		Last Modified: Tue, 14 Oct 2025 21:08:33 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed2f055b76ddf2f8f383f0ae25186a9cca520758beae3b20968fc512d87b0ce6`  
		Last Modified: Tue, 14 Oct 2025 21:08:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdeae4119724ab8e8225a0580283c89158f567e62ecdb861e2f303e53dffec6`  
		Last Modified: Tue, 14 Oct 2025 22:07:42 GMT  
		Size: 527.0 MB (527032708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:341544d3b3b8e4fee6ae89185065e97fa17e85de32feea4c0b06d3878498ab39`  
		Last Modified: Tue, 14 Oct 2025 21:08:41 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368d44ec28fb6db230064f06488d35ac59da70428bdfd302a353d92b6d948bea`  
		Last Modified: Tue, 14 Oct 2025 21:08:43 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14b91cf819eeb06068d16adac451a2d74a4394149d9e56536310a21d5ef86be8`  
		Last Modified: Tue, 14 Oct 2025 21:08:47 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull mongo@sha256:b0968ed513d248179b5b6dfc6b9a76d36bf130ebb29a544fa29473d98f027d33
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2016054732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bb14b10d89ba0ae5cb32559414ab7c12797f17e23ea7324789bae7cb2600829`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:48:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 20:50:58 GMT
ENV MONGO_VERSION=6.0.26
# Tue, 14 Oct 2025 20:50:59 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.26-signed.msi
# Tue, 14 Oct 2025 20:51:00 GMT
ENV MONGO_DOWNLOAD_SHA256=b32578a8d982810c6a9a0b2f962bd45053701d97415f901030b796ec93dea75a
# Tue, 14 Oct 2025 20:52:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:52:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 20:52:08 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 20:52:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf36dd4cf94dfcc8e04b005a1770950e32fdd4386f208a4e8f02edd1687aef2`  
		Last Modified: Tue, 14 Oct 2025 20:59:29 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:020882393389d9777683aa0d21a26f698b0c5d25d2b437be748d3134661ad092`  
		Last Modified: Tue, 14 Oct 2025 20:53:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3968cb862076daa8c3eeb5df94ebe8c5a283b36c5d2a906c92505b95f2cf2bcd`  
		Last Modified: Tue, 14 Oct 2025 20:53:11 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2823c662e61ab6161827d514881b95fd0ba5cc236dfd439c0ef5cc69f3ed7`  
		Last Modified: Tue, 14 Oct 2025 20:53:11 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40457a1d30274a2c09eae4a63b1d10b876f71369b46be0261e9ea547ace1dba2`  
		Last Modified: Tue, 14 Oct 2025 22:07:49 GMT  
		Size: 527.0 MB (527026497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0094e477235977a223f412a8d90157d50570719acc5087ba934c81e211244c`  
		Last Modified: Tue, 14 Oct 2025 20:53:11 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517a8abf6e25e64d62c1eb0fc6216e0f89a6375994d079edfccceb9bb7b90513`  
		Last Modified: Tue, 14 Oct 2025 20:53:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd0cba2f635d3da15dac47996e09ea090c48a55031a51d455aa683e093fd4a6`  
		Last Modified: Tue, 14 Oct 2025 20:53:11 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
