## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:9e2f4383a15f9569019f6484f06a9f70f236e8d0c525d2486471949d22330281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `mongo:6-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull mongo@sha256:045c507a95f758025bd1fd0c4b35f4c42f3fdf78c19b68557fbc93adf25e8ca3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3921671138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7feae2acecc9bbdda9565df67c77c1a4b2175b66845ab7320f68f57d199f9ba9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Mon, 14 Apr 2025 23:05:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:06:00 GMT
ENV MONGO_VERSION=6.0.22
# Mon, 14 Apr 2025 23:06:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Mon, 14 Apr 2025 23:06:03 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Mon, 14 Apr 2025 23:07:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:07:19 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:07:21 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:07:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1953279dd1283d563aa9afe5fea8bd9419bcb80bd4a103bf9e47b8dc000bb0ea`  
		Last Modified: Mon, 14 Apr 2025 23:07:29 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1684eb05e1f04b5726b271d3037dcdcc0116cabd1282509d4a377b5b3b9a7666`  
		Last Modified: Mon, 14 Apr 2025 23:07:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94e365b354c7b42eb554a0352943b9418f1dddad574ae64ee42b6d3e28bc74df`  
		Last Modified: Mon, 14 Apr 2025 23:07:29 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78246fcc5f4ec23f7f5832781cd926665885c61c446762e5c55d1c13d5930c1e`  
		Last Modified: Mon, 14 Apr 2025 23:07:27 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd40a7b6db988e9a63a89839a083be75e65aebf66b18149e0d187552e763cb91`  
		Last Modified: Mon, 14 Apr 2025 23:08:19 GMT  
		Size: 527.0 MB (526982345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d6312a5a7520a7cb017078eea48f97751ae30aa8e8453a4a149a772480054b4`  
		Last Modified: Mon, 14 Apr 2025 23:07:27 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb60207c6b0373e454c0b216a7853ac2fb4aa9fd2288b4d4a39ccf3276674b3a`  
		Last Modified: Mon, 14 Apr 2025 23:07:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a3be16c5a209fa75ba21e5f2a3b4354048978ca335ac45097bc7939be730ff`  
		Last Modified: Mon, 14 Apr 2025 23:07:27 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull mongo@sha256:dafbb8462ce44e6e134bdffe2c9822a23a3c5cbe26afb5e5493d9f94becea925
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2797955597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f09d5b438899609aeb011c93702ac29a5098a4a8a686b02e8c9038ad1f9c2af`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Mon, 14 Apr 2025 23:10:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:10:40 GMT
ENV MONGO_VERSION=6.0.22
# Mon, 14 Apr 2025 23:10:41 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Mon, 14 Apr 2025 23:10:42 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Mon, 14 Apr 2025 23:11:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:11:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:11:43 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:11:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f702fc94dc524ce8daf5f1bd3d3c718f9ef2196e155d111c8d515aeb5863120b`  
		Last Modified: Mon, 14 Apr 2025 23:11:47 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85c2b1634ebc569be146d9d0b54c43e902f5b1a9ae6ea3f5d88b9956ae91c80`  
		Last Modified: Mon, 14 Apr 2025 23:11:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d9e37c94646e2347efefb1460e4db716c346521f5799b0ef0d894b140047a0`  
		Last Modified: Mon, 14 Apr 2025 23:11:47 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d439ae5ac7369da2dffd785e40fac2c0122bd4d812695dac43565ce3ff4f5`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5f9b3abb5d7478407beb7956cba27263d8aee5c5758d5796878c90f538542d`  
		Last Modified: Mon, 14 Apr 2025 23:12:32 GMT  
		Size: 527.0 MB (526950961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8946c87fdcae33a21864535dbf4f7d8af599023727e495862784e7908b5270c5`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c97b443d3f44ce66012a9d4f53b26014c4d6975982595a248409ea469b9702`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d91f99ec53560cf1377c811799e6dba5360519e9734b185a96a1b74af9b09805`  
		Last Modified: Mon, 14 Apr 2025 23:11:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull mongo@sha256:bbf40cbc11a22b1e650b3dbf694da86a4c23e1eeab01a4c6d28d4cc1b6fee61b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2689684524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7808ff17c1477d094f8abdb9abaf2354170bbe791ed27898c6b74a4553c09dcd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Mon, 14 Apr 2025 23:07:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:07:12 GMT
ENV MONGO_VERSION=6.0.22
# Mon, 14 Apr 2025 23:07:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.22-signed.msi
# Mon, 14 Apr 2025 23:07:14 GMT
ENV MONGO_DOWNLOAD_SHA256=8d15563eae81fe7ec7530ab84cb04a9f7af16391dffbaa27d02ae9937b7e9c3c
# Mon, 14 Apr 2025 23:08:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:08:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:08:52 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:08:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a094a3c992e9c6f7aaab4af3fbff834fc69dfdf6d9947e02b56d77549ce8fb3b`  
		Last Modified: Mon, 14 Apr 2025 23:08:58 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce256afbc1123ea5d93b5e56c4a179f2daf90a5dbb4d7a206bbeb5108448b02`  
		Last Modified: Mon, 14 Apr 2025 23:08:58 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad437bfbeec11bd61917cd0fb6ba421f16e176ed41e588ec33481b7294528e28`  
		Last Modified: Mon, 14 Apr 2025 23:08:58 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57bd6f9ab65be169a380617d133f4dadbd3602f0abf43a803b8b67f7c4aca60c`  
		Last Modified: Mon, 14 Apr 2025 23:08:57 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444c05bdd2e52c148df6138b83e7a931d44ec24820e06c3d762fe100e585a02a`  
		Last Modified: Mon, 14 Apr 2025 23:09:44 GMT  
		Size: 526.9 MB (526949588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41674482e903f6b01b14f72ba33d6622052a9af69a975e59a16d416e7e7397dc`  
		Last Modified: Mon, 14 Apr 2025 23:08:57 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d5ce4c3ca4066592a998946926b59af281979ba14eca197bc1273714588eb2`  
		Last Modified: Mon, 14 Apr 2025 23:08:57 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:097e150fbe9a25cdc8d1d4e4df4b181c0e1a1a9cfe7c4975ea330f62a2e6e7da`  
		Last Modified: Mon, 14 Apr 2025 23:08:57 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
