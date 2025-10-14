## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:cb34b7112c1498870a3d2cb554c0d167b6b6fdc1b702596be1c946420241e112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull mongo@sha256:854fc84d25f11df294382ff468b5013893b833b7296d7e7de60189a3f6a43cb2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3838690535 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d51e48938bbc1ba0de6f5eb1bb150b77cec9743536c5bbc8096393a1a16952ba`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:53:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 20:53:05 GMT
ENV MONGO_VERSION=7.0.25
# Tue, 14 Oct 2025 20:53:05 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.25-signed.msi
# Tue, 14 Oct 2025 20:53:06 GMT
ENV MONGO_DOWNLOAD_SHA256=a6e4b64f4130bd82642eafc83a3644ebb7425c0c26ce7d445ed95da4a9767613
# Tue, 14 Oct 2025 20:54:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:54:39 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 20:54:39 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 20:54:39 GMT
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
	-	`sha256:eb189b6d2ad81070cdb79408b8c35e4ead93ad5579e738dd73cc4a4e7a8570dc`  
		Last Modified: Tue, 14 Oct 2025 21:39:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95b30ce991e009b1e4f3e7b5a2896d75bb96f2b66264964d79118c7ffbb073ce`  
		Last Modified: Tue, 14 Oct 2025 21:39:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c30c18033aeda3f1cd53c5abdd28e999babe0bf4281930eda17f99628ebc2d2`  
		Last Modified: Tue, 14 Oct 2025 21:39:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fbec231050608e9d1c356589e238254c92b5a7c475c50e7d2d7f59bcbb7cc99`  
		Last Modified: Tue, 14 Oct 2025 21:39:15 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f8a951d027ae8dcf53b352ff6a2433829543cc312b3ed66206ff4195be5b6ce`  
		Last Modified: Tue, 14 Oct 2025 22:08:19 GMT  
		Size: 618.2 MB (618200927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6db88ab80065b2ae64e87469475279da27633fa641e3725da7063d1b5f56fde`  
		Last Modified: Tue, 14 Oct 2025 21:39:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03dcd8758fbb7d493280a98b6b37464941ceb955ce7739b34e863819d736324`  
		Last Modified: Tue, 14 Oct 2025 21:39:15 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499215cd10f610f5f5e8bf3f28a489e6e2f0cbb1c23f62dc139be4803eb80e47`  
		Last Modified: Tue, 14 Oct 2025 21:39:15 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull mongo@sha256:3f716ca1ecc1b83a4ed7b266ccd02c5b87fa7bbe3c7460e2e29b3b89a9f47cb6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2107259506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad5d0aa55214cdde92217bb787fe973419b667b480f1fcde6ef43cd03b67986f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:45:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 20:50:19 GMT
ENV MONGO_VERSION=7.0.25
# Tue, 14 Oct 2025 20:50:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.25-signed.msi
# Tue, 14 Oct 2025 20:50:20 GMT
ENV MONGO_DOWNLOAD_SHA256=a6e4b64f4130bd82642eafc83a3644ebb7425c0c26ce7d445ed95da4a9767613
# Tue, 14 Oct 2025 20:51:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:51:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 20:51:33 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 20:51:36 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e7f80425e30f99b2a225ab9723761e1b0b6be510a713f91396d9c65e2837c0`  
		Last Modified: Tue, 14 Oct 2025 20:46:12 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d6ea3851880938a4a95dc71ca42f93d10de38c0f763ce0e8e4a79680664c32`  
		Last Modified: Tue, 14 Oct 2025 21:36:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1780fa1690a3511e771decec637f3b971ee0c47dd27938ac0dcbc446559e17`  
		Last Modified: Tue, 14 Oct 2025 21:36:04 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce6ca5c92f6d72849565d74bd6c62a45ea78473754024cffb3f4617730de27f6`  
		Last Modified: Tue, 14 Oct 2025 21:36:05 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b14e98e1f09010c7f2030a7f63f557b571935ff24dfadf9aace4428ab90dd1a`  
		Last Modified: Tue, 14 Oct 2025 22:08:23 GMT  
		Size: 618.2 MB (618231249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a064942b648836d5093e1d47fee2a414be541729fdc8b4413a9c410ef2a474`  
		Last Modified: Tue, 14 Oct 2025 21:36:03 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bebc90efc21f8cb9cd0b90b5b702ecaa36490b061e89417cccf2b5e5220db2e`  
		Last Modified: Tue, 14 Oct 2025 21:36:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff5a492e3972fc6d650a9fa471a21849e1026e52f300954eddd6a20a69e43bc`  
		Last Modified: Tue, 14 Oct 2025 21:36:04 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
