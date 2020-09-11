## `mongo:3-windowsservercore-1809`

```console
$ docker pull mongo@sha256:84c137a7645c132501bf06b26e0f454708ffe88fcfe561edc6afba953a2bdbb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1457; amd64

### `mongo:3-windowsservercore-1809` - windows version 10.0.17763.1457; amd64

```console
$ docker pull mongo@sha256:7b3fdaf9f200e1b4df293ec949e9ca0dc7a435f747825b544265f74732a884b0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2579929419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:506fce9c6a1c10a65dae4ee6d037d28d7bd0205a13a9807c654da14f58880774`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Sep 2020 13:15:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Sep 2020 20:41:34 GMT
ENV MONGO_VERSION=3.6.19
# Wed, 09 Sep 2020 20:41:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Wed, 09 Sep 2020 20:41:35 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Fri, 11 Sep 2020 21:22:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 11 Sep 2020 21:22:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 11 Sep 2020 21:22:58 GMT
EXPOSE 27017
# Fri, 11 Sep 2020 21:22:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1df31adcc7026c3bf0cb32832a3f307dd6e1e54b8b3e050f8a73b5caee674d88`  
		Last Modified: Wed, 09 Sep 2020 16:48:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1aa7beacb3c01eb97a75bcf3fbf2d6b9990a2c4427a2e87f3aa299d7c4f3b3`  
		Last Modified: Wed, 09 Sep 2020 21:05:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c5d71baad1176ea57cd07c3a1393b7237d5e30d51b46a5094c7879a67fadba`  
		Last Modified: Wed, 09 Sep 2020 21:05:43 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9a58cd18c7fc5ef6e7584fa7668c5b030b1fbbbc2e8110267bf54f01c0c040`  
		Last Modified: Wed, 09 Sep 2020 21:05:40 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c307ef330f1c43817b83d7b2d0ddba98809750463c6a7aef122dbb1e85a1bf8`  
		Last Modified: Fri, 11 Sep 2020 22:33:00 GMT  
		Size: 228.6 MB (228649317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc69a974ebe15fcdc6d904efc851eb3032dc8bf40621714acf1bec0dbeb5cd2`  
		Last Modified: Fri, 11 Sep 2020 22:32:15 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc16b7b660b50e38bd7a07c0a927e1e3c489a2dcf6884b109a4813b2fe9daad`  
		Last Modified: Fri, 11 Sep 2020 22:32:15 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ce7edd04e4cab4c85b7c935e647be36b271da16c02f855c15535d72b7c6858`  
		Last Modified: Fri, 11 Sep 2020 22:32:15 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
