## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:9fc0a229597d6db3ae0c771ddb1d67853dfef3dc5988aec9c240ab55d5159f2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:fa39059e5f017c6c10a853a6fda64e0d778e0b408940afa0d50a06b9db5fe852
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2882474844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad419674ed9bbb09772811dac8de8280e10002c3a0abd10b1bf91ef85c144f0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Mon, 24 Mar 2025 21:22:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Mon, 24 Mar 2025 21:22:15 GMT
ENV MONGO_VERSION=7.0.18
# Mon, 24 Mar 2025 21:22:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.18-signed.msi
# Mon, 24 Mar 2025 21:22:16 GMT
ENV MONGO_DOWNLOAD_SHA256=ab23d0e0488dd0b9ab07bae73e481271c7574e212b4bb61b1331400a3cffb02b
# Mon, 24 Mar 2025 21:23:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Mon, 24 Mar 2025 21:23:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Mar 2025 21:23:26 GMT
EXPOSE 27017
# Mon, 24 Mar 2025 21:23:27 GMT
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
	-	`sha256:c0ed38093e05f979f562bae99f8f5fd888cd7f140de1e0137a6f904d4ecf707b`  
		Last Modified: Mon, 24 Mar 2025 21:23:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c5645aeb8ae9d4e142942cb0d02b2a9b134ffcb24bc959c6eecc553c663012`  
		Last Modified: Mon, 24 Mar 2025 21:23:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b157681df2d34907aa515c04095eddd667deeeb58a5f31f599634e8d81ae8e67`  
		Last Modified: Mon, 24 Mar 2025 21:23:33 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e07f621f45673f27424df8db9b86fc52d3d76bc7e98b0366fe647a2b86dee1d0`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff6448284b2012c009dfc958847177cd69558dac577ad743fbf6bc07619e9d`  
		Last Modified: Mon, 24 Mar 2025 21:24:21 GMT  
		Size: 612.5 MB (612524695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff51bd16c74c7da607ab0c40b01569a657c999a5ae6c9480e18ef997135b3cb1`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858b7ced5bda43382167d2744c85fd8a5686f6187f2da67276ebcb23d5140214`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024207ef982c7c0df1fe5ece519c2f7730de92a5fe1160f74c5c26343481cd15`  
		Last Modified: Mon, 24 Mar 2025 21:23:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
