## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:16437aeaf82d2f98883ffed9eca017e2e1eb7bc0ef837415e9891988cecb87de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:4737d94ae4d8751369940a86bfd2c995748676a208f380fca39d1f5799f85e90
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3032537546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7ab373633b236cd6d032ca4150978958418058f8d7440980b02209a05562f1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:39:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:39:53 GMT
ENV MONGO_VERSION=8.0.4
# Thu, 13 Feb 2025 00:39:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Thu, 13 Feb 2025 00:39:54 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Thu, 13 Feb 2025 00:41:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:41:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 00:41:20 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 00:41:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4975f734cb8f39ea9dc1cd530259eaff48e98673fc95d7cd0f3c1ee8083539a0`  
		Last Modified: Thu, 13 Feb 2025 00:41:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100b218cbae4606d60a9d4d57f063777682c54ad0a09d110ee77b032c5af0fb4`  
		Last Modified: Thu, 13 Feb 2025 00:41:24 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285a87fab7fa4fa8e8912a658e22004c5ea04364a81137d9c5e90ea293a76bfd`  
		Last Modified: Thu, 13 Feb 2025 00:41:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246ab2c7f8297d5f54f16a7367dc5e816364dc79a8866c55ef61081ea18cc496`  
		Last Modified: Thu, 13 Feb 2025 00:41:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f543e3ed8f3d4e6bbec3077126f10e8935a6557d480a76cf6b6b6ec69abe746c`  
		Last Modified: Thu, 13 Feb 2025 00:42:24 GMT  
		Size: 768.7 MB (768670506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3650ced460cf3ea1439fde0a85c3b52d901ac3c23ae6266665733ba3076e8c`  
		Last Modified: Thu, 13 Feb 2025 00:41:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9199654a3ca0e1a33ce3cd36994fc268e6d7dc84f50aac81f488c00d1aa02a52`  
		Last Modified: Thu, 13 Feb 2025 00:41:23 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87822732e5db248167c3ce8ea042d369d117d44f76350f9d52c49c791518e65`  
		Last Modified: Thu, 13 Feb 2025 00:41:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
