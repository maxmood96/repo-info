## `mongo:7-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:a6bcc77b43f862e5abcd84be85bfe5d7ce170735ad77486f5b4bf7a46e5dd50f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `mongo:7-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull mongo@sha256:6731b3477d6a4e5e770de4c593b6e579ae7fbdeb42dbeeb3a3083ec2e8c2a82d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2700829448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d17ba4a65ad06060476e7a7e2c214fca3b11dca9db93133b9482c36e11d7e405`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 22:05:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:08:12 GMT
ENV MONGO_VERSION=7.0.30
# Tue, 10 Mar 2026 22:08:12 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.30-signed.msi
# Tue, 10 Mar 2026 22:08:13 GMT
ENV MONGO_DOWNLOAD_SHA256=bfdcc24c27082a220867a139aad04d734eead0f85e8caacef135bb2a4810f9cd
# Tue, 10 Mar 2026 22:09:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:09:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Mar 2026 22:09:45 GMT
EXPOSE 27017
# Tue, 10 Mar 2026 22:09:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07c5c01027f6cd13916d665e90362fe31d3eed5e697254cf94258157c11218bb`  
		Last Modified: Tue, 10 Mar 2026 22:07:57 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6f6ec360d30c9055b63aab36f7fc6f6018989d6c8b1ec2f0f024d1d4906a30`  
		Last Modified: Tue, 10 Mar 2026 22:10:02 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e28e3cf19ed1b18de780562a470bcfed181bc728f9a69cdef5158756af4d854`  
		Last Modified: Tue, 10 Mar 2026 22:10:02 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a4802799f394e13ed50f317bad7602e07b8c97efe6afc0a34f310043f6b61d`  
		Last Modified: Tue, 10 Mar 2026 22:10:01 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175b2af0ac61be01f5db50cae9ddf55097511e2461cf8b621a68fc0730244ebb`  
		Last Modified: Tue, 10 Mar 2026 22:10:58 GMT  
		Size: 619.6 MB (619624279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0be65e08fcdea1555abdee1ec0b50d87689992650af6db3aad335dec1e448f6a`  
		Last Modified: Tue, 10 Mar 2026 22:10:01 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e780a5085e64b80091ccd0ebb620b81966c5d2202be69701c95add41debd08e2`  
		Last Modified: Tue, 10 Mar 2026 22:10:01 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4e8d005b7e80dea93493a0283d89284473b3c723a1d6e804f47a654bb93db0`  
		Last Modified: Tue, 10 Mar 2026 22:10:01 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
