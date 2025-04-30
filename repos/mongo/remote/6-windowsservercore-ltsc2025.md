## `mongo:6-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:453200072f9f85bcd041dee98dd820cb2e2f640df51e9e19d3251b90c16e749e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `mongo:6-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull mongo@sha256:999b05d3c17999a78b7e7fe21fc3498bc6a8bd24f480429ca60ac59dadf59595
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.9 GB (3922218248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54101b28a3bbe293c32f181c239dabea51784ec82a2eda60c140c6547b7c720d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 30 Apr 2025 17:31:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 30 Apr 2025 17:31:09 GMT
ENV MONGO_VERSION=6.0.23
# Wed, 30 Apr 2025 17:31:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.23-signed.msi
# Wed, 30 Apr 2025 17:31:14 GMT
ENV MONGO_DOWNLOAD_SHA256=805c9b5d6828a8b015e2be2028dca5587437038a17a345d0dfd06537ec1c3f40
# Wed, 30 Apr 2025 17:32:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 30 Apr 2025 17:32:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 30 Apr 2025 17:32:32 GMT
EXPOSE 27017
# Wed, 30 Apr 2025 17:32:33 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af39b4fd5a91c7cdd6d987661cf5e5369cb6f37d9cc7b38e3fd69601f732d267`  
		Last Modified: Wed, 30 Apr 2025 17:32:37 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916fefd238f9a9c797803265d1fa76d62f92c585221e3bd686e9ffacca6ed09d`  
		Last Modified: Wed, 30 Apr 2025 17:32:37 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e49327a070dbb8c94ea0091329f6ec7ed83b6f4153a12607c453fb6e5f3daf7`  
		Last Modified: Wed, 30 Apr 2025 17:32:37 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef7eb2f1615adb9ecef6ee0c60065c992f3178dc882a74d37f2ad241d0c30ff2`  
		Last Modified: Wed, 30 Apr 2025 17:32:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659ddfa82b619d94c5242571983a81ccdf0ac07a5ee3d099cca89c1f863db930`  
		Last Modified: Wed, 30 Apr 2025 17:33:28 GMT  
		Size: 527.0 MB (527047626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbacd5dec0498d54a09c13c477d50bd402096415fa3895aec379e24817fa770`  
		Last Modified: Wed, 30 Apr 2025 17:32:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb58b2edc6c40cd9b7fe27c93dfbf519c441c0e70a1dbb38abfba26efefeb73`  
		Last Modified: Wed, 30 Apr 2025 17:32:36 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0220ba25537897456a28d73caebf47d11b31011de7a0ddf9dab77ad99297f224`  
		Last Modified: Wed, 30 Apr 2025 17:32:36 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
