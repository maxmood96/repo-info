## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:0ccddb754b1797eda99c71a6bb0722d9adf5e750f0e205887a57d2fef451cef9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull mongo@sha256:b04a31ee394275c9f2e3f1518353262f1a44d94e3ae91a6a1706a10219b7dc8b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2947256507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0fba07e02e8b0b97cf6a2cbf788c70aa200704cf84868410ba4d1eb45935f6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:12:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Apr 2026 21:12:36 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 14 Apr 2026 21:12:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.6-signed.msi
# Tue, 14 Apr 2026 21:12:37 GMT
ENV MONGO_DOWNLOAD_SHA256=a6672561354b1bd37c5ba8d7dd76b66bfdbd28baec6fd8eb2b7eb2b32eaf344f
# Tue, 14 Apr 2026 21:14:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Apr 2026 21:14:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Apr 2026 21:14:32 GMT
EXPOSE 27017
# Tue, 14 Apr 2026 21:14:33 GMT
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
	-	`sha256:c93dfb163be42a2c9d7f691b0d7d60196bb56525fae130c10464d1aded18eff1`  
		Last Modified: Tue, 14 Apr 2026 21:14:45 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d691c6ce6102c38d975341234ae6cce051b08aee0c7e50e3d5e4304c17433d`  
		Last Modified: Tue, 14 Apr 2026 21:14:45 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f8948060fd5bbbaaa4091db122a4eed10081b8ffa59d0692071360897eeb9`  
		Last Modified: Tue, 14 Apr 2026 21:14:45 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44075d631fbf717ac1f0023d83380b72f98e0e34963c1361497a5bbe4af63db3`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cb2d05daec8d7a4de15f5cc9083fe1bc10cacf395d30188ab506710fc1e6f8`  
		Last Modified: Tue, 14 Apr 2026 21:16:03 GMT  
		Size: 817.3 MB (817261289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a79e9aac3ae30da683c9b33ffb23c467909251c098570e0873cc998d29797e`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6e28d8d2b34bf3f77d9475a73e83e675de2994ef9120ae0baaaad9e45a63d7`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef20b7fbd97b9fdd9d51ccd1c8758618fae8e8f08312a28faa7a8d7a03996625`  
		Last Modified: Tue, 14 Apr 2026 21:14:43 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
