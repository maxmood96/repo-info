## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:4332861fd68163acd42b8703f386e1410c2e4e61b4cdcd4518c0fbdae783372d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:aad03ce3afae32b36f9300c32f7980f8dcf8ed1ab64a6ad1e498edf13bd8fcd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269817081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df26cecf559493ab129a38c1f6ab0f4e44161eda41ce58add3dfad646220c7c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 27 Mar 2024 21:49:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 27 Mar 2024 21:49:47 GMT
ENV MONGO_VERSION=5.0.26
# Wed, 27 Mar 2024 21:49:48 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.26-signed.msi
# Wed, 27 Mar 2024 21:49:49 GMT
ENV MONGO_DOWNLOAD_SHA256=dbe45ab5b3b04170fab6861629932354408d4033f773c54248dcd0680ea39ef8
# Wed, 27 Mar 2024 21:52:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 27 Mar 2024 21:52:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 27 Mar 2024 21:52:51 GMT
EXPOSE 27017
# Wed, 27 Mar 2024 21:52:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a84712dc641b332e435d9cb5a06eb587539720d23b53deb155aa21d8ce8aceb`  
		Last Modified: Wed, 27 Mar 2024 21:52:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc9430f82d81d9ce38293c6357228497f5e8cf8f694913846cb4415bdb47c31`  
		Last Modified: Wed, 27 Mar 2024 21:52:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8b055ae5cccb7943bd0836d1c8e83a371687c393424154f1be974c6bf00bfbe`  
		Last Modified: Wed, 27 Mar 2024 21:52:56 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f036e0bba3718ab601edc25596df4bf10b3bed5cfc8b0d147142393587d5e63`  
		Last Modified: Wed, 27 Mar 2024 21:52:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96a34aa73b5aad5b5bebf9e6c6e8f1518f41498ba5f8ab28634c6025ed08fa4`  
		Last Modified: Wed, 27 Mar 2024 21:53:26 GMT  
		Size: 312.3 MB (312349060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59a2d641164cc59b14159ad8e5025454cff42acc0b6c2d043ac7921f9d8d64a1`  
		Last Modified: Wed, 27 Mar 2024 21:52:55 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1602ac0de63fdb695064b0f84fa04c2555199d3f9e1460b99d13969c4263d15`  
		Last Modified: Wed, 27 Mar 2024 21:52:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582691a65868425ab22c2db3d9192c9307a8a2d5e5b0ae052b5d27a2ae232528`  
		Last Modified: Wed, 27 Mar 2024 21:52:55 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull mongo@sha256:35e2ba975901a8d0714cfa6eff427cf4d87e6c666824ed3d80a1ac5fd3866fd9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2437478051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6f3a04b8d6e929cb1ceb2cb12749960a6e036991fd9bf46d9c363c340dea92`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 27 Mar 2024 21:49:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 27 Mar 2024 21:49:39 GMT
ENV MONGO_VERSION=5.0.26
# Wed, 27 Mar 2024 21:49:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.26-signed.msi
# Wed, 27 Mar 2024 21:49:40 GMT
ENV MONGO_DOWNLOAD_SHA256=dbe45ab5b3b04170fab6861629932354408d4033f773c54248dcd0680ea39ef8
# Wed, 27 Mar 2024 21:52:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 27 Mar 2024 21:52:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 27 Mar 2024 21:52:32 GMT
EXPOSE 27017
# Wed, 27 Mar 2024 21:52:32 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e99ac86f3b3859009e8e6414255bde6260bf8fa3a4ebc5a4208ab9e68404fc`  
		Last Modified: Wed, 27 Mar 2024 21:52:38 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a74cab96d8b68f07fa23169b9d16330f574253aeb70f586ae365f81a500fa216`  
		Last Modified: Wed, 27 Mar 2024 21:52:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a57caa4d83c9c5fe860b287e5f1f9e3e2e96b0c50a5e97232a3f42a9c9bc74`  
		Last Modified: Wed, 27 Mar 2024 21:52:38 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:948869264f8ed407172c8a16543a4fc0cbc968024bfeca069ab8cdbff62fc5fb`  
		Last Modified: Wed, 27 Mar 2024 21:52:36 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2f0ac562906f15d53df03663fa69cdee4f1caa76ffdd5655db8c3ed38c0ef7`  
		Last Modified: Wed, 27 Mar 2024 21:53:05 GMT  
		Size: 312.4 MB (312368955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d29061783d742f53e9bad05b1e5a09b8762f0c1aad595db2b3e95b69ddafdc`  
		Last Modified: Wed, 27 Mar 2024 21:52:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac8d95b3d2fd2a3a0aeb40a1b78ab02c9633024f62f96487bdae48ac9fb0a344`  
		Last Modified: Wed, 27 Mar 2024 21:52:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:976ca4369184cdbebff03866ee6f157a8bc9997a1b293dbbff7069edc5f84734`  
		Last Modified: Wed, 27 Mar 2024 21:52:36 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
