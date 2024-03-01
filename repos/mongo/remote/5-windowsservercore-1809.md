## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:a03ff4e84acc349d2c4111196c37ba0531cd1088f0174fa5d016cb31ee874341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:39050f42f89ae1912d463f1015680ba16fb8bed2f3ce51ee4db7589e7635e9c4
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2396604008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97689e687d7237113148f02301c916a25c482e1365d33c307de9a4ba9e4d2670`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 01 Mar 2024 00:49:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 01 Mar 2024 00:49:34 GMT
ENV MONGO_VERSION=5.0.25
# Fri, 01 Mar 2024 00:49:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.25-signed.msi
# Fri, 01 Mar 2024 00:49:35 GMT
ENV MONGO_DOWNLOAD_SHA256=65f3fde2ddadbf61dc5895d54670bbbd6febf8b4f7c3a081d1012038452011b2
# Fri, 01 Mar 2024 00:52:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 01 Mar 2024 00:52:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 00:52:19 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 00:52:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8052457c74eb539ab97645c6ce73527f388f71b98f42c902e323b13f96e8fa24`  
		Last Modified: Fri, 01 Mar 2024 00:52:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d4dab3a561ffa4e4181b7bc840b103355180a8104b2c046306e5c67d52d4f3a`  
		Last Modified: Fri, 01 Mar 2024 00:52:27 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7469ef49c225cd9b613dc4843f560be70dd07ace3fa16054976a1b884f6c28b`  
		Last Modified: Fri, 01 Mar 2024 00:52:27 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7d7e1ac276aa0122c093b187d19301ed1505a2f4b8fa82514f3b9a0a2131ce`  
		Last Modified: Fri, 01 Mar 2024 00:52:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e579d7495db4b9dc58274c97b780559f8b571815592fe5ca798c0e4f6b8bda4e`  
		Last Modified: Fri, 01 Mar 2024 00:52:55 GMT  
		Size: 316.1 MB (316146078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933e0f139280ca180672e0721b302970208fcbe4c0156f463bcf22fbc55c3d9f`  
		Last Modified: Fri, 01 Mar 2024 00:52:25 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdf5605330ded64a4efe44552d8636c3ceef0a9fea783f5bd58e24e4b6af413`  
		Last Modified: Fri, 01 Mar 2024 00:52:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c45328b7d3e2066d7bdeffc5277580b98df4bf9f13cd0a25e3bdae1b69ea924`  
		Last Modified: Fri, 01 Mar 2024 00:52:25 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
