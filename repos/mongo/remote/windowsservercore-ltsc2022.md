## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:7f5326d6f4a30ad2c6d471a9ce2b5718f18368727b334524f3529b4bce38c9e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull mongo@sha256:3a8c489ce9cede1e53d9f52adcd67897782d94d230b088c72719d906c2938d9c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2583729097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4bf80390fee34df0118aee06813d6e0c906a2e43128a471e9cdc80974d31866`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:21:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Nov 2025 19:24:43 GMT
ENV MONGO_VERSION=8.2.1
# Tue, 11 Nov 2025 19:24:43 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.1-signed.msi
# Tue, 11 Nov 2025 19:24:44 GMT
ENV MONGO_DOWNLOAD_SHA256=b005cfd5655f0e752d80fa83a6a37be231ab57639dd2f75cf9647ad315701386
# Tue, 11 Nov 2025 19:26:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:26:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 11 Nov 2025 19:26:26 GMT
EXPOSE 27017
# Tue, 11 Nov 2025 19:26:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f291d602329acab85d3ee064a4257428aa4eb5ce7707134d2630f8b68bba8577`  
		Last Modified: Tue, 11 Nov 2025 19:24:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd71f963b3d7dbe6707b772ab6c3dbd748703cced39e151410ae771fc704bd6`  
		Last Modified: Tue, 11 Nov 2025 19:28:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a03c9e0d321eb0422765df04324f9706925fe9b4bb94fbabaafacd2489ada11`  
		Last Modified: Tue, 11 Nov 2025 19:28:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7886d11d782b465faa8aedeeedef6f8352cce7195725ee095073db3f241a810f`  
		Last Modified: Tue, 11 Nov 2025 19:28:00 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5293f75266e37266e19fd7cf389cd4fdd21775657ee32e99c8c8e15d3ed1931b`  
		Last Modified: Tue, 11 Nov 2025 20:13:00 GMT  
		Size: 813.8 MB (813758363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f324600ff7b1f64bf9397c45b70dc45f48bb093b38f633152139bd1cd40fd6b9`  
		Last Modified: Tue, 11 Nov 2025 19:28:00 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6331797b7c20047edda86fc348df34119f7aaf4c3e2400a15840ecefc97e16e6`  
		Last Modified: Tue, 11 Nov 2025 19:28:00 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae668cb0350354a785d6d38ebb9c17c21b334a288fe79c8be1e6157803416e6`  
		Last Modified: Tue, 11 Nov 2025 19:28:00 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
