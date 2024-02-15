## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:b2b6d1fec5e60652df84a5540fef7978cea33d3e7ce7a806f1b33177f302df25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:9d7b734f2109c560992e8285e85b8e6c19e08dad0d050a605fba6b90f47f8be2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2693352661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc967a4e02b21b7c35af30be81781db3fa1645dffc703c72942dbec3c68bf67`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 19:59:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 19:59:24 GMT
ENV MONGO_VERSION=7.0.5
# Wed, 14 Feb 2024 19:59:24 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.5-signed.msi
# Wed, 14 Feb 2024 19:59:25 GMT
ENV MONGO_DOWNLOAD_SHA256=96441addde451b9d81dfaa10aca9678ada35d17d02a9a07481c6137d3df55e2b
# Wed, 14 Feb 2024 20:01:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:01:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Feb 2024 20:01:27 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 20:01:28 GMT
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
	-	`sha256:81933a922996d262b42c6fe75e2abda32e9ae780b8047d43cad13fb644857704`  
		Last Modified: Wed, 14 Feb 2024 20:01:34 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30769b7ee273a658ec8e53933d1a895910696351222e30e67e9603fae7f7bd3e`  
		Last Modified: Wed, 14 Feb 2024 20:01:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68dbd33c762d299e7b6817b74a985faae7ceb3a97237fd93d2416466f96330ce`  
		Last Modified: Wed, 14 Feb 2024 20:01:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3d9b35e5d3499b0e578ed21cae1774a9fec786d0fbcc0d523761e68091c82ad`  
		Last Modified: Wed, 14 Feb 2024 20:01:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ae243294025b514033905e153dcf217672a96605d77e864d2d303805ba1746`  
		Last Modified: Wed, 14 Feb 2024 20:02:24 GMT  
		Size: 612.9 MB (612894759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964773b073b58becd543c92b0aa514db866c7af3db62837c5f7a7b43389e5bf1`  
		Last Modified: Wed, 14 Feb 2024 20:01:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa2d9f49f712f9d7ee3fbbda5e25d99cb8d32448a48be3b4c8110f7c7cbae53`  
		Last Modified: Wed, 14 Feb 2024 20:01:31 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09a5c4d48a5d7497c5170f643f14c4123d273e5f4368f1015ca3c701002a7320`  
		Last Modified: Wed, 14 Feb 2024 20:01:31 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
