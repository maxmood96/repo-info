## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:2e5fc0ad8da463b6c583efb536aee7127a86793d3921a7aef7e1ff1120f26c70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:50c4b48b609176b7c7605d7170295a29041bc778f6452ce2796fb680547d5f42
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2692505144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d50813081dafa45c7acfa47ae018989a875903c102e889b5415d212dbf30fc6f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:27:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:27:46 GMT
ENV MONGO_VERSION=6.0.22
# Fri, 18 Apr 2025 03:27:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Fri, 18 Apr 2025 03:27:48 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Fri, 18 Apr 2025 03:29:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:29:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:29:30 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:29:31 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0b9f82b798295343b7f973fa953119c7658425bd05e8a59edbfb76ad7a1375`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac89e21e70a997c36bd204cadbb698595a5fd2b699d6736f5c584f90d3270dca`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4ab7c11aa52778ab5cb643a77822c22b2fe095f85c9b7d190bcc238ea16ac7`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a9c64b8971dec10ebf4d5de8bf09819554f604405c3970efac75d7011fac2fa`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d316aea26790a987b4b93cbfb7834802d22f48537e98c202917c9b905f5ee1`  
		Last Modified: Fri, 18 Apr 2025 03:30:17 GMT  
		Size: 527.0 MB (526970272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b399594b5463df25bef9837a0c587697f43314a21179182d1b0baf1226b78e4`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48166358ffd0bd636f7ec971d79a276e78714f284a54563a02057bf471419553`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbdc83b6a1da48d21fc098df4f7a6e06ac0f8ef3a70736659fc36e3792556cb`  
		Last Modified: Fri, 18 Apr 2025 03:29:34 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
