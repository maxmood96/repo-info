## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:eae00fc6b73cba792ee9bf8b4315eedb17070a7941fb02debef6c29ba12e4d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `mongo:windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull mongo@sha256:90c9a7017b5102feb1bf835248392138066ee12130b92972f979c68e3cbd6f86
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2525662735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d139759e1a611e948925f243f24aecdcc24732fdb1fe9ab8705eee656d600ef`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 01 Mar 2024 00:49:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 01 Mar 2024 00:49:35 GMT
ENV MONGO_VERSION=7.0.6
# Fri, 01 Mar 2024 00:49:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.6-signed.msi
# Fri, 01 Mar 2024 00:49:36 GMT
ENV MONGO_DOWNLOAD_SHA256=29fb23ca36a9dd6fee2f6491a92392c404d544ffe38bfaf3d2467db0bd774fde
# Fri, 01 Mar 2024 00:51:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 01 Mar 2024 00:51:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 00:51:47 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 00:51:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d2a8bf51790a318a0f95e76feead20b23bc7b7fd70ecf77dc4014df5dfd7ec1`  
		Last Modified: Fri, 01 Mar 2024 00:51:54 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d66bcc3ebf61224a2756acf0f40b2a58995ebc7bbb6db8e7ba8d5119e6cb46e`  
		Last Modified: Fri, 01 Mar 2024 00:51:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303acd4dedfa5ea1d95ea93880418e948e801d1438f038bcbf8b20c07539e1ce`  
		Last Modified: Fri, 01 Mar 2024 00:51:53 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3412634cb3241ebb134bc78d795f38f43fc538a33d04b943fcb0a8d141f989cf`  
		Last Modified: Fri, 01 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01c55462c8660f56e95d01849a3b2f4c225f2f62c955ac7ed301761888b9933`  
		Last Modified: Fri, 01 Mar 2024 00:52:41 GMT  
		Size: 615.0 MB (614999526 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dae8b165520a0325df2e45416e18345dc55b4181b45d21566ee97efeba4d372`  
		Last Modified: Fri, 01 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7929a56ab2bb5fdec361076f15a2bf033e656e43a999770f253ac32758b222d6`  
		Last Modified: Fri, 01 Mar 2024 00:51:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecc6333e415594c9b702d794a8eb6af2fc6bbacd08123deb2591b316c0fc0e88`  
		Last Modified: Fri, 01 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:dae3592a118b917f2c8aeb6000c7e612d6be788ac091e674f7e431d1ef4d33de
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2695545113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9023c9ea0727a3949f1db36609c3af2c8d60d850a63ad4fe91ce590cce35a0ad`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Fri, 01 Mar 2024 00:49:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 01 Mar 2024 00:49:39 GMT
ENV MONGO_VERSION=7.0.6
# Fri, 01 Mar 2024 00:49:40 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.6-signed.msi
# Fri, 01 Mar 2024 00:49:41 GMT
ENV MONGO_DOWNLOAD_SHA256=29fb23ca36a9dd6fee2f6491a92392c404d544ffe38bfaf3d2467db0bd774fde
# Fri, 01 Mar 2024 00:53:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 01 Mar 2024 00:53:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 00:53:31 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 00:53:32 GMT
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
	-	`sha256:80378cf80c679d3cbfd5c1d83c73695789b70779cf470aab553f980b6a6fbd5f`  
		Last Modified: Fri, 01 Mar 2024 00:53:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:469eae7e6b0b07c952d654b538a405e4942f9a10b35b0f88d61ad7953401bbf4`  
		Last Modified: Fri, 01 Mar 2024 00:53:36 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b174a244dc2f30394270615bb1f3ca07d63a7c0ebbbd3b0cffe9b5263769775`  
		Last Modified: Fri, 01 Mar 2024 00:53:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade464e94a28b7eae1c912fede48228526e8d8a8aff2faa9e6d0bff4780ae5a1`  
		Last Modified: Fri, 01 Mar 2024 00:53:35 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:991049959e202825c691d981517ce0a6a5deb72e6cce9781c3b498cba77184cc`  
		Last Modified: Fri, 01 Mar 2024 00:54:22 GMT  
		Size: 615.1 MB (615087286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5784400d3ba345440d98245b70df09061b44e6fa60181a188c303170fd440249`  
		Last Modified: Fri, 01 Mar 2024 00:53:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b97aa5faf64dfd52b6c4d495bfc9f46df63600ecc43424b71dcee8134817ff`  
		Last Modified: Fri, 01 Mar 2024 00:53:35 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d7cfb124b9af890285a2c41270d43bc220e443e8ad588f25a68ba0cde299bac`  
		Last Modified: Fri, 01 Mar 2024 00:53:35 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
