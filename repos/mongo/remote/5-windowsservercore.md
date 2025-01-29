## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:af4c98789a6976557489aef5c4d8e7aa881b26f5e04b76d3bb558c230f2d1187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `mongo:5-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull mongo@sha256:9162937e13442ffdd8625f2b301451e52c00326f8e0d0fb0bc2ee66762f372d9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2813860751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f1a4bbae84e6494cd912588108036889645c1e34b013cd779148621cfbd1d24`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 29 Jan 2025 01:30:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 Jan 2025 01:30:43 GMT
ENV MONGO_VERSION=5.0.31
# Wed, 29 Jan 2025 01:30:44 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.31-signed.msi
# Wed, 29 Jan 2025 01:30:45 GMT
ENV MONGO_DOWNLOAD_SHA256=fd7fdc89d5caeb56a86f5a5f67007435a48af9c80407b181b6edac0945bb2e63
# Wed, 29 Jan 2025 01:31:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 Jan 2025 01:31:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Jan 2025 01:31:41 GMT
EXPOSE 27017
# Wed, 29 Jan 2025 01:31:42 GMT
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
	-	`sha256:0c535544cf5630f54fd992faaf4d509d0efca5001ff49489ff05b45c720f1367`  
		Last Modified: Wed, 29 Jan 2025 01:31:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb53542b7c852b57b9e3d5a11adccdc723e8c8720dfdc94cc291f6cfaaf08ac`  
		Last Modified: Wed, 29 Jan 2025 01:31:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c0b06721350c3b3931567998b9f03ebe4f16dfb08cc15094e49ea868371e3d5`  
		Last Modified: Wed, 29 Jan 2025 01:31:45 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1949fb0fb8693a6c07e2d62e3d3c70957b41b66ac485305cdde592046c2b718b`  
		Last Modified: Wed, 29 Jan 2025 01:31:44 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdaf0919729b675cc2f6b96020a5dfca19e4bf0444dec4714214600529b9d23`  
		Last Modified: Wed, 29 Jan 2025 01:32:21 GMT  
		Size: 313.6 MB (313574041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f47d8401926f0dfb3ab088daddf3e0b8cc200f23976df1b3453afd51742c85b4`  
		Last Modified: Wed, 29 Jan 2025 01:31:44 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9a07b617038b82447bd2dd00eb53d31ca9944c2b244171583d5938509939cc`  
		Last Modified: Wed, 29 Jan 2025 01:31:45 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0f4003184b845fb09d8bfa0844600172b3e2c7c3cc1844ebebedbfd9d07b9b`  
		Last Modified: Wed, 29 Jan 2025 01:31:45 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull mongo@sha256:b18db1dd16275a2429a243905c4b9d4c280ae519e6ac8306afa630a91706ee8d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2575939128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d02c564dbacd4ff1c19507595cfa68d5ab627042c6e0f334b3491a66170315a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 29 Jan 2025 01:26:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 Jan 2025 01:26:53 GMT
ENV MONGO_VERSION=5.0.31
# Wed, 29 Jan 2025 01:26:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.31-signed.msi
# Wed, 29 Jan 2025 01:26:54 GMT
ENV MONGO_DOWNLOAD_SHA256=fd7fdc89d5caeb56a86f5a5f67007435a48af9c80407b181b6edac0945bb2e63
# Wed, 29 Jan 2025 01:28:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 Jan 2025 01:28:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Jan 2025 01:28:36 GMT
EXPOSE 27017
# Wed, 29 Jan 2025 01:28:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4409590a814fe8cd443b306593fc7a189dcb10767c8d3e24a1def8fed5c23115`  
		Last Modified: Wed, 29 Jan 2025 01:28:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d71d234ed8d36c9f170ee7ef51ea5967cc722dcb2dad803180ed90614845d9`  
		Last Modified: Wed, 29 Jan 2025 01:28:42 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c391821969e76f17a8cce177f482d828649953701b0145a5efba8a4e56ebb44b`  
		Last Modified: Wed, 29 Jan 2025 01:28:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b663826ed738cb67abb6c5cc704a475e34b90d980bdee060ff34cc80337d3b`  
		Last Modified: Wed, 29 Jan 2025 01:28:40 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7f59590bf7e10981e26b3a4f4e053bbb6926443bc00839dcab2f19086daeeb`  
		Last Modified: Wed, 29 Jan 2025 01:29:10 GMT  
		Size: 313.5 MB (313544816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b636f69e01be06912697b6cb87d874ef9c8fb196486c86a537ad975e874f7`  
		Last Modified: Wed, 29 Jan 2025 01:28:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5c1e04b3bd9fd6001fdc54412358d5c1a1b81c230a166079e23a4938e290610`  
		Last Modified: Wed, 29 Jan 2025 01:28:40 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808632afc61c0eb5ad84a86e841a4065eeb4cf503879896f753ccfeb16329243`  
		Last Modified: Wed, 29 Jan 2025 01:28:40 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:f95cd66e3737a05b228c1ef0bfbf3cdbc339c4ce1b65f35fecbbb741f7d6fbc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2435762086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca334cd1f8a6f2795b49d25424621dbac18cd82475ddd225db03996c5cb63919`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 29 Jan 2025 01:26:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 29 Jan 2025 01:26:46 GMT
ENV MONGO_VERSION=5.0.31
# Wed, 29 Jan 2025 01:26:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.31-signed.msi
# Wed, 29 Jan 2025 01:26:47 GMT
ENV MONGO_DOWNLOAD_SHA256=fd7fdc89d5caeb56a86f5a5f67007435a48af9c80407b181b6edac0945bb2e63
# Wed, 29 Jan 2025 01:27:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 29 Jan 2025 01:27:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 29 Jan 2025 01:27:57 GMT
EXPOSE 27017
# Wed, 29 Jan 2025 01:27:58 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c31250104fa721b9de3449dc8a61f5b06ad81d9b686a166ebc48cab43e973037`  
		Last Modified: Wed, 29 Jan 2025 01:28:04 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764fc478820f9c0c3b43957224922bdc78bb4e6ada06b473c6bceb33ae760954`  
		Last Modified: Wed, 29 Jan 2025 01:28:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6a308b5dd58790b8d6c624eacec291968600c43f544098383754be78c3385d7`  
		Last Modified: Wed, 29 Jan 2025 01:28:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dba4c5e6119b66af25dea4428b63b45c9f0da357d1c16f144b5510318cbfb8`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848afb43bf95b16c28527bd086c420017fad290302ce03ea44563ae408e26813`  
		Last Modified: Wed, 29 Jan 2025 01:28:32 GMT  
		Size: 313.5 MB (313540867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58cb2e40aa062792d48159e526902c03f5f50adacd7474277cfb92738a98aee3`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd640a6d77665062ee2b7b524df0cf22244c0b8c51d7001c96bb6be0303520f`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ba7ef6452bce86d8da5bc0f9d5e890c69550366174ea7bc2b41c8c74aa765bc`  
		Last Modified: Wed, 29 Jan 2025 01:28:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
