## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:7f7647a091da326140ee0d46ea7a3b2dba44c443cf7424b5aa2a314f33cef785
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull mongo@sha256:c0e998492d08c471c495afcf4e2236c6794f314889de8285c442e1f28cd0df68
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3096720235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11651e51e83972ed188417d26fa8b6c86e6e963257fc39e5dd6fb49532160d94`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Wed, 10 Jun 2026 20:15:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Jun 2026 20:15:05 GMT
ENV MONGO_VERSION=8.2.10
# Wed, 10 Jun 2026 20:15:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.10-signed.msi
# Wed, 10 Jun 2026 20:15:07 GMT
ENV MONGO_DOWNLOAD_SHA256=6027ca428953cadaef4bf6a2681e66cd3e1f9ebaa65fc961a32c4d363c55889b
# Wed, 10 Jun 2026 20:18:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Jun 2026 20:18:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Jun 2026 20:18:17 GMT
EXPOSE 27017
# Wed, 10 Jun 2026 20:18:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9483635f243f900a69ce8b88b2fafe43b529e8687251c0220c401e11aa7e421`  
		Last Modified: Wed, 10 Jun 2026 20:18:34 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77357b29115bbfa8175b741d0cd93c3b63f636880bb04febc7339287dc5778d2`  
		Last Modified: Wed, 10 Jun 2026 20:18:34 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5d9fe6ff95f6f11182b16d1f9cf297083cdf623c7d115077742ffd71eed0eee`  
		Last Modified: Wed, 10 Jun 2026 20:18:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdb2cc34960adb40dc717561781a5bbf44309cdfefb715300c9443f7edb5dde`  
		Last Modified: Wed, 10 Jun 2026 20:18:32 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6296084d21af9496aaef779862b2fcf9e192aadfbe12f76762290dc96ac6c22c`  
		Last Modified: Wed, 10 Jun 2026 20:19:42 GMT  
		Size: 817.6 MB (817568145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e279551c009a314041cc6040a85e2306d613a0da18e8f4a628e67e9ca90bcddd`  
		Last Modified: Wed, 10 Jun 2026 20:18:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56328052973c51308eade8332a9364c652f6eca80180d8a42a279f452aca6474`  
		Last Modified: Wed, 10 Jun 2026 20:18:32 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:542d61e9b49881ddde1afe5333d6cbc9b474fe1b9085572aefe68480b5dbee6f`  
		Last Modified: Wed, 10 Jun 2026 20:18:32 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
