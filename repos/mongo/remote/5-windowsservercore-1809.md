## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:f8e46b8eec350bd5548b7be5112c967c33dd1b146530608ae5a2ebcf1a313c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull mongo@sha256:f7235eb5c3bf9adad58dbd8381d8806057b4960d5150b5e8cb3654042268e4e6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2435615495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dad0d3d0396bcda703048d42cbc6d3255050a514327be8a7fc093fb8c6398cd7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:37:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 14 Jan 2025 23:37:56 GMT
ENV MONGO_VERSION=5.0.30
# Tue, 14 Jan 2025 23:37:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.30-signed.msi
# Tue, 14 Jan 2025 23:37:58 GMT
ENV MONGO_DOWNLOAD_SHA256=acabc07cba2e1b4a8bc2a852715a21ca29cae0f08a0dc157d54c1049f586fe45
# Tue, 14 Jan 2025 23:39:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 14 Jan 2025 23:39:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 14 Jan 2025 23:39:23 GMT
EXPOSE 27017
# Tue, 14 Jan 2025 23:39:25 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aa91a2c88518c9538fcf256ae6469e45853e5871c44de25f7929857e9f5a107`  
		Last Modified: Tue, 14 Jan 2025 23:39:30 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f849d28f43c730077b955a164435a5aeab0414889ed4b5f5b554d1a2b9bd5f8b`  
		Last Modified: Tue, 14 Jan 2025 23:39:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a426d13647289f31a6d86344e080d6895d9341981efc3b9804207c32518e0e`  
		Last Modified: Tue, 14 Jan 2025 23:39:30 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86980b6cd464bb4cc56ce80aa30143ec7bae7d1aec956ab1d26454210f978fd1`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40499dbd59b428dfd2a0fda8575b878e9ca7bca73590d6f991622a886537d2b3`  
		Last Modified: Tue, 14 Jan 2025 23:39:59 GMT  
		Size: 313.4 MB (313394182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de7b6acb290eeef4729aa41b0d884393a2d9774af708d9f88426ab062b4d438`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2612e8405c4e644fd329fa38468b90fe701b45f18620e5e0dcde0b9bac15ac6`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af60615b1540c419c77c8472a240e456aa13ffc3add93f867d43dc2e9f6f5e5`  
		Last Modified: Tue, 14 Jan 2025 23:39:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
