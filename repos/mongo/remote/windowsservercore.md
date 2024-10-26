## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:2b759d0f5cbf7938f7a635bbd1d8c9fa97db61d21cb1739ddcf5d3cbdaca4c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:06472eb9afce60b19596150621e877a47eb0667110b99f2e8977f49ac0542ccd
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2568049456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98efadaec49409b1d2089fd87677cf77990556f795ce1ec2000f3bd9c8fad0ef`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Fri, 25 Oct 2024 23:57:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Oct 2024 23:57:12 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 23:57:13 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.3-signed.msi
# Fri, 25 Oct 2024 23:57:13 GMT
ENV MONGO_DOWNLOAD_SHA256=f064b0d5096136a70edd9a4a1c17d23c78f62600ba860512523eee2206a018b9
# Fri, 25 Oct 2024 23:59:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 25 Oct 2024 23:59:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 25 Oct 2024 23:59:49 GMT
EXPOSE 27017
# Fri, 25 Oct 2024 23:59:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1199f3a042eeaf1554bf78a1a3b3e30ec6a6ba8371772feb2bd5552de7c4c09`  
		Last Modified: Fri, 25 Oct 2024 23:59:53 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c58624da82b4c32ac0f2aa179f66eba0f192c1b7c5124d5cd5a7ed4c08a03a04`  
		Last Modified: Fri, 25 Oct 2024 23:59:53 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e612f83dec9fa8bd61af3574a8e8aad95bdbbdf2e60c83227042fa6ecc8d1d`  
		Last Modified: Fri, 25 Oct 2024 23:59:53 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d4a723b0e20fa35f7e27b895d4ec554e1cc3b995f44b1b7b224c7e3764f28e5`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598057ebd54e7d5789d7dab0c9c5d1a3481c0fa793550b5388ce1e45e6df1842`  
		Last Modified: Sat, 26 Oct 2024 00:00:51 GMT  
		Size: 768.7 MB (768698892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6538712d000ab89cfd995663aca54e24fe6b611a6d74ab61ed812eb91a7d09ca`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e4bf14a2a6ab78e4f0895573f09cd741cbcd535978e0c56a2b5ec2c9f0ab652`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e79b0f655ce9b9961df283430428b764c3e76f44a14c7e2210e324ccbf2f54`  
		Last Modified: Fri, 25 Oct 2024 23:59:52 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull mongo@sha256:52a770a60dc2fe6710864c8d3f907b102eea04090994298b786a93318d43d313
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2670541584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f3bbc6251375d6e0e8bfc9567c3b1633afab0ce259dee23e4c5ba111378d75`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Fri, 25 Oct 2024 23:57:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 25 Oct 2024 23:57:10 GMT
ENV MONGO_VERSION=8.0.3
# Fri, 25 Oct 2024 23:57:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.3-signed.msi
# Fri, 25 Oct 2024 23:57:11 GMT
ENV MONGO_DOWNLOAD_SHA256=f064b0d5096136a70edd9a4a1c17d23c78f62600ba860512523eee2206a018b9
# Fri, 25 Oct 2024 23:59:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 25 Oct 2024 23:59:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 25 Oct 2024 23:59:57 GMT
EXPOSE 27017
# Fri, 25 Oct 2024 23:59:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c93e022fd5b1459e2a0287132848ce0766c424dd1e488d7bbc93fb1fc98ade`  
		Last Modified: Sat, 26 Oct 2024 00:00:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d4e9c0880ba7f6fa2ba82ff317a53b7587d82aac46dba86c24b21784427a8d`  
		Last Modified: Sat, 26 Oct 2024 00:00:03 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9504ea41fe8eb79a354a741e534bb5d13a77c7289f196073039fd6931ee17455`  
		Last Modified: Sat, 26 Oct 2024 00:00:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b52bce99ca5ac3c9c4e430f8f9fda368da15464908ed9da4a6ba975deb58ad`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192c9faefcffc6b2fac10996e6a79eb51ffac2e966da72d1c76e426de879b2eb`  
		Last Modified: Sat, 26 Oct 2024 00:01:00 GMT  
		Size: 768.7 MB (768707186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29126f60832e4ef19432321239aedbe553944a85ef71311c216070ae9375b9a2`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b274bcbd39a27a8f3e7bd19451a9bed7744bbcc8dc2c19da6318283a654f8a9`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0f0b5c1b45d6b7b79cb03b2b30b9b22c83c29fdeb3a9e118bea0dac73ed98d`  
		Last Modified: Sat, 26 Oct 2024 00:00:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
