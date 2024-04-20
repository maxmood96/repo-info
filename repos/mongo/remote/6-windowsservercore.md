## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:5c1aa17328e14c4cc6d5cddf3bc87dd18377fd1d0b7566ca7c095b5ad933248f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `mongo:6-windowsservercore` - windows version 10.0.20348.2402; amd64

```console
$ docker pull mongo@sha256:b1803ded42268f20ea84c74141322ec71256e161c1570431c5842c821b29c039
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2516938180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91288d5eb504968b3b3ab17968f5169929de4f839939bdb8af67506fcc43a8ce`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Thu, 18 Apr 2024 17:49:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 18 Apr 2024 17:49:46 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 17:49:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.15-signed.msi
# Thu, 18 Apr 2024 17:49:47 GMT
ENV MONGO_DOWNLOAD_SHA256=a59408edea70438c1c9793ecdbc8b2111e44f10dd90f1ed0d2cc8071ae1cc95f
# Thu, 18 Apr 2024 17:52:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 18 Apr 2024 17:52:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 18 Apr 2024 17:52:03 GMT
EXPOSE 27017
# Thu, 18 Apr 2024 17:52:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53db21a499ba275bd8666eaaedcd077bb7b89b5ac9e3a54bc61f16724dcd7a33`  
		Last Modified: Thu, 18 Apr 2024 17:52:10 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35272f28a0078eff5bc9b31a7e297e2fe833e3b04dd32b705341ceddcae096e4`  
		Last Modified: Thu, 18 Apr 2024 17:52:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3922cddd153f1b3862a01a4005cbf8189727e86422ecc63563e339d4bbfd9b32`  
		Last Modified: Thu, 18 Apr 2024 17:52:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5bbee6242caeb1f0e7a3edbdf6b9a29b8b850980bfc92cc4226b8c53a5f69a`  
		Last Modified: Thu, 18 Apr 2024 17:52:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50f12e0addc3ee508923e5cdc8f23974d9fa82f616d399741863b3adb569d4b5`  
		Last Modified: Thu, 18 Apr 2024 17:52:48 GMT  
		Size: 517.6 MB (517555475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3869c6a8792243161efd562fdc214073e7d68a8b4a0dc7433f9672349b9835d7`  
		Last Modified: Thu, 18 Apr 2024 17:52:08 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf9a3c00afe61eb912c02770a630ac1d2dccf700994acea5536b45102eccb25d`  
		Last Modified: Thu, 18 Apr 2024 17:52:08 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f4cb6e0fb1d55cc756baefa9d2756cd8a6c3ec215194b3be8902334a782b688`  
		Last Modified: Thu, 18 Apr 2024 17:52:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.5696; amd64

```console
$ docker pull mongo@sha256:2f8a42cceb60461b137aec7a3fe8feb55dca31482e56276b967707f6105a0f43
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2681998486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bec9ec9e7f8a5eb61fe7c52f633707fecc663333a9d4cf1d1ab5e8d4a994efd8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Thu, 18 Apr 2024 17:49:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 18 Apr 2024 17:49:46 GMT
ENV MONGO_VERSION=6.0.15
# Thu, 18 Apr 2024 17:49:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.15-signed.msi
# Thu, 18 Apr 2024 17:49:47 GMT
ENV MONGO_DOWNLOAD_SHA256=a59408edea70438c1c9793ecdbc8b2111e44f10dd90f1ed0d2cc8071ae1cc95f
# Thu, 18 Apr 2024 17:52:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 18 Apr 2024 17:52:28 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 18 Apr 2024 17:52:29 GMT
EXPOSE 27017
# Thu, 18 Apr 2024 17:52:30 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f2092c2b38eebe48f177a5a543e46c76f762c6d457dc261a01635242c7ea4f`  
		Last Modified: Thu, 18 Apr 2024 17:52:37 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a4b365c72040f84286d837493cb45e2ce71ddfb324da2979532bd3fe8e942e`  
		Last Modified: Thu, 18 Apr 2024 17:52:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a58688282cfe9b6dfc33977256f1ed19d2b2466df135fbecc4ff5e7789680c4`  
		Last Modified: Thu, 18 Apr 2024 17:52:37 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d784ba81301d4650baf6048c4bd3cc32e5ab3e126e0b270dbf92800101129a2b`  
		Last Modified: Thu, 18 Apr 2024 17:52:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74346ecb6fecc82c0e26c8613be11a22f8afde0da3669c86ffd7788d6eeeb3c`  
		Last Modified: Thu, 18 Apr 2024 17:53:16 GMT  
		Size: 517.6 MB (517561454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61dab34e31ee051f34886aecc55217ead3fd28af918703b3d2177c8b0bdb8611`  
		Last Modified: Thu, 18 Apr 2024 17:52:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5cd43b8e844261a623d3aae88cd8512142848f12c0667eb6dc9e895dd5e663`  
		Last Modified: Thu, 18 Apr 2024 17:52:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d9e21cd63e858325dd1035b5840c3bb89e0df6b01ce512476a9a48be225ed4`  
		Last Modified: Thu, 18 Apr 2024 17:52:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
