## `mongo:windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:d8ffc4254fbc239a334bb00c8f1c1f01fa801173c2bf1fe281c7fc21798d04fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `mongo:windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull mongo@sha256:9383e7996927645a8b611946bd5f7434a34d4a29bdd8a6d2dfd0556480e8bfd6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4165142704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b44b32b3ba361735d1ed6584e3573a337d04a109ef64334781bcb50d2455219d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:45:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Apr 2025 00:45:41 GMT
ENV MONGO_VERSION=8.0.6
# Wed, 09 Apr 2025 00:45:42 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.6-signed.msi
# Wed, 09 Apr 2025 00:45:43 GMT
ENV MONGO_DOWNLOAD_SHA256=c90e72bd480ba96934708a90e456080732b473665abc8bfbe828b33b833f8a70
# Wed, 09 Apr 2025 00:47:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:47:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Apr 2025 00:47:21 GMT
EXPOSE 27017
# Wed, 09 Apr 2025 00:47:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3974fd75c3e06c04069eb1310e884f7e379f52f24ae0dc8c8a3dc5f9e7a931c3`  
		Last Modified: Wed, 09 Apr 2025 00:47:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bf684ac6fdc54c506743d2014c303e18430a2ec2ef5e757a8e78d54d03b32c`  
		Last Modified: Wed, 09 Apr 2025 00:47:37 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aff941b9ee7c227f1fd8fa9d8ae9fa8370cd6311c35e7b9b5fd11c5e86593e4`  
		Last Modified: Wed, 09 Apr 2025 00:47:36 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d32d8dea6f75da520700046292e86fed87823d7f4de818065ad45d5b1fce42`  
		Last Modified: Wed, 09 Apr 2025 00:47:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1c6296abcd9b80f37191b949ad5deb20f16f8d8c65039ceb8d4a436f3105e4d`  
		Last Modified: Wed, 09 Apr 2025 00:48:50 GMT  
		Size: 770.5 MB (770454035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09f7d5062e0135c40de1b76310e561d8861d4dcf317af8a612acec19c7a5a98`  
		Last Modified: Wed, 09 Apr 2025 00:47:34 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc47386558fca2f80f539a9d9103d8606203d7a32e63bad65e1925d04340cbce`  
		Last Modified: Wed, 09 Apr 2025 00:47:34 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d0e3dc6e302133ff23994f39c35ee4ef1f347a9c4cf9c523efd1d3ad8224662`  
		Last Modified: Wed, 09 Apr 2025 00:47:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
