## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:9ed10eb725e5631e2e86a6d316227799302ef71d402bbfd4fef915840be09a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `mongo:4-windowsservercore` - windows version 10.0.20348.768; amd64

```console
$ docker pull mongo@sha256:3de602dc9498c5ae5531e2c786053821e1e0c8bd008e3e0542f5220166fb30a7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2521890443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:209fa66374ea9f3919e5bc40657783321b1c690cf19d7870d23e5835e34fa6f1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 09 Jun 2022 04:32:50 GMT
RUN Install update 10.0.20348.768
# Wed, 15 Jun 2022 14:31:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 05 Jul 2022 23:16:23 GMT
ENV MONGO_VERSION=4.4.15
# Tue, 05 Jul 2022 23:16:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.15-signed.msi
# Tue, 05 Jul 2022 23:16:25 GMT
ENV MONGO_DOWNLOAD_SHA256=cac59647e791ef572d2706c82ed3d5e8fdb2c93e0680a3d18a8a831e7ee35a36
# Tue, 05 Jul 2022 23:17:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 05 Jul 2022 23:17:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 05 Jul 2022 23:17:48 GMT
EXPOSE 27017
# Tue, 05 Jul 2022 23:17:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6c71967ff41928927e4c407171e4ffbac3c9ab4221eb64f5ca5a34ff4c230567`  
		Size: 841.6 MB (841600427 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3379fc6ae767c051adebaf0b48ae517fb6ba89d6b73c778e3e5675865b8b44fb`  
		Last Modified: Wed, 15 Jun 2022 16:17:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0fb78e544b68bdd679698295b17c1fd6342604eb73ac5a0e26e1cbb8585f3e`  
		Last Modified: Wed, 06 Jul 2022 00:18:53 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2716b35ec5fe63b4b7a1cf67ff12416ef1fbe5d06be3b9f069c29d56682cd79`  
		Last Modified: Wed, 06 Jul 2022 00:18:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86da303323f2120a471ff7f68d6dce1a01122195e47c810590fcf0d86dfd156b`  
		Last Modified: Wed, 06 Jul 2022 00:18:50 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d003018ebb745c6be7c10130b6eae45d4c5e80676725171d044a40e3b19d607e`  
		Last Modified: Wed, 06 Jul 2022 00:19:46 GMT  
		Size: 243.4 MB (243416477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a929d69918c2a8f01a83bfee04a3d7a723e37bd689b5f1f05001b32b08428f`  
		Last Modified: Wed, 06 Jul 2022 00:18:50 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4003a4d7fbd11d845e52c1634ba1ebfd4feb0f56a10eadf5d883ccf7ba6ed613`  
		Last Modified: Wed, 06 Jul 2022 00:18:50 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8c708bdb00bf88d40e3a9c2ab87c581b4bb31d22cccd84730f2c839e4477230`  
		Last Modified: Wed, 06 Jul 2022 00:18:50 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.3046; amd64

```console
$ docker pull mongo@sha256:5566d8328c52807d6210a9a8a202691285252eac1e1dcaf1870809b48757cf3a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2906475306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c886ebb268d02b64c10fe08729748f80a36079270064decb2b1343bd29d2122`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 09 Jun 2022 19:41:03 GMT
RUN Install update 10.0.17763.3046
# Wed, 15 Jun 2022 14:40:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 05 Jul 2022 23:18:08 GMT
ENV MONGO_VERSION=4.4.15
# Tue, 05 Jul 2022 23:18:09 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.15-signed.msi
# Tue, 05 Jul 2022 23:18:10 GMT
ENV MONGO_DOWNLOAD_SHA256=cac59647e791ef572d2706c82ed3d5e8fdb2c93e0680a3d18a8a831e7ee35a36
# Tue, 05 Jul 2022 23:20:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 05 Jul 2022 23:20:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 05 Jul 2022 23:20:32 GMT
EXPOSE 27017
# Tue, 05 Jul 2022 23:20:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc6ae6c5aa2b4920ae68469c5e7e7c3a3c85e5eaafc24660e7b3adb21d6fce77`  
		Size: 786.1 MB (786113785 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:14def1e29581c5e5d0af7fdf9ff44ed6536e79561eb0f0cdff89e322fb87c423`  
		Last Modified: Wed, 15 Jun 2022 16:18:14 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fff3e536a5cd292cb620d4ef63470b6a039c66dfc6bef49fbf6fcde68c0bb06`  
		Last Modified: Wed, 06 Jul 2022 00:20:01 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031012493e2d7d70c3c9727cd884ab2f0d8e13b4325939e62b4ad6a3100c02ad`  
		Last Modified: Wed, 06 Jul 2022 00:20:01 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de97098f1500beaacde82c1f52f3bcac884fc9937484bc176f4add477574c4c2`  
		Last Modified: Wed, 06 Jul 2022 00:19:59 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246f57bc34f1672e0b59801a990ef1b7c54b85e962e2ebf2f0f327c73388b9a0`  
		Last Modified: Wed, 06 Jul 2022 00:20:45 GMT  
		Size: 243.2 MB (243185514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc681ba90bc68738f088684cbe0dc3ae9d9385ddf2cdb11c1205ea83a0c1fb12`  
		Last Modified: Wed, 06 Jul 2022 00:19:59 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2635afef452cddc301c9e8e281e38ab74bdb107748d302ea92f24daa9de6f226`  
		Last Modified: Wed, 06 Jul 2022 00:19:59 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd1589ef0fe534e03fe012846aa0486753fb00a943861182aa2ce718885baf5`  
		Last Modified: Wed, 06 Jul 2022 00:19:59 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
