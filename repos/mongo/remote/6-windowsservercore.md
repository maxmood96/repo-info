## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:ce18302023d6429e850bfdb30b1ad6aadb823ce33c7a04ec7e688767caa27b4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `mongo:6-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull mongo@sha256:55544fc4c7bffdf793e760fbdd7558f2332456db4168208a86e2b32ff06de1b9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3027325858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7281c494a5a561bcd920b4329003f00228fe0b2f08bbd47715e3352fcbad493d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 22 Jan 2025 20:35:18 GMT
ENV MONGO_VERSION=6.0.20
# Wed, 22 Jan 2025 20:35:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.20-signed.msi
# Wed, 22 Jan 2025 20:35:19 GMT
ENV MONGO_DOWNLOAD_SHA256=518cf974540402bd2992996372d29dd13912e2662d2288649e7984ed091a5e5c
# Wed, 22 Jan 2025 20:36:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 20:36:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 22 Jan 2025 20:36:25 GMT
EXPOSE 27017
# Wed, 22 Jan 2025 20:36:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Wed, 22 Jan 2025 06:04:03 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10e5d88fee4b3b7f74dba52cfb6af6270ef5befca6199b600bdcbfd7e804148`  
		Last Modified: Thu, 23 Jan 2025 01:18:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:670cfe13867757e4d4fee78fa9521d1e9d780fc2a461ad987184ca2e2904c1a4`  
		Last Modified: Thu, 23 Jan 2025 01:18:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97975b1e711e9ae750b4bcd285804c8512163a64fd185d151e0fb153281601ab`  
		Last Modified: Thu, 23 Jan 2025 01:18:19 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c43c1aca0e6b7eaa75f1b2b16021ae29acd29704b97a92f2348d1f89c60eb44`  
		Last Modified: Thu, 23 Jan 2025 01:18:19 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14827e71c9fa93e9fb8607ce15dfbbb7b9cf31924e0457345a01adf37c6c1a68`  
		Last Modified: Thu, 23 Jan 2025 01:18:36 GMT  
		Size: 527.0 MB (527039195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dd3ad5160dfdfaf58a2c12e5c0d227b61e0e68ddafec9045841184f7c2aa50e`  
		Last Modified: Thu, 23 Jan 2025 01:18:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ecfcb046358ad54063c83a4008b3739952b6bbe724f3901b997a8cd277df8d`  
		Last Modified: Thu, 23 Jan 2025 01:18:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b5e995910437633436955a96cbd573853432dc17af7048883196aaa65d0cbf`  
		Last Modified: Thu, 23 Jan 2025 01:18:21 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:05f88a660b581acbea8df599bf6cd88f15f431652b457dc6741cafe0fff7e027
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2790889908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2343559f5d7ada83184d5e60739be29ff1de7e3d81c02fb1ceed5e4f130d954e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Thu, 13 Feb 2025 00:39:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:39:05 GMT
ENV MONGO_VERSION=6.0.20
# Thu, 13 Feb 2025 00:39:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.20-signed.msi
# Thu, 13 Feb 2025 00:39:06 GMT
ENV MONGO_DOWNLOAD_SHA256=518cf974540402bd2992996372d29dd13912e2662d2288649e7984ed091a5e5c
# Thu, 13 Feb 2025 00:40:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:40:09 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 00:40:10 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 00:40:10 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Wed, 12 Feb 2025 22:14:21 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dffb5aacff1c800658f5b18af62c3da8f76e84d72d453bccb0cf39d26673af9`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c0356fcaba206bd1d631ce9fcefbc6099e9fb54b98483531e5496a23bf745`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec89274411e23f38af322e986eb8e4ec6f34a7ac5398f4d1445bc4569226f97a`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c0b88162244537d9939df218b477bc648f280999149173d2109f04b07ca69e`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e686a43f5c84961f09dee0c9fb4598e210b23da24bde5f6e14057aa7502f7f`  
		Last Modified: Thu, 13 Feb 2025 01:09:11 GMT  
		Size: 527.0 MB (527022888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90edf7936751c679e0ac8276153dd89fdc4aa344a502c764da60a7129b01e245`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fba7fc87211abeaa30a394844cc1d35d31cd9313514a0b13ba34a5ad0d0d0b`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462fee53de1df907ac83f738d04f6c2851bbbf19254f0c785fb21bf91e4adafd`  
		Last Modified: Thu, 13 Feb 2025 01:08:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.6893; amd64

```console
$ docker pull mongo@sha256:3ebc79d0f9432d6653643ebdedfb0b1cf8d8eff92f8490eee3ff662afead17f5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2663906806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c2a4e84bde80784ed844096b1fd96861989fb883dbc44ece0dd58ce04e442f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:35:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 13 Feb 2025 00:35:21 GMT
ENV MONGO_VERSION=6.0.20
# Thu, 13 Feb 2025 00:35:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.20-signed.msi
# Thu, 13 Feb 2025 00:35:22 GMT
ENV MONGO_DOWNLOAD_SHA256=518cf974540402bd2992996372d29dd13912e2662d2288649e7984ed091a5e5c
# Thu, 13 Feb 2025 00:36:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:36:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 13 Feb 2025 00:36:46 GMT
EXPOSE 27017
# Thu, 13 Feb 2025 00:36:47 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a011eff9e8ecfeccf1538251586ade8a6b9c8cfe65461f13cd9e4ae3958ad6`  
		Last Modified: Thu, 13 Feb 2025 01:09:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a76d0bd6358d0bac3edc6b749319fb7c591beb8dbb3d0568a224744932518e`  
		Last Modified: Thu, 13 Feb 2025 01:09:17 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9737368fc845a16e1bfb82bf8db5fb7867ad5c180c7a6291abcdfc2fa7ee6964`  
		Last Modified: Thu, 13 Feb 2025 01:09:17 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260242d33de2e3536a369a13ac77ffbf16a8f4842eec8bebce99ccc958195af6`  
		Last Modified: Thu, 13 Feb 2025 01:09:17 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb176f67d9263d0d403bff8c563a0c61c3c314d3a8b8a2808d09ba0742161006`  
		Last Modified: Thu, 13 Feb 2025 01:09:31 GMT  
		Size: 527.0 MB (526988924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec58391dfd3ed478047890f06c1ec9f58efb3763e4ad95b89b5a95a0025a4d`  
		Last Modified: Thu, 13 Feb 2025 01:09:17 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca216b80630e1f3fc4fb828229fc85f097ff7071a67e17c9f0cee4cf0a87ce75`  
		Last Modified: Thu, 13 Feb 2025 01:09:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441330c975c0cec95053ede21c9915b0072d72e9767789170bc7f7929609a01c`  
		Last Modified: Thu, 13 Feb 2025 01:09:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
