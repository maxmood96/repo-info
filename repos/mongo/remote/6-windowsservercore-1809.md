## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:2aecfb5ffe0960379a0b7ab83f60bdc40767f64dc2ac5263d7fe5a560d29b61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:b48782dcf773e7422affb88bb99c32c361dc6ae6850804f84553df1b5cf94a69
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2744980083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8b1ff88d0ec684f9949e578903d20b496f3d5646ac9066dab8ddc8504ebfa27`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 28 Jun 2024 23:55:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 28 Jun 2024 23:55:19 GMT
ENV MONGO_VERSION=6.0.16
# Fri, 28 Jun 2024 23:55:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.16-signed.msi
# Fri, 28 Jun 2024 23:55:21 GMT
ENV MONGO_DOWNLOAD_SHA256=4a0da9d2a8e7151a2c7c8e68406dce00336f2bb2f6b9f1129184c9888c59e032
# Fri, 28 Jun 2024 23:57:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 28 Jun 2024 23:57:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 28 Jun 2024 23:57:49 GMT
EXPOSE 27017
# Fri, 28 Jun 2024 23:57:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0e066bf82ce04d0c32e9aa7617cf7b886dfb8231742343f2fa062f499ad7cd7`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f55510d5e79457d793662a9a32a0d44182b203127eb2a3c4fabe85b3d735483`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36d13212f2041e32ae4309d971c6f594762039e66798a0a2cfb28c170017abea`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ea8da32548365a3a02fab9927d5f756955ead2f15e2b35b2fabe40049250`  
		Last Modified: Fri, 28 Jun 2024 23:57:54 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8adceb7bae7fba3af7c96e4d4aa9d666e5ea54d215aa8ef8b2d2aa86e7a9b0`  
		Last Modified: Fri, 28 Jun 2024 23:58:34 GMT  
		Size: 524.3 MB (524289774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271757798b0ee553c6d17ce406f3e0619f486c1a81377d5299900d6030a51651`  
		Last Modified: Fri, 28 Jun 2024 23:57:54 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50042b2e2be865c25fca654dcbc3a915a80a8f03958670b1e5ac39963c39cd15`  
		Last Modified: Fri, 28 Jun 2024 23:57:54 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3fc4dc625bd3d2c7b35e4b5a0ab679d1405f71d6d4a8be20f3c899e2d759af`  
		Last Modified: Fri, 28 Jun 2024 23:57:54 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
