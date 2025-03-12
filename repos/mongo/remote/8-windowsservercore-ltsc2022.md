## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:7aa1d3f7650dcf543f6dcb951d24bd315966f912725432cb52c6aaeaecbf3bfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:651cec05973d7dcb5d1c8a77d78b72af881f6110ff626609eba3adc4ad1c4ff0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3040912786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a22597d8ad42488c8dea3bc36a559c96adddd1235b7eb6429d63a5f9303569`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:57:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Mar 2025 18:57:19 GMT
ENV MONGO_VERSION=8.0.5
# Wed, 12 Mar 2025 18:57:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.5-signed.msi
# Wed, 12 Mar 2025 18:57:21 GMT
ENV MONGO_DOWNLOAD_SHA256=96b835f9cd76d4edfcdaa700c6d56aac47b1242541c05238d87c568c92db590e
# Wed, 12 Mar 2025 18:58:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:58:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 18:58:37 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 18:58:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed6fec1b72c7a8b9a20653ed52d07f80d2cbec46367070f4dcaf8fe6be4b299`  
		Last Modified: Wed, 12 Mar 2025 18:58:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bcb4c153ff0f5490c331c6ff1830b2af1fb6594d7a87b00e86552c99e39df4`  
		Last Modified: Wed, 12 Mar 2025 18:58:43 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c70b90637bafa2ee45112e83d0c8b0ee6092db2304c5abda456ae43cb436c64c`  
		Last Modified: Wed, 12 Mar 2025 18:58:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5364e60d76403098f67e8935b682f87dcabb8b88e28aa9445df9796609486f`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402034f52dd8075f4758aefcb5662043cc9c9b3beaea2f978a9ba326bbdfa1af`  
		Last Modified: Wed, 12 Mar 2025 18:59:43 GMT  
		Size: 771.0 MB (770962633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c895d11ad1e8f434e31ed666a80f0557ed2da28efea16e23412d088f986cf1`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3ea8843243f89cdc7302b1e39aa67ef10f4565568fdefdef177c5ba3304aed`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243636056b5ce394b33cdc686963ea624e388a5f7941c8f10b9813921123d03f`  
		Last Modified: Wed, 12 Mar 2025 18:58:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
