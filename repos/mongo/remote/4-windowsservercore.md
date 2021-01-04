## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:ec3ea97c48dedf9707ec201072abde21fa34708c1f706781bb202916b97c64f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `mongo:4-windowsservercore` - windows version 10.0.17763.1637; amd64

```console
$ docker pull mongo@sha256:44453059167806e68701c5f7f3a175862f0b5f875238674bb25c39daa218851c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2630730135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ba2649cdb467ccd36fb65e7a285ae18d7d19d01c9485993e173038920f258a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 14:02:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 04 Jan 2021 22:23:34 GMT
ENV MONGO_VERSION=4.4.3
# Mon, 04 Jan 2021 22:23:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.3-signed.msi
# Mon, 04 Jan 2021 22:23:35 GMT
ENV MONGO_DOWNLOAD_SHA256=d811282527bbdc3266244209ad0971c0d375dbb209bb8eb4ae66ba576b19e9f6
# Mon, 04 Jan 2021 22:26:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=ServerNoService,Client,Router,MiscellaneousTools' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 04 Jan 2021 22:26:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 04 Jan 2021 22:26:52 GMT
EXPOSE 27017
# Mon, 04 Jan 2021 22:26:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:240407eb82b6591b0574396ec829a4a5cd9a75257a4663f9876942995275965d`  
		Last Modified: Wed, 09 Dec 2020 17:10:14 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22061bafff402fecdcfdc393917a5e27f9b8eb154f2e9fbb62ed7fd1c804a98f`  
		Last Modified: Mon, 04 Jan 2021 22:34:26 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee22bb8acd20531fd59b42a44f1dccaee8a63059c5ee8a56caffd08135c41b2f`  
		Last Modified: Mon, 04 Jan 2021 22:34:26 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0009b56252b87261ace9d78c1c3d436d96efa891747bf7f8136f712e3cdbb27`  
		Last Modified: Mon, 04 Jan 2021 22:34:23 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a09e7a998b53c1340ad67ce780b4ca0cd1e6d02bec1244b1a678b38cf13f3b27`  
		Last Modified: Mon, 04 Jan 2021 22:35:05 GMT  
		Size: 239.8 MB (239847774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74eb0c6548847cf74fe9f19063d7a41044da83d9b59f43ae2f82546b61c82e19`  
		Last Modified: Mon, 04 Jan 2021 22:34:23 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b84110c2b55ac75c1cbd9492fb995107756a4476863348846da2b56b57bb46`  
		Last Modified: Mon, 04 Jan 2021 22:34:23 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f03299f3178458c7a31a86086503a2226c8454be9b1b8ccbd903303d0bc940f`  
		Last Modified: Mon, 04 Jan 2021 22:34:23 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull mongo@sha256:78ef64ede71474e410c48188797f133a162463abfe110c5b086b83a8d3b75878
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6009434039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdcba5af7daaed9966caa30e82279cee5e2d348e806825b7a338520a3ab29f80`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 14:41:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 04 Jan 2021 22:27:02 GMT
ENV MONGO_VERSION=4.4.3
# Mon, 04 Jan 2021 22:27:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.3-signed.msi
# Mon, 04 Jan 2021 22:27:03 GMT
ENV MONGO_DOWNLOAD_SHA256=d811282527bbdc3266244209ad0971c0d375dbb209bb8eb4ae66ba576b19e9f6
# Mon, 04 Jan 2021 22:31:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=ServerNoService,Client,Router,MiscellaneousTools' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 04 Jan 2021 22:31:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 04 Jan 2021 22:31:07 GMT
EXPOSE 27017
# Mon, 04 Jan 2021 22:31:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5a79f8be42bf1c358ccc82f32c1481de95c393ef97e712a321c1440d132fda9`  
		Last Modified: Wed, 09 Dec 2020 17:11:03 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66ed6eabbe0629def987ae9a59ab4143065625906ec580605b376f2965b80cec`  
		Last Modified: Mon, 04 Jan 2021 22:35:31 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcd8c68224aa353f236c72cd255b2c810310e6d1e2b18421bb4acbc59d2c08c`  
		Last Modified: Mon, 04 Jan 2021 22:35:30 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277e63f380b12813c6508f90e8dbc1fc120b66eca072cfa955ed3eada4dc5d2c`  
		Last Modified: Mon, 04 Jan 2021 22:35:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924c1827532309ab811fe6c8237889ff0609cb18b38a25a616de7137faa2b305`  
		Last Modified: Mon, 04 Jan 2021 22:36:10 GMT  
		Size: 240.6 MB (240581996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f8b6f894aaab562049aa7a75e4634c6393b482d866481e175112102349f4b83`  
		Last Modified: Mon, 04 Jan 2021 22:35:27 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b152601fa94b531b76e92551e4d579965e456e5b315f0289f784691512b806ac`  
		Last Modified: Mon, 04 Jan 2021 22:35:27 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2d804f27797906f589ac7bc283c328314f27f95a9155f386b6768d9528cf3e`  
		Last Modified: Mon, 04 Jan 2021 22:35:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
