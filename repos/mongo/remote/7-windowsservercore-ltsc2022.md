## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:c09880381d1a1f936a3a432793d1e1fe65792810e87f2883e2fe90cf40b64f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull mongo@sha256:2cda3b6e306b7654282756ac6dbabdb1f29dc9ebb6d283ce98c24e5887800f7e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2876408066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576da906de91742655d63172ea99f5adca90642deb3e79ea846df5be15e9be6d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 25 Feb 2025 01:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 01:39:22 GMT
ENV MONGO_VERSION=7.0.17
# Tue, 25 Feb 2025 01:39:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.17-signed.msi
# Tue, 25 Feb 2025 01:39:23 GMT
ENV MONGO_DOWNLOAD_SHA256=4e289d657aea36ecac5fa05a5d82cd1cc377efd75f682a2126ac6473d3a22d12
# Tue, 25 Feb 2025 01:40:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 25 Feb 2025 01:40:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 25 Feb 2025 01:40:37 GMT
EXPOSE 27017
# Tue, 25 Feb 2025 01:40:38 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a05be15bc565bcd6957cdf4e2603efec2bdcf953bfe3089c475e50f7e62283`  
		Last Modified: Tue, 25 Feb 2025 01:40:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ef8849d08483f4ef60eceba83848178eb15182e4998478952f2906e8bc4a17`  
		Last Modified: Tue, 25 Feb 2025 01:40:44 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11576a158f72d03f436b1ecc649ae0d3b1df19f092f0ec189537d44c3411476`  
		Last Modified: Tue, 25 Feb 2025 01:40:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbc6f94f5b20fdec7b1d8a3a1a291dac466f7dd20ff92b8c3b5941f0a6755b0`  
		Last Modified: Tue, 25 Feb 2025 01:40:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9118da82f56baa08e8e8985b7d7687e0819f9ab9157c1426d51db6abcd8ae01`  
		Last Modified: Tue, 25 Feb 2025 01:41:32 GMT  
		Size: 612.5 MB (612540972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fca5a3304152c710a0b18e18d3eafdad4179c9b5d30ad465e1093374717a0e`  
		Last Modified: Tue, 25 Feb 2025 01:40:42 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb84db21d7e94b42ed95c6cebb4d88f30815be63568efd144ef91dcd2c263816`  
		Last Modified: Tue, 25 Feb 2025 01:40:42 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a0be9c0d42b36ce4905aec60b2088cefef416ce89b2a4c48bc90b69b6657ce5`  
		Last Modified: Tue, 25 Feb 2025 01:40:42 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
