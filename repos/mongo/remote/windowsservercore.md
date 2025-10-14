## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:12b26557b6930008131186b0ae836a54e633c8531b2b6f061884e01d6acea4fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull mongo@sha256:3b2e385a31e0e5a41f196d1077cef2d4a5da3641becf0a8fd98cabd70ac76329
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (4004692449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a0118e7af0c38d7a4a40314d82620b731c6c42a4f1c4acbeea2fe84ed0b7a9d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:53:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 20:53:03 GMT
ENV MONGO_VERSION=8.0.15
# Tue, 14 Oct 2025 20:53:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.15-signed.msi
# Tue, 14 Oct 2025 20:53:04 GMT
ENV MONGO_DOWNLOAD_SHA256=212be476297cf2b93e0d1279506780aaf5e67865e0ba342e740d1bc9ff772557
# Tue, 14 Oct 2025 20:55:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:55:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 20:55:18 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 20:55:19 GMT
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
	-	`sha256:aa9faf4534df046ccefbb9725a8c7ac6c8ea486c0ec50a565d907aa29ab27f44`  
		Last Modified: Tue, 14 Oct 2025 21:26:21 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a39f0d51c4f1949aa604c107fc8c16d3add49280ed9fa92ef0089c2ea30eb1d`  
		Last Modified: Tue, 14 Oct 2025 21:26:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71fd6e7da8927bdde9feec2279f7aec73f947dff5e45d58c625706578425ba9b`  
		Last Modified: Tue, 14 Oct 2025 21:26:29 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0a888970f51130404989b93cc6c292ddb23f53397122a68dbb1a263f188ff6`  
		Last Modified: Tue, 14 Oct 2025 21:26:32 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f1affc5bcca083e018fac583b1bd8d5fdb38dfbcb96a56804bb2c31c7b81e4`  
		Last Modified: Tue, 14 Oct 2025 22:09:08 GMT  
		Size: 784.2 MB (784202859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9bd26589d48366571f4b0787099df26601a6509e50a0ebf536b5dd18f4fd6a`  
		Last Modified: Tue, 14 Oct 2025 21:26:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453b2d6147d0cfe669f84985f8b2f988db25fb4aa558839b7b27389cbff96b79`  
		Last Modified: Tue, 14 Oct 2025 21:26:38 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e87dee4da1325b30829f88af4a86a34be1ad54502a559ed6e229591ef7c51e7e`  
		Last Modified: Tue, 14 Oct 2025 21:26:42 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull mongo@sha256:3ef00afef0cff9311e4fc7bff7a4386603f77888eb4d8f45fb47b6ea769c2087
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2273279497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97edbe2d8869ee7daa546bb2fb29a93996dae465b8ee737025ce17ebc5d3ae3b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:48:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Oct 2025 20:48:53 GMT
ENV MONGO_VERSION=8.0.15
# Tue, 14 Oct 2025 20:48:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.15-signed.msi
# Tue, 14 Oct 2025 20:48:54 GMT
ENV MONGO_DOWNLOAD_SHA256=212be476297cf2b93e0d1279506780aaf5e67865e0ba342e740d1bc9ff772557
# Tue, 14 Oct 2025 20:50:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:50:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Oct 2025 20:50:49 GMT
EXPOSE 27017
# Tue, 14 Oct 2025 20:50:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9fe01b4a1ab9c875e396b09f24ef78a7c8d92db798ec3be2513d1640f18db`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5f0df60f9ecd9295fe2bf6e3ba479ed0458e91fda192c739dd7985c0ee9abd7`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389c1d69cca695f630ed6c311465a24ca9281059ceb47641a1e8660b85b6c654`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:673bec9c2579e7eab29f09762c5f0a7f1696e95c20867bd25ae6a6f3c5bfe36d`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdeaab470ac97e50c4e03f9e2dd1523b5326e3d795aad83cd456fa6aec537cff`  
		Last Modified: Tue, 14 Oct 2025 22:09:59 GMT  
		Size: 784.3 MB (784251196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b803e5e49f9b4a2802649ee9109072b86f19ac55c99b452288f2b3342891ad0`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092ecd2a1a9248ff336e7005c553677392a0b8b4d0b1d8d95c0a92ec4ce0af08`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9790161778ab7574dcde28564c2de96cbc68489861c30393f636c872ca5ca7ce`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
