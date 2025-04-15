## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:216f60962ef9afa3be200c5fc17c54b53b47cf53918ec990d4269861ab937c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:58103ae024c00b16ed46b55189fc2218a86cd354458b479a36615667c0b9e97a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2933050052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebea519f0c160bb90e3dc16480e64595e3204ff09e64b6f84dc18c3eff71b39`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Mon, 14 Apr 2025 23:07:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:07:09 GMT
ENV MONGO_VERSION=8.0.8
# Mon, 14 Apr 2025 23:07:10 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Mon, 14 Apr 2025 23:07:11 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Mon, 14 Apr 2025 23:09:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:09:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:09:18 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:09:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba63a614e4961406ee57f2b3cbbf0e9f2f575d620b30e1c4d0d3587d7dd908b`  
		Last Modified: Mon, 14 Apr 2025 23:09:22 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e6083570406ee1589ca6f567b74f28f6cd28ece847e898feea5318b29257ca5`  
		Last Modified: Mon, 14 Apr 2025 23:09:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c94f6dbd82b369ee4f4463a1c11a2e119c9b079f1ecf258919133788e8f8b43c`  
		Last Modified: Mon, 14 Apr 2025 23:09:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f463dee2349393ec3d7c86edf41226311943db5213411471b6b81530bb18a2`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84273db5c5b344d59a16022ebed0cd2008087d9fb794392de7b24b99a275171d`  
		Last Modified: Mon, 14 Apr 2025 23:10:23 GMT  
		Size: 770.3 MB (770315156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1afb484edc3ec136e9329243d3942a86b67c2374a5305fb99514e399b9c0e41d`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7636dc854e4edfb4d9c26e90420ce3253ac61782cf47859fccb3e8d012548a6`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382d52a299fe0a0570c9ec85876bedf3e6005d4584f248db2d495d3dc646ef91`  
		Last Modified: Mon, 14 Apr 2025 23:09:21 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
