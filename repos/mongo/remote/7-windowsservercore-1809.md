## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:bd1ad175b6ee4d31a0a62a7a183f5e603646ded381a57b1092640c5b2c5dfaa0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:a588134a37f27e925081cc375b3abf9f73062eac6de12eff9ac94c1b510481b3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2778183806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5841bdf0fdd64cab474acde95d0dd9a553fd23796571ae1e752ba17a5614921`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:21:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:21:16 GMT
ENV MONGO_VERSION=7.0.19
# Fri, 18 Apr 2025 03:21:16 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.19-signed.msi
# Fri, 18 Apr 2025 03:21:17 GMT
ENV MONGO_DOWNLOAD_SHA256=815ab9b621acea764f1ecc99c0b686162116ded842a384e4b280713343a3bf9b
# Fri, 18 Apr 2025 03:22:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:22:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:22:46 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:22:46 GMT
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
	-	`sha256:56835393ad3c890eb322e986aa0e91498af09073e8fa3cd144ac272c98342cee`  
		Last Modified: Fri, 18 Apr 2025 03:22:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f973cee713af7b34180ab5d8b06a510b14aafd614596944d22a30d115dbd4e01`  
		Last Modified: Fri, 18 Apr 2025 03:22:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce950f468917856ee3731e299571341558b56be0fa6431730d8ffd5e4065b5e2`  
		Last Modified: Fri, 18 Apr 2025 03:22:53 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fdeb688244ad10d0763f9320d21c7353475b893825f81e77d41690017b3c23`  
		Last Modified: Fri, 18 Apr 2025 03:22:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82f9b35a4f51318636f0f7a8d4e8e2ce0b0aeddec50ab90431278ea52351417e`  
		Last Modified: Fri, 18 Apr 2025 03:23:40 GMT  
		Size: 612.6 MB (612648904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac25bc4abaa12b3a421905ed44423d2d686f1f971697989148176e4bcf0d8b61`  
		Last Modified: Fri, 18 Apr 2025 03:22:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74935dc0eccc8f1c6bb6ed15c24c5d0b62b82076aff98d9d8bd8e3ae0c8b19d4`  
		Last Modified: Fri, 18 Apr 2025 03:22:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315ec52930ff653a2100c1bcfe6efaf97396a010ca3e5b5d1239c6588df69f07`  
		Last Modified: Fri, 18 Apr 2025 03:22:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
