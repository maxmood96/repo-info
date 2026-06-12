## `mongo:7-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:c17de65a08a511d88c50c387ff8430daaf528fdcc362d813a6e7c55316c9e768
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `mongo:7-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull mongo@sha256:2a2ab6dd46a8eebb2895da89a0a6dba6e5132c2420eda555b33226e09d2766fd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2902994151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c833fc4a2ffe5c15fa1441191efbda806bc08579b0a341298ccfc949e387768`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 12 Jun 2026 19:14:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 12 Jun 2026 19:14:33 GMT
ENV MONGO_VERSION=7.0.37
# Fri, 12 Jun 2026 19:14:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.37-signed.msi
# Fri, 12 Jun 2026 19:14:36 GMT
ENV MONGO_DOWNLOAD_SHA256=110a4774e93dd3dd253725f18bc87b77468521875d7448ca5f79fb1d5045cedc
# Fri, 12 Jun 2026 19:16:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 12 Jun 2026 19:17:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 12 Jun 2026 19:17:01 GMT
EXPOSE 27017
# Fri, 12 Jun 2026 19:17:02 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebbdfcf85d8f881db133bd5455f1a7e0332c4f35d9eded01268ed34d9c8393a`  
		Last Modified: Fri, 12 Jun 2026 19:17:08 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d0013d156d83b3d20d42f3db0f68c7c003037ee96457602e409fc760fa0721`  
		Last Modified: Fri, 12 Jun 2026 19:17:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e06e0ee86ec37503073a9fbd12d32eacc908c3c11e1d5ad49f9938ed50deb2e`  
		Last Modified: Fri, 12 Jun 2026 19:17:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0093f9b7695ebedc27123f0b235ed3f5b63d46a6dec785e96539a649dac02562`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82ce48c312ba0bce59e76d997616e69be954527c444159c080d7ed037e41ff2f`  
		Last Modified: Fri, 12 Jun 2026 19:18:02 GMT  
		Size: 623.8 MB (623842059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea2a143fa3def0432fb11d53e74033d6e3c5b67ee9519e6b83e76f54ec54adf`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e1ddad0f55447ffb460e0fd19e7111d65907ab23e50eda42b076915cb07113`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31dc0337ed531ad7a46b9d83177c1886270f8c502041ffc5beb3b886d1e56047`  
		Last Modified: Fri, 12 Jun 2026 19:17:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
