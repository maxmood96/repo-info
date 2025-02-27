## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:dcb4b9562253eaca2897cea323ad5291b5782e87b2a3ee7068574f8461febd81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `mongo:6-windowsservercore` - windows version 10.0.26100.3194; amd64

```console
$ docker pull mongo@sha256:c1a683605dbe74924db1575ba148a902295091011c1be867dfc442820277efd2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3343646749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa208a6c79806fbe2b120ea3e0111380724b244019e1bfd8c8e2fc30668e9c6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 27 Feb 2025 18:18:56 GMT
ENV MONGO_VERSION=6.0.20
# Thu, 27 Feb 2025 18:18:56 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.20-signed.msi
# Thu, 27 Feb 2025 18:18:57 GMT
ENV MONGO_DOWNLOAD_SHA256=518cf974540402bd2992996372d29dd13912e2662d2288649e7984ed091a5e5c
# Thu, 27 Feb 2025 18:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 27 Feb 2025 18:20:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 27 Feb 2025 18:20:08 GMT
EXPOSE 27017
# Thu, 27 Feb 2025 18:20:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7cffb015dd0bbc3cb3a6bdc87583003ced666c7e884ed5d90402622e140459`  
		Last Modified: Thu, 27 Feb 2025 18:20:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d901324cd787cd8f256160071a7b8aecdd52d54d30791beec72599d522cf89`  
		Last Modified: Thu, 27 Feb 2025 18:20:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9306133314e40c122488f73fe40333f6d1cc8e0a15e5f2a4a163f204ab0a01`  
		Last Modified: Thu, 27 Feb 2025 18:20:14 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4aef4b609292cace1760d0f02a5bb3962ab816fed260ba45ff3d124d95142f`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6ecc7f892abcefca956b11f83f3debccce1f727f850d97e18c006d45499974`  
		Last Modified: Thu, 27 Feb 2025 18:21:02 GMT  
		Size: 527.0 MB (527049985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec70e518058761a833b4fd94b0a00132397e5a00987ea78a2b1ac707c2b4cb9b`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf30942b85f4b5a03323c46d30cc861d44fc53479f5985dea086be1d3e5a813`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f060071df79fddf203fa976dfea6656f2ba912962065986b16f9d35b0dc31f9a`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.4 KB (1371 bytes)  
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
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dffb5aacff1c800658f5b18af62c3da8f76e84d72d453bccb0cf39d26673af9`  
		Last Modified: Thu, 13 Feb 2025 00:40:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a4c0356fcaba206bd1d631ce9fcefbc6099e9fb54b98483531e5496a23bf745`  
		Last Modified: Thu, 13 Feb 2025 00:40:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec89274411e23f38af322e986eb8e4ec6f34a7ac5398f4d1445bc4569226f97a`  
		Last Modified: Thu, 13 Feb 2025 00:40:13 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c0b88162244537d9939df218b477bc648f280999149173d2109f04b07ca69e`  
		Last Modified: Thu, 13 Feb 2025 00:40:12 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e686a43f5c84961f09dee0c9fb4598e210b23da24bde5f6e14057aa7502f7f`  
		Last Modified: Thu, 13 Feb 2025 00:40:57 GMT  
		Size: 527.0 MB (527022888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90edf7936751c679e0ac8276153dd89fdc4aa344a502c764da60a7129b01e245`  
		Last Modified: Thu, 13 Feb 2025 00:40:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7fba7fc87211abeaa30a394844cc1d35d31cd9313514a0b13ba34a5ad0d0d0b`  
		Last Modified: Thu, 13 Feb 2025 00:40:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:462fee53de1df907ac83f738d04f6c2851bbbf19254f0c785fb21bf91e4adafd`  
		Last Modified: Thu, 13 Feb 2025 00:40:13 GMT  
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
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a011eff9e8ecfeccf1538251586ade8a6b9c8cfe65461f13cd9e4ae3958ad6`  
		Last Modified: Thu, 13 Feb 2025 00:36:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a76d0bd6358d0bac3edc6b749319fb7c591beb8dbb3d0568a224744932518e`  
		Last Modified: Thu, 13 Feb 2025 00:36:53 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9737368fc845a16e1bfb82bf8db5fb7867ad5c180c7a6291abcdfc2fa7ee6964`  
		Last Modified: Thu, 13 Feb 2025 00:36:53 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260242d33de2e3536a369a13ac77ffbf16a8f4842eec8bebce99ccc958195af6`  
		Last Modified: Thu, 13 Feb 2025 00:36:51 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb176f67d9263d0d403bff8c563a0c61c3c314d3a8b8a2808d09ba0742161006`  
		Last Modified: Thu, 13 Feb 2025 00:37:34 GMT  
		Size: 527.0 MB (526988924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ec58391dfd3ed478047890f06c1ec9f58efb3763e4ad95b89b5a95a0025a4d`  
		Last Modified: Thu, 13 Feb 2025 00:36:50 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca216b80630e1f3fc4fb828229fc85f097ff7071a67e17c9f0cee4cf0a87ce75`  
		Last Modified: Thu, 13 Feb 2025 00:36:50 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:441330c975c0cec95053ede21c9915b0072d72e9767789170bc7f7929609a01c`  
		Last Modified: Thu, 13 Feb 2025 00:36:50 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
