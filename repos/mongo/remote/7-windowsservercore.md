## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:54904f95165d3772460bb147878c78f230d4b4b3a4ff75762f895fb2f46e5ac1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull mongo@sha256:ece19c94f007ec0babd8af55e92abaeeec9ee709fd09972d5d4387043506949c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (4007818698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35bea149b1af1168e7f371a2f5dc63e03c7f406601dccc0fd191362214ae9227`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:21:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:21:20 GMT
ENV MONGO_VERSION=7.0.19
# Fri, 18 Apr 2025 03:21:21 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.19-signed.msi
# Fri, 18 Apr 2025 03:21:22 GMT
ENV MONGO_DOWNLOAD_SHA256=815ab9b621acea764f1ecc99c0b686162116ded842a384e4b280713343a3bf9b
# Fri, 18 Apr 2025 03:22:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:22:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:22:43 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:22:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73c2d9ff4d6942332cab8ad7ce65e6bb0a1d230c41afced957bb4de25f018dbd`  
		Last Modified: Fri, 18 Apr 2025 03:22:49 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e97adc6144862b44817898597929fbf82c11ec310e39af5b433718345c6a6a`  
		Last Modified: Fri, 18 Apr 2025 03:22:49 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59de38f60fc28820e3cb6f8288d26ba191858e3efa23880b606412b63680d447`  
		Last Modified: Fri, 18 Apr 2025 03:22:49 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667bf6be2a92ab9879d89ae6e2f3aec97be7cb752f67bdcd29a31fdbd32b080a`  
		Last Modified: Fri, 18 Apr 2025 03:22:48 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890a08030d769352c944724ee3f2c446a9bf9f8075225a69694c514f62fb1432`  
		Last Modified: Fri, 18 Apr 2025 03:23:47 GMT  
		Size: 612.6 MB (612648042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07cd53d9068ce4c11479b000308dab231f2c8786022db1e65bf8c8fca4e6433d`  
		Last Modified: Fri, 18 Apr 2025 03:22:48 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1ab4632c5c5c8e57582f24ac0b2df9809f849eb0f27fc924fa946d6517124f7`  
		Last Modified: Fri, 18 Apr 2025 03:22:48 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07a395e7d82b8f679bb88db893b8b60bfb624edde21623d691127b67177f91a`  
		Last Modified: Fri, 18 Apr 2025 03:22:48 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull mongo@sha256:04282642264cd829f139d26268036bf877be19614506994cdf6f8053fd55c120
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2886240083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7d323e64a1b2c89034fc2b9d0797a904da29c7339c27d68ea74679c504fba54`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:25:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 18 Apr 2025 03:25:05 GMT
ENV MONGO_VERSION=7.0.19
# Fri, 18 Apr 2025 03:25:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.19-signed.msi
# Fri, 18 Apr 2025 03:25:07 GMT
ENV MONGO_DOWNLOAD_SHA256=815ab9b621acea764f1ecc99c0b686162116ded842a384e4b280713343a3bf9b
# Fri, 18 Apr 2025 03:26:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:26:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 18 Apr 2025 03:26:18 GMT
EXPOSE 27017
# Fri, 18 Apr 2025 03:26:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c5b7072fee1b8a3221c827a794645d99e21e2d2fcebbbd0e71f06f26997ff9`  
		Last Modified: Fri, 18 Apr 2025 03:26:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96cd42293001a3ae1b3874e89771df68afd36579958cf8757ec5695976cb4ea1`  
		Last Modified: Fri, 18 Apr 2025 03:26:25 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becef1e64ec65d3cda60c38f288c9910236f4c66b66d257daa0abc6246456454`  
		Last Modified: Fri, 18 Apr 2025 03:26:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:962763d1cb0743568be800c274af781a462f4037050f75b10bbf5d4b84302ee0`  
		Last Modified: Fri, 18 Apr 2025 03:26:23 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6de5853de4c2ff1ba98120c69021fef06cb1ae03f80e5736a9d57315f656a76`  
		Last Modified: Fri, 18 Apr 2025 03:27:13 GMT  
		Size: 612.6 MB (612648524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaa712238e8dc83b1235b4c7585f3716817a2595da51f53d2bcc529208b775c3`  
		Last Modified: Fri, 18 Apr 2025 03:26:23 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af03635df351c1e88da3163837a4ae27f3e72c766d3b645caa2202abb6f27e9e`  
		Last Modified: Fri, 18 Apr 2025 03:26:23 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62197c2bce3eae11d81f6717d547760c4d1d694db8202f7eec9f68eb2d3a1114`  
		Last Modified: Fri, 18 Apr 2025 03:26:23 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.17763.7249; amd64

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
