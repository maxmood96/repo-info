## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:ed199087b219379d28b25a5e54933023d94d28ba95324a2f939fa9ad39597c29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:78412e6dcbbaaee1ad2591a64b56202326876d7cba85a00b5dbfb001cccce7b6
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2935867325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26572edf84dc7d7b7c5deda6c75890e3a41a856320de57097026915b54b15abc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:28:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:28:40 GMT
ENV MONGO_VERSION=8.0.8
# Fri, 18 Apr 2025 03:28:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Fri, 18 Apr 2025 03:28:41 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Fri, 18 Apr 2025 03:31:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:31:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:31:06 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:31:07 GMT
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
	-	`sha256:1d2f43a262d308cfe1f268287e4fe56c5ef247a93dee890eba1f83fc06ea2927`  
		Last Modified: Fri, 18 Apr 2025 03:31:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8693d0a96489660d79cc622375e5a68b93f769d636262b560e16c24981c831a9`  
		Last Modified: Fri, 18 Apr 2025 03:31:10 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6c5bd9c1e8cfa1f8894962056e9cfacdf08d8f949e9b563c2c586652cf49aa`  
		Last Modified: Fri, 18 Apr 2025 03:31:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23591c367ea3efce2db797fbe89ee62ead09fb3ebe93b7662c1db5a0defd9519`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b595492909e0d220b0044379bd60f637e565fe24df29d5ef535655ebd56dd15e`  
		Last Modified: Fri, 18 Apr 2025 03:32:11 GMT  
		Size: 770.3 MB (770332486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9e1cd493039565bb8392cbef46fdb31c898536e6e86b12bea0b2f374eb6913`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a13f3c38e97424c30cb2ffe6b9ea782388b4965196cf42b6907b5f7482b39a85`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a1a5c4a5f14d76766678956edc63e6c7ac69f70bbf40fcf5d5b39cf35f30f`  
		Last Modified: Fri, 18 Apr 2025 03:31:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
