## `mongo:8-windowsservercore-1809`

```console
$ docker pull mongo@sha256:b5dea205d8688b7a81f14f0b123ef9148ffde02349e26cceb5d2cbeff4f5f7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `mongo:8-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:ddd7172f47cdabf8015c8e679277e6b9ef63a53f9cda3ccea9a646bc14df6fec
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2667817002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d294836b58fbd2dc4e4d04c8fcfe303e34946162295e8db59aa58459b022d7cf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:00:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:00:33 GMT
ENV MONGO_VERSION=8.0.1
# Wed, 09 Oct 2024 23:00:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.1-signed.msi
# Wed, 09 Oct 2024 23:00:34 GMT
ENV MONGO_DOWNLOAD_SHA256=303e766388b9965ce5ee40f01df921275fbd53da7ba3d729c8767c4d0de0ce8b
# Wed, 09 Oct 2024 23:02:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:02:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Oct 2024 23:02:16 GMT
EXPOSE 27017
# Wed, 09 Oct 2024 23:02:17 GMT
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
	-	`sha256:e63b93b0bdcdeab3146d2d74645398fa6939e3b0f435c5d1f70461dbbb128c2c`  
		Last Modified: Wed, 09 Oct 2024 23:02:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ca0531cd4572a2f793f2fc7e75abf1e3a85faaeacae0b184c784d882906e674`  
		Last Modified: Wed, 09 Oct 2024 23:02:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2e6454a4597fc0e2a3b0050240f7bbbdf3db05331705a621d8f372992a3913`  
		Last Modified: Wed, 09 Oct 2024 23:02:23 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:262a85d86e89be080b224b7cf593e4566cb8263ace525b74104740a56d37390a`  
		Last Modified: Wed, 09 Oct 2024 23:02:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9125bf5d50ab579bbfcc1751ab8a3a26452ef2ef1c49422274f82034eabf704`  
		Last Modified: Wed, 09 Oct 2024 23:03:20 GMT  
		Size: 766.0 MB (765982654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35e8f8ae99c713c471408b0093337344f41d8ad45ffe0e5c8aea7d98ffe8f6d`  
		Last Modified: Wed, 09 Oct 2024 23:02:21 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6be9a9170f421e71cb48120cd5be3c92b8e96042ac1b8d27ab94b6348bf7ba3`  
		Last Modified: Wed, 09 Oct 2024 23:02:21 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5451e07c019eea53475035504eaf2dec4a17868d56625cffb41b615440a42b35`  
		Last Modified: Wed, 09 Oct 2024 23:02:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
