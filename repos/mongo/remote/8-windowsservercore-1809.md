## `mongo:8-windowsservercore-1809`

```console
$ docker pull mongo@sha256:8197792affc3e6bb4e6501cd62e6999d9a5576345042cfce84c4f8c86cd97b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `mongo:8-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull mongo@sha256:9e43383e6ca1d3be2c128d5670b51977100e8c1ccd84a438fda2b0c603148012
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2485285280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c36268ecd0496d2b6679c40c246a11137301cc7d674be17d4b1c3f709729fb`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 19 Sep 2024 18:57:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 19 Sep 2024 18:57:22 GMT
ENV MONGO_VERSION=8.0.0
# Thu, 19 Sep 2024 18:57:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.0-signed.msi
# Thu, 19 Sep 2024 18:57:23 GMT
ENV MONGO_DOWNLOAD_SHA256=778f03552b6638822c18a9a2e8996d31cf12e4c9b87ffc73be8ce71e0a8465e9
# Thu, 19 Sep 2024 18:59:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 19 Sep 2024 18:59:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 19 Sep 2024 18:59:18 GMT
EXPOSE 27017
# Thu, 19 Sep 2024 18:59:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fdd9502c4b68024084c88d0782929ee759f273a442011b2bcf833b576b6fa4e`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82e243d7a17956bf9424e764cc4d3ab4f359cfd3c8643dfa3ac7ce8a0dd76485`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c28e73026a011b1c1e665a2e2f6f4ede28c39beaee51aea83a19cac01bb063`  
		Last Modified: Thu, 19 Sep 2024 18:59:25 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3caddb3e1dbaea7dbd32889ca53f8123d94ce1d02b49d569f5ce0211530f8685`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53023350b6c4c96532a470d5cbe3468d5127c46484dca0358ff81360ee552448`  
		Last Modified: Thu, 19 Sep 2024 19:00:21 GMT  
		Size: 765.0 MB (765007868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f2ec306c60dc1b0e9d515dc0e6cfb63a3b0658ddd93e856d8c8325d2ec1563`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d3324a0b94a41ea65e391cbfb1fa48f604f3baa86f3c0b08175d1b097c8dd5`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af1344664231c31c2007cc360a73163229ce210ef226379e6fda9fd10c56b0d2`  
		Last Modified: Thu, 19 Sep 2024 18:59:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
