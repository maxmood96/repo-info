## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:4482c9e43549ac247aaf4303be16eb22ec7306412f4ac691e3d182906676cfd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull mongo@sha256:6a9a9f2e549368db97c29d9e30baf855a03da3334b8e9d3d9e919766a1677519
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2762718769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbc7ec13e7159620a70aa158d0562f5b774bfaeabebc8bf7193e63d4c5121fd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:01:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jul 2024 17:01:53 GMT
ENV MONGO_VERSION=6.0.16
# Wed, 10 Jul 2024 17:01:54 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.16-signed.msi
# Wed, 10 Jul 2024 17:01:55 GMT
ENV MONGO_DOWNLOAD_SHA256=4a0da9d2a8e7151a2c7c8e68406dce00336f2bb2f6b9f1129184c9888c59e032
# Wed, 10 Jul 2024 17:03:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jul 2024 17:03:29 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jul 2024 17:03:29 GMT
EXPOSE 27017
# Wed, 10 Jul 2024 17:03:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c906486ef3ef625e65019fe94bca1b4a4f3ea5f18c22453fb21a1e60e13d7ed2`  
		Last Modified: Wed, 10 Jul 2024 17:03:36 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b0a4da683d055edc87ba99519bbf6bceebb694f9515781bd142dd2bfdde295a`  
		Last Modified: Wed, 10 Jul 2024 17:03:36 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67d10df55f547e1e1230436540d8326075430da43310316152e2bc8fa68923b1`  
		Last Modified: Wed, 10 Jul 2024 17:03:36 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289cc7738e7c53a9dee6d72039e8dc2016cd223049e24c194985ec09fb2bcc10`  
		Last Modified: Wed, 10 Jul 2024 17:03:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8be3862015623a73242ffc5aa017de6fd5172396e15a3ee2d32184ad617fb42`  
		Last Modified: Wed, 10 Jul 2024 17:04:17 GMT  
		Size: 524.3 MB (524280283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989a027ae8cdaaae8dc02e19cabf10e1f304e806d130fecbbe736a17ad00cdd5`  
		Last Modified: Wed, 10 Jul 2024 17:03:34 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b89445e8c51a2fa32c383dfc5e03cf420242f67fa950733972989861f8874a`  
		Last Modified: Wed, 10 Jul 2024 17:03:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888d278bf3439c767e2d06933864b7cb64f0cdfa3a129eb033a13e18faf56351`  
		Last Modified: Wed, 10 Jul 2024 17:03:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
