## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:3de3690b9e4abc3ac386c4cf8231f1dc3ec97f684b29a0477a55b2e83134401b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull mongo@sha256:5d7921c7a8df385add3bbae49de746d010c797719b8e8258290337c977a74ca0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3271274287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47dc70993579a2bb5272675ac5e0340defd9d489aefdd8ec669be468a3f729d3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Mon, 24 Feb 2025 21:31:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Feb 2025 21:31:48 GMT
ENV MONGO_VERSION=8.0.5
# Mon, 24 Feb 2025 21:31:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Mon, 24 Feb 2025 21:31:49 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Mon, 24 Feb 2025 21:33:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Feb 2025 21:33:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Feb 2025 21:33:23 GMT
EXPOSE 27017
# Mon, 24 Feb 2025 21:33:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5c6f86bc5b91f6ce3021beaed74ff0007edd67d426d7f8efca89424459181b`  
		Last Modified: Mon, 24 Feb 2025 21:33:30 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e1fdaf741b797803ef5291e504bd0ea2881db1fdae54cf0a87ca311c3d5d1d`  
		Last Modified: Mon, 24 Feb 2025 21:33:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53545ccba179ca5c05bd36ff6d66620de259a4d3e53a4402938aab06f9e26a5`  
		Last Modified: Mon, 24 Feb 2025 21:33:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee20ec398a053ccc3f71067da1b6ec1e14cffcc2102de6a98e2917c3745da198`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1801578596dd19be7f0a964f602ad91877864f8dcbcceefdf6c72c441e7633f7`  
		Last Modified: Mon, 24 Feb 2025 21:34:40 GMT  
		Size: 771.0 MB (770987566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9f1a7b48a714ff4466630e3054babe8260ae748a2fb9b0874d99174efe85ee`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4001265539cbc3afcdd7d95e57ed51826f3607d2da9b71a06731f19f26f587be`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10bdba0f6991d8ced8e4505ab318ef9da3bc33eff424dd06c4da5884e0aebebe`  
		Last Modified: Mon, 24 Feb 2025 21:33:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
