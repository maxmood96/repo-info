## `mongo:6-windowsservercore`

```console
$ docker pull mongo@sha256:b7caf80511f5dea19e2e46ba7d529329375372bb4eff14994f1777e733aee9b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2849; amd64
	-	windows version 10.0.17763.6532; amd64

### `mongo:6-windowsservercore` - windows version 10.0.20348.2849; amd64

```console
$ docker pull mongo@sha256:05c46c156444060d63c7d546099915f4a260b130b74f94dc15b8ca6421dcc4d6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2779228033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9edee5f0f7f325a481747e7bba135d63a05a5084874b4c26ee14f2143f8658`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:18:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:18:26 GMT
ENV MONGO_VERSION=6.0.19
# Thu, 14 Nov 2024 20:18:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.19-signed.msi
# Thu, 14 Nov 2024 20:18:27 GMT
ENV MONGO_DOWNLOAD_SHA256=2d9f5555d820c1b6a3f3177f0a73a4f9e9b3a7f1275d2aa3122a2ecc3a1b31a2
# Thu, 14 Nov 2024 20:19:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:19:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 20:19:36 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 20:19:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e26806188f079670b56e95bb08c55ec22b6a3ed9bab122f533eecbfb29e3ca0`  
		Last Modified: Thu, 14 Nov 2024 20:19:41 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b51c368deacc525a4bc46bc8ae980ade032a2c1b98531ea151d5bd9409beba`  
		Last Modified: Thu, 14 Nov 2024 20:19:41 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c307fa0161f935f4ee1ba00bb7239188b80b5181603104fd9716246d0fa0a6`  
		Last Modified: Thu, 14 Nov 2024 20:19:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3465f95a3bb4cc82ac469b47da5599f8921a7ec9ee86c75a2307f40c2b0dca60`  
		Last Modified: Thu, 14 Nov 2024 20:19:40 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3bc33c8d9bc1167d29cd02ac49fef3e5a5394e61bd9224246ae8e1ccde2d418`  
		Last Modified: Thu, 14 Nov 2024 20:20:23 GMT  
		Size: 526.7 MB (526734774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e475a4fdcd5c1d3a89a2ccafece51ba492cfc45c3cdc68ff6b7ec42040fb20ac`  
		Last Modified: Thu, 14 Nov 2024 20:19:40 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a028e6576aba4bb37ba006e0e452e4f4e04c65f4d555507a341a20bd9be5beb6`  
		Last Modified: Thu, 14 Nov 2024 20:19:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d980b14f3182f4140b09ff6aeb190d6404bbc8f270e2a916f05d14a571e34cf`  
		Last Modified: Thu, 14 Nov 2024 20:19:40 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:6-windowsservercore` - windows version 10.0.17763.6532; amd64

```console
$ docker pull mongo@sha256:a5acbd961b7bdba6d11fd9e03cb717224fcaa244b398aca0a432fb2cd50fee30
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2537579084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:003e7d563109cab41681dd01fe1f5d1690ff9ea3aeed93938bd2a43a22d20f64`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 14 Nov 2024 20:12:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 14 Nov 2024 20:12:31 GMT
ENV MONGO_VERSION=6.0.19
# Thu, 14 Nov 2024 20:12:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.19-signed.msi
# Thu, 14 Nov 2024 20:12:33 GMT
ENV MONGO_DOWNLOAD_SHA256=2d9f5555d820c1b6a3f3177f0a73a4f9e9b3a7f1275d2aa3122a2ecc3a1b31a2
# Thu, 14 Nov 2024 20:14:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:14:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 14 Nov 2024 20:14:48 GMT
EXPOSE 27017
# Thu, 14 Nov 2024 20:14:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50430f6a8d86c67a565ea6067b98bffce4514c78fce3f6c8c6c7a0dcb7775c6e`  
		Last Modified: Thu, 14 Nov 2024 20:14:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3729ae263fd30842e69d7fbfa3ac188ca5f54b474bd1bd8e929bd13b32ce17a`  
		Last Modified: Thu, 14 Nov 2024 20:14:52 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14de2cc4f0221d1517fa16c6534f51d96cf851bfab44bbfe88e2b6b611d2914b`  
		Last Modified: Thu, 14 Nov 2024 20:14:52 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0138c027c1de9bebdaa74e3aa1f92498a87fcc1c57bb034588621cd1456b276d`  
		Last Modified: Thu, 14 Nov 2024 20:14:51 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd3e3c33fff2b2a5a55100d7341bdafcc607b3b860be4629be7110c53a48920`  
		Last Modified: Thu, 14 Nov 2024 20:15:36 GMT  
		Size: 526.9 MB (526916127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3da14fac41a7648a2370b741166b458dc7e8422df3f7ef90799bfcd50b3621`  
		Last Modified: Thu, 14 Nov 2024 20:14:51 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d64c4b554a6f20d603af0e7ce9660a45b81841c9f136546ef320efc130296b7`  
		Last Modified: Thu, 14 Nov 2024 20:14:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2cff90b482db9972df19e802ab8f608d839e6c101eacd251cfebc168e6802c`  
		Last Modified: Thu, 14 Nov 2024 20:14:51 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
