## `mongo:7-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:4f32ad25278fd232f9b501108308b85b6ee3ba9eb74c9251038e9a1fb13fa0f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `mongo:7-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull mongo@sha256:0e1e4c9afff4f906bd7ae470f04ac0e12b4784d0a5456867c5187d6513448fa4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (4046708304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34293d281221888b2d190fd49f1cf2482a287133e3233e2eb8f44406a026f944`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:01:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 May 2025 21:01:14 GMT
ENV MONGO_VERSION=7.0.20
# Wed, 14 May 2025 21:01:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.20-signed.msi
# Wed, 14 May 2025 21:01:16 GMT
ENV MONGO_DOWNLOAD_SHA256=960b961edb4b01a65d209a36cefe715c0cf14aea6a886853f2a31fb143790f55
# Wed, 14 May 2025 21:02:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:02:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 May 2025 21:02:34 GMT
EXPOSE 27017
# Wed, 14 May 2025 21:02:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab92c5eb1943b12ca707a29d479ba07117a09af929c4ed3663d9e84108e25571`  
		Last Modified: Wed, 14 May 2025 21:02:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc75dc23fd65d0d8770353580d71c5770835cc10140dcb962a1d95f579f52b85`  
		Last Modified: Wed, 14 May 2025 21:02:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b78ea95e31c01a21aa26557cf613cbed286790bf3bc9a7c209e59db643c09f8`  
		Last Modified: Wed, 14 May 2025 21:02:38 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a781548c1e860888de26f31bc00d5f007a825830b0c8f99c4542e290a22fe886`  
		Last Modified: Wed, 14 May 2025 21:02:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72aba9935c84390256923338dd2d136b7e3bebc473826dcaecbec9d98c19607f`  
		Last Modified: Wed, 14 May 2025 21:03:38 GMT  
		Size: 615.9 MB (615933438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243c76ee5866d7bb9678521a5747939e162e6b36ff531af03cdfecfc1c3f04ad`  
		Last Modified: Wed, 14 May 2025 21:02:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba21027b164642ae8486e8649c901cd60627291c60e172e36832b6f5e6a7d047`  
		Last Modified: Wed, 14 May 2025 21:02:38 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde9223d42495ccd8b6de2defd8ad92d7ac823850c2e5c56ad0252e926788669`  
		Last Modified: Wed, 14 May 2025 21:02:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
