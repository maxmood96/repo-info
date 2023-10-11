## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:c243e98e27f9a6ffae2f557877f618c1cf764dfe609964bf9ab220d91ae53d8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:9f87d7f32a5b4619b7afa67fdccaa9943301d7a5fc821b969b5c5575f1cd2d15
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2471118006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37cfebe2a02c7d2e06af5ad47be960160685527e50bbcfdb9fe5b88e8f220c43`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 02:54:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 02:54:36 GMT
ENV MONGO_VERSION=7.0.2
# Wed, 11 Oct 2023 02:54:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.2-signed.msi
# Wed, 11 Oct 2023 02:54:38 GMT
ENV MONGO_DOWNLOAD_SHA256=0bcdc885a437a7fd23f780a7c53a2a43aa99a3bc8bc93db5d1f0d8425066004c
# Wed, 11 Oct 2023 02:57:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 02:57:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2023 02:57:49 GMT
EXPOSE 27017
# Wed, 11 Oct 2023 02:57:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c131d94d08cb023367d3fd8434c336e9d07495660367cc521ddff869fb44dc7d`  
		Last Modified: Wed, 11 Oct 2023 05:52:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175ba892e50025592126ee51edb4f9dd31ffa7e760458eda16d5dcbd1c9aacec`  
		Last Modified: Wed, 11 Oct 2023 07:38:04 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0de44f158a1253e5ee43bd39a33dd237f83a1b267e1612d8a0727a99613a7db`  
		Last Modified: Wed, 11 Oct 2023 07:38:04 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2319d97ae390737faefc4ea4081f249c6267a66e8615668b8d8a25f88b4a1f70`  
		Last Modified: Wed, 11 Oct 2023 07:38:02 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a774b7db3262709d5571bf7f2defd4a4462a3ba99e3cd3be89002c72b4feccd`  
		Last Modified: Wed, 11 Oct 2023 07:39:29 GMT  
		Size: 611.3 MB (611264913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:607399825d143f51505e3bacb057ea077d576ca5bcb1e12f7f747926105dc133`  
		Last Modified: Wed, 11 Oct 2023 07:38:02 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c08f6f39cd2e3a118539189b818cc5fbf5af5d6f131f38ec07b82fdce43175d`  
		Last Modified: Wed, 11 Oct 2023 07:38:02 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bac9d87d6601e034aa1ed2624c08f1b35f37305ade335f2b80cc9edc4a9e53f5`  
		Last Modified: Wed, 11 Oct 2023 07:38:02 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
