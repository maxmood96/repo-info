## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:5d25c4753163a3d260deb358f5efa7acfd2ca3c0b676ca637d3c23b08d86beb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:83350c6d383bd00af1d7a72545c76906139ef0e4ad59cd4ce9e45444fb3395e7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2513418695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8acb8f848422513ae0cb9ead9ff5fe468ab6b4ea21c5d537c8707f8fd67ead4f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Fri, 25 Oct 2024 23:57:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Oct 2024 23:57:19 GMT
ENV MONGO_VERSION=7.0.15
# Fri, 25 Oct 2024 23:57:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.15-signed.msi
# Fri, 25 Oct 2024 23:57:20 GMT
ENV MONGO_DOWNLOAD_SHA256=db61d1e382ab03ee98dcef1a65c4065efc4eb9eba2733852828670cfce23db3e
# Sat, 26 Oct 2024 00:00:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 26 Oct 2024 00:00:49 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 26 Oct 2024 00:00:49 GMT
EXPOSE 27017
# Sat, 26 Oct 2024 00:00:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5b0ec16b3f1b54bc7aa00454db788c9b86591d6661f576639b13cb7174c6a2`  
		Last Modified: Sat, 26 Oct 2024 00:00:54 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9336b4fb3b5eac48895c8526c6267b84ea241de1bff23a91f66d6a58861806b1`  
		Last Modified: Sat, 26 Oct 2024 00:00:54 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375b24d07b09ac6c082164b7e8aa6da60cf7cf356619c96812bf56b80567eb70`  
		Last Modified: Sat, 26 Oct 2024 00:00:54 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa4f8e9ca02a6319670b10f10a75175507abbd0afb54540b168bc68eb28ad18`  
		Last Modified: Sat, 26 Oct 2024 00:00:53 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6ebf27cdbb69609004e8a3a8ad9524524027bee4e39ad796a51ac415bf0548`  
		Last Modified: Sat, 26 Oct 2024 00:01:39 GMT  
		Size: 611.6 MB (611584342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac300f7ff0ba41f3a5bf32ff0ba2abf3f19c91e076955c9f166d3937a92f7676`  
		Last Modified: Sat, 26 Oct 2024 00:00:53 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc1bf7db78fdea03db2cdce8efac62829b0b36e77094d819f0898ede479b604`  
		Last Modified: Sat, 26 Oct 2024 00:00:53 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd3ddf9dcc1af135be636758b629e2072fc7d9ebfa22cbb285a2891a6f903bc5`  
		Last Modified: Sat, 26 Oct 2024 00:00:53 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
