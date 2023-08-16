## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:e28b4374a88fcf06fd743944f57ecd01a2d3c52c246f183a05982bf671158a70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:a36fffafc3e58b1d2cb9e8975df88ae0282143ab0233449922f6276759ad7c6d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2514484376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23323fe8f662b3b3cc1b35623b8b6c9354503380b0d176cc058f416862a1bf1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Thu, 10 Aug 2023 01:11:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 15 Aug 2023 23:17:06 GMT
ENV MONGO_VERSION=6.0.9
# Tue, 15 Aug 2023 23:17:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.9-signed.msi
# Tue, 15 Aug 2023 23:17:07 GMT
ENV MONGO_DOWNLOAD_SHA256=9e5d9380f3ccd409b288609ecf96c0a74ca5fde8a2371ff727402812fbb25ebb
# Tue, 15 Aug 2023 23:19:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 15 Aug 2023 23:19:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 15 Aug 2023 23:19:53 GMT
EXPOSE 27017
# Tue, 15 Aug 2023 23:19:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5180b8f5f7c2303ba89717cfa778a2173921ca7efdc058cfd6ed951c6d5ca3`  
		Last Modified: Thu, 10 Aug 2023 01:57:18 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23353c8ae10e39c8ce615dc279a785c7e7417bdef14f13413986a2fef167548d`  
		Last Modified: Tue, 15 Aug 2023 23:31:25 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1aeebaf26df2f13a6b6dba80dd235933515cc016c223247c58498779c366974`  
		Last Modified: Tue, 15 Aug 2023 23:31:25 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8102685b470c1a9b115b3fd3642d7a90adf2bf0431ce5c7ba72cbf47645379c1`  
		Last Modified: Tue, 15 Aug 2023 23:31:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9193c002df4e300cd14699831d4ca33a35f4e569d8ef9d3e6c1c98acf468085b`  
		Last Modified: Tue, 15 Aug 2023 23:32:34 GMT  
		Size: 518.5 MB (518519079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c124b11ad50e8efbd31fb2259af4c2684b6647147291be4fe805111a86bc16bf`  
		Last Modified: Tue, 15 Aug 2023 23:31:23 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e563b59748f4badfec6dbd02b248021190aa98abc33dc173c5d11208dd700303`  
		Last Modified: Tue, 15 Aug 2023 23:31:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ddf6f85c16dcd2901da763e0e7913bf15465f03b1e938a65213ad7fff9bc6e5`  
		Last Modified: Tue, 15 Aug 2023 23:31:23 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
