## `mongo:windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:df3aa63efcc91193d21b8689e096359d7a50debf7487a138f49cfb7ac01e4794
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `mongo:windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull mongo@sha256:34f827f6569f777f45ea1421a2403b97a3a182e3a0c9082928b2bc397d032dc0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4206089059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68f16b49888c93d8df9fac4464288e1e93ecd61bf14b1accdbe613906a6bb391`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Tue, 03 Jun 2025 22:54:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Jun 2025 22:54:47 GMT
ENV MONGO_VERSION=8.0.10
# Tue, 03 Jun 2025 22:54:50 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.10-signed.msi
# Tue, 03 Jun 2025 22:54:53 GMT
ENV MONGO_DOWNLOAD_SHA256=ae5f02f81ba456ee9fcf819c362255ccae9a961f039435a09b6887f46732c940
# Tue, 03 Jun 2025 22:56:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 03 Jun 2025 22:56:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Jun 2025 22:56:43 GMT
EXPOSE 27017
# Tue, 03 Jun 2025 22:56:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f57447c3a3d36049626c72bf20681d3171df27313fb06fdb353e7b17fb6aa2d`  
		Last Modified: Tue, 03 Jun 2025 23:12:30 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677bbff2b6789d45185f0da489b1ce22123a018bc16f076837d877ab1c156cfc`  
		Last Modified: Tue, 03 Jun 2025 23:12:33 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf5e64ca84c6d8f242a01ffb418ca5f70fc2414e9dce0ca553180cba456978`  
		Last Modified: Tue, 03 Jun 2025 23:12:36 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4249714be2b28c923f77db3deb60885c2aae6b28f4bb849fde20c81a84e6e8d9`  
		Last Modified: Tue, 03 Jun 2025 23:12:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3962da23c1605dd72dd32db0d075cd0cc4b83c3cffd00262f077ed05e942035f`  
		Last Modified: Wed, 04 Jun 2025 01:10:20 GMT  
		Size: 775.3 MB (775314108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0bab1474e2298043b082d67527dfa8671930e84ac214b660d0eedc91fc3235d`  
		Last Modified: Tue, 03 Jun 2025 23:12:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:067eca58cc97060938c6a13f1392d388b11dbe22b36590e0b4db566959f9e3fc`  
		Last Modified: Tue, 03 Jun 2025 23:12:48 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1880229d65fe5315a36f1077f482b46d877efbf0ff40d7c3d493ce23440eef2`  
		Last Modified: Tue, 03 Jun 2025 23:12:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
