## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:9dd15f1e5413dd8d2252ce8ef126f3cf4d8625233678f2e4539e33ba7579a709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:4cdc1b42c969779aa235db37bd2032d4039bafe4873cd92815ff6da5fe6b174a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 GB (3188041560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff3f79430666efb79ad68d561dfc49d451739643832d5bb12078a697252376d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 Aug 2022 22:23:14 GMT
ENV MONGO_VERSION=6.0.1
# Wed, 24 Aug 2022 22:23:16 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.1-signed.msi
# Wed, 24 Aug 2022 22:23:18 GMT
ENV MONGO_DOWNLOAD_SHA256=999b39df67a77eda3198f8412dc159b0cd8aa6677b901a0cf287921884306ac3
# Wed, 24 Aug 2022 22:26:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 Aug 2022 22:26:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 Aug 2022 22:26:11 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:26:14 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34716fa1da4761caaad6e9f10e85cc622d30700891d1b9bd5d4a423a40f8631d`  
		Last Modified: Wed, 24 Aug 2022 22:52:01 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d87db2a376c901b76b0863788cd1298471786b9d204bb55b99ed0f804c6958`  
		Last Modified: Wed, 24 Aug 2022 22:52:01 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a4206639ce1c663688d04594a60ba96835f233d935d31464f1ec23036ae5931`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140f1ef13fb603028e27e2b450ced77785ed3b92dc98d854a60570b79d7c47e0`  
		Last Modified: Wed, 24 Aug 2022 22:53:17 GMT  
		Size: 510.3 MB (510318914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:336ed0a278d09575040bcc31ebdc9bfab524cc363df32ebcb5663a77f3f18f92`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b59915d09f1fddc1c80a13998bfc256f358f566e16a84599f3b2deeaf52f0ca`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b685ca4f8bfb31c6fa64a7f3333908590a5a64ee6f62595a87961256233da08`  
		Last Modified: Wed, 24 Aug 2022 22:51:58 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
