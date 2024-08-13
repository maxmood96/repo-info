## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:965ad7d5822edb2f47b52a8fdefee13f0f92613a9911da56420d422c049257f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:09f7458917dfa6cb05f39ad6630fb8a1c7c9f3e1a8d3bd400e629db35adf9266
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2750562909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:312a825e0fc0adc403a982ef1763ccc2fec51df69d2a46179ca61d180cdac5c3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:15:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:15:02 GMT
ENV MONGO_VERSION=7.0.12
# Tue, 13 Aug 2024 20:15:03 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.12-signed.msi
# Tue, 13 Aug 2024 20:15:04 GMT
ENV MONGO_DOWNLOAD_SHA256=314f1b988490d46c9831cbf7ad7669a949507df17cc0674f7bdac47de74281b1
# Tue, 13 Aug 2024 20:16:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:16:23 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 20:16:24 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 20:16:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304371999569501d22285076d583445ae9a71dbc9bbc8794422c2172c0f4c730`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef456b8e36791a63aebfd02aa1457364b236b1e2d2ee28217313ef896cfe0fd`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9a1faaf446fba34c83978864b5b7d75a38c16fbfdd6843bb2b84eabdd57c842`  
		Last Modified: Tue, 13 Aug 2024 20:16:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9a13aa819105bd796037c014ef879e4bcd9dd5c8d3824b8a2250c14dc5818a2`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffee34de017a49064632da5d7e1030bfc31a5105652f49a2ee08474a7f5960f`  
		Last Modified: Tue, 13 Aug 2024 20:17:19 GMT  
		Size: 608.8 MB (608788900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddbae91ab071def197c99a0c9b02d0b1e796e34cc04132d24c6d91d8b7cd3c0`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42165731c8550589c978e9d836425f3d687ae47963aa87ce4541efa9d5d993b0`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4299b8be79063f08fb975a723b9b4ec3315a2ea1ccd398081fbf8462cb5c816e`  
		Last Modified: Tue, 13 Aug 2024 20:16:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
