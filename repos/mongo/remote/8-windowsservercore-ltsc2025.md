## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:ad147c3e9df6f69a9e5c8b6941e83b5bc056fd6f1c974608638d4c6ee63bc2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull mongo@sha256:3204cc69c577d2baaac34a72f9157c953c0f3868974a192c7a563b1d93184da3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2896855749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e76be2efeea61115d3cc764af6eb2396c570708194572351b6f6cdab185606f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 22:06:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:06:02 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Mar 2026 22:06:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Mar 2026 22:06:04 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Mar 2026 22:08:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:08:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Mar 2026 22:08:06 GMT
EXPOSE 27017
# Tue, 10 Mar 2026 22:08:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0ecf41559df61247aa99121106588c7bd8133fd5ca3eb5f0e11d7e10364714`  
		Last Modified: Tue, 10 Mar 2026 22:08:23 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9699db20dbc71231d41a6fe8de88a9bcc647aeceaae843a5439a9045af49ee47`  
		Last Modified: Tue, 10 Mar 2026 22:08:23 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567a8c0273ee13e49c4dd4f1c65a04d4271f5befa11f150e85b278eea2bc459e`  
		Last Modified: Tue, 10 Mar 2026 22:08:23 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94c00da52a9c16e3a235e7ed24f6ec80170deb3ba8ff8fb38be4766cb133d139`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfa1ceb8f1ba5bdb79de11862752366ff6bcfbef13f98e3707e9e801cd3cc00`  
		Last Modified: Tue, 10 Mar 2026 22:09:39 GMT  
		Size: 815.7 MB (815650484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9001a4eefdfc8174fc09c0caa404a4d80f9eec24bcbc3e2d4f6ed940be24bf4`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bebaea12e708b7610da7975067b5a903426108e9d5973ef0ffdb40b46728d392`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d187e65a211430393432b9e4a7769cc0722abcb2e0b1bffb097ac5fc7f5664e6`  
		Last Modified: Tue, 10 Mar 2026 22:08:22 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
