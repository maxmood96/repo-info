## `mongo:windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:793f277af77467fbb477fdc7599150cccba0ea4c9d5d73790adeb4755737ff60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `mongo:windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull mongo@sha256:156d32d6e5d6c4e258367c0547300e586181383fd7ce44df5d301ad72926357d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 GB (4165014464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3dd7f6d282fc634f83b507a56dd2b5c2380b7034a0d3539a3e88673d27ee195`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Mon, 14 Apr 2025 23:04:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 14 Apr 2025 23:04:27 GMT
ENV MONGO_VERSION=8.0.8
# Mon, 14 Apr 2025 23:04:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.8-signed.msi
# Mon, 14 Apr 2025 23:04:30 GMT
ENV MONGO_DOWNLOAD_SHA256=4bf700912876c337697fa02bf4c38db0baed89604033b138e5e27d4e3eb743ee
# Mon, 14 Apr 2025 23:06:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 14 Apr 2025 23:06:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 14 Apr 2025 23:06:04 GMT
EXPOSE 27017
# Mon, 14 Apr 2025 23:06:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82028042ef11bde09d30dfc8e76c04bb0549ef5343f040d0f35211f18c922f16`  
		Last Modified: Mon, 14 Apr 2025 23:06:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43868b7b7ed83ddd09a90df0280281b5acc55b6b00ed9f7678e2287cd4517565`  
		Last Modified: Mon, 14 Apr 2025 23:06:09 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b82926b66a6b878b37c07f222b6117186b25e64dbd4e3f75a0679164c2e23a`  
		Last Modified: Mon, 14 Apr 2025 23:06:09 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8fc0295e5d9dc3c8a7da88556d324f0cb4f141f64421abb63ad66d07a3b461`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5681951b04cc47982ae75d3bd6e4182235b9fd2c8982bf0eb7cf46104a964f`  
		Last Modified: Mon, 14 Apr 2025 23:07:21 GMT  
		Size: 770.3 MB (770325704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7bc91a9e00753d2ec07332142a5e238e2b2a96e2e6abc6fbe0a7cc215577e34`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a9ec1eac9d9c10aba98576cffdde6a77c63dac0dded08194c5355075a58aae`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5be0fa93a35a40def8901bc87cb62976e71f71d800ea8a7b9b1e98eba5ef26`  
		Last Modified: Mon, 14 Apr 2025 23:06:08 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
