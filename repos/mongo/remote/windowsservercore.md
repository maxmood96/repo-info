## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:909e2c083cca30481944e3f033c2438cea2c227f3cedfb7882b9911d4922af88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.887; amd64
	-	windows version 10.0.17763.3287; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.887; amd64

```console
$ docker pull mongo@sha256:18540a4bbf163408c1a0ce7b9fc97f751e66eaefba1893494521e984273fd3f7
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2626462646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:885f7fb51b5b1b8a9d989e84a400a07aeaa153b2b5458ab17acea017d018eec1`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 13:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 20 Aug 2022 01:16:14 GMT
ENV MONGO_VERSION=5.0.11
# Sat, 20 Aug 2022 01:16:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.11-signed.msi
# Sat, 20 Aug 2022 01:16:16 GMT
ENV MONGO_DOWNLOAD_SHA256=c13f071b45dce322f2d6e6a7f569d1dbebbb8d9baa62f5f1bee8efd4479b7861
# Sat, 20 Aug 2022 01:17:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 20 Aug 2022 01:17:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 20 Aug 2022 01:17:49 GMT
EXPOSE 27017
# Sat, 20 Aug 2022 01:17:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ff9b89cbdb5f88cb926263140643eb2bfad61fb092119830e290c8f8ff711c8f`  
		Last Modified: Wed, 10 Aug 2022 15:05:31 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e676e5bd1bcbd6eed0ddb75e36e46366aa20702718f144032c5bf07a7849a80`  
		Last Modified: Sat, 20 Aug 2022 01:38:02 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91924f603c1693ceec6b555fb3a502126ba1c7cb5c0094a92643e6cf403d81ff`  
		Last Modified: Sat, 20 Aug 2022 01:38:01 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:460e427e3aa14c11009a679937a91159ea89577f3768438bd897c363557926bc`  
		Last Modified: Sat, 20 Aug 2022 01:37:59 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d04926a8089570105de77c448c51f6911ef4006a10e9ebbc80138fbb608f4df`  
		Last Modified: Sat, 20 Aug 2022 01:38:58 GMT  
		Size: 309.6 MB (309563650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a6abc9e37aa18e7231018a30c98cd5b61ae953ffeef7f46c24aeb9a6e1dde7`  
		Last Modified: Sat, 20 Aug 2022 01:37:59 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ada324012adbf8c624989b22df43ddc00e7f2ee0951d8b8e9ca0b805192fb85`  
		Last Modified: Sat, 20 Aug 2022 01:37:59 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab580bcc488c2191310d5fef44f4cd6d2b6052777822a16144dfc31eee8703fc`  
		Last Modified: Sat, 20 Aug 2022 01:37:59 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:dbb9182ed7c52bd3e9e4fa6d520f03c8f1a4af76ecba4e95f5ed5dc6c52df905
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2987044349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b4049e2da0c1a94bcddfdb91d926e9e1f21060524e70f619a5400f97cb9ad4a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 20 Aug 2022 01:17:58 GMT
ENV MONGO_VERSION=5.0.11
# Sat, 20 Aug 2022 01:17:58 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.11-signed.msi
# Sat, 20 Aug 2022 01:17:59 GMT
ENV MONGO_DOWNLOAD_SHA256=c13f071b45dce322f2d6e6a7f569d1dbebbb8d9baa62f5f1bee8efd4479b7861
# Sat, 20 Aug 2022 01:20:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 20 Aug 2022 01:20:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 20 Aug 2022 01:20:24 GMT
EXPOSE 27017
# Sat, 20 Aug 2022 01:20:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f4ce4df21f88690194f34ba04f6a20c77dcb9ee4e860c6668e85090b7faa630`  
		Last Modified: Sat, 20 Aug 2022 01:39:15 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef55c9abe93febc4904717abb4bcfbdfd6978020723b694457f4c69532b2e87`  
		Last Modified: Sat, 20 Aug 2022 01:39:14 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6890d5b856229ee99d06de1b34a1100bc9c3265cbc2bc8d4e2be1745a6e966f`  
		Last Modified: Sat, 20 Aug 2022 01:39:12 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa24bb649e96e75d1fe4354f9ace262248c9457c04449e610c4e862db91ac70`  
		Last Modified: Sat, 20 Aug 2022 01:40:12 GMT  
		Size: 309.3 MB (309321651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be19cae07d7399f9599d9d7d022c98a7ab10c6f22eb454742a4a1e81b7671df7`  
		Last Modified: Sat, 20 Aug 2022 01:39:12 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f660e251a44d76b683c5dd397956820d1d6225c31da2de8f733c15ce8604d4`  
		Last Modified: Sat, 20 Aug 2022 01:39:13 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5897e75510c055d7c0999a5953522a9a01d8e1eb42437ef779123e7bb0bd5ef`  
		Last Modified: Sat, 20 Aug 2022 01:39:12 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
