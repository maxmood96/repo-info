## `mongo:8-windowsservercore`

```console
$ docker pull mongo@sha256:e17e86659080a61d4bda47cfa3718c80179f5d0eb9cdd2625dc6647b8dffce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `mongo:8-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull mongo@sha256:8f7c9735624ddf9d5b67e51ecd831255ba579011c0af552ec96357854016515f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3268989100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956e2b03ce62058872e3e33f18069da7912ae04c1e1f996ab4110bac1bfa455d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 22 Jan 2025 20:35:37 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 22 Jan 2025 20:35:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Wed, 22 Jan 2025 20:35:39 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Wed, 22 Jan 2025 20:37:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 20:37:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 22 Jan 2025 20:37:22 GMT
EXPOSE 27017
# Wed, 22 Jan 2025 20:37:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b56c5fd6794c07fefaf0232dd4a4029649ef5aafad03b3d876da0984dc2df`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8c121d958eda51211881df659ba4a3c567827216e786eee9b1c6ff12a39fd5`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8092e5dd1bb09ad612b643d4055b4bb34fb7d25f6b4150e626569296662e79`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c392de1897e918f2a1056e13fcc94d9c6d1c66195da9e827c80d8589cc437c`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a895b6f681c6b079586ef7c6669574a6195e010cf7d5e63b7b0cc40557b0`  
		Last Modified: Wed, 22 Jan 2025 20:38:35 GMT  
		Size: 768.7 MB (768702153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d76470dc3e7660d9fa033ce776b68d4c7f3dd2170283cfba127e9d932f4a23`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3ff8753e952f28001ff9b3f6e88cd03cbac0e32a9832b2e9b41e15f4f12a7e`  
		Last Modified: Wed, 22 Jan 2025 20:37:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d3ab988655e45e1a4a8df1efc3d73ad38cf43c5899e5a4e00cbf8a78b856cd`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:8-windowsservercore` - windows version 10.0.20348.3207; amd64

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

### `mongo:8-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull mongo@sha256:b3da5b1ff2071e3e0ea1f4b04b3000239cb05f312e13d69fe541035572561e9a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2905595148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe6640b7e8f284b843bc348c778979b2b147ad28b175671babfee3d8f5dee39`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:33:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:33:16 GMT
ENV MONGO_VERSION=8.0.4
# Thu, 13 Feb 2025 00:33:16 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Thu, 13 Feb 2025 00:33:17 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Thu, 13 Feb 2025 00:35:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:35:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 00:35:23 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 00:35:24 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c3ae7503871f68ad07654150267980535d8a9d2cec2c84a82683598d95a862`  
		Last Modified: Thu, 13 Feb 2025 00:35:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd1c9c6bab98396ae096fc00c343337c6e6a021bd0d083533a2c8f84231141b7`  
		Last Modified: Thu, 13 Feb 2025 00:35:28 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62778542b0cbcfcf34c927da8712b43ce03a8cb14ef04a646748d02102f6ade8`  
		Last Modified: Thu, 13 Feb 2025 00:35:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c51372c1e990b7e87452d7976aa0b9fc4a9cfe5207257cae1bd5e6e41728c3d`  
		Last Modified: Thu, 13 Feb 2025 00:35:27 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148bf2d1f3b7dcb7d8cc00eba467bb018085d87d229040d9d5fa1589a18a85cd`  
		Last Modified: Thu, 13 Feb 2025 00:36:27 GMT  
		Size: 768.7 MB (768677272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62bc6639d9d5b148531f0a779e9d37636eb5f021061f4a427272f6b71bd13f3f`  
		Last Modified: Thu, 13 Feb 2025 00:35:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b2a452a0951d6d468bbfbfa8389575281efbe0371e7de91d8336285af27c21`  
		Last Modified: Thu, 13 Feb 2025 00:35:27 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b1a162a40d679f890536b5d4adf4a6733c8fe717aaa319892e643a90e1ea6bd`  
		Last Modified: Thu, 13 Feb 2025 00:35:27 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
