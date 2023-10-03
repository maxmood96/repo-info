## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:006070fd603cb6010dfc88591cdcb5906188e9bace9543cacd4ac97e0ffce033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1970; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.1970; amd64

```console
$ docker pull mongo@sha256:dce7d224a499e46939aff26a0a6e5ed3fdbdf8e6ea100f5a005c621d33963094
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2448572641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f630ef257e8d303d0ddbd1e01b4c02d475ec07b0bca26367e4a85ead6c623f88`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 01 Sep 2023 00:43:48 GMT
RUN Install update 10.0.20348.1970
# Wed, 13 Sep 2023 03:53:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 03 Oct 2023 01:15:08 GMT
ENV MONGO_VERSION=7.0.2
# Tue, 03 Oct 2023 01:15:09 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.2-signed.msi
# Tue, 03 Oct 2023 01:15:10 GMT
ENV MONGO_DOWNLOAD_SHA256=0bcdc885a437a7fd23f780a7c53a2a43aa99a3bc8bc93db5d1f0d8425066004c
# Tue, 03 Oct 2023 01:17:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 03 Oct 2023 01:17:53 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 03 Oct 2023 01:17:54 GMT
EXPOSE 27017
# Tue, 03 Oct 2023 01:17:55 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feca8e06011ab171ad74cda49c7c305e791965aef283d5b7c2b987dd5388e6c7`  
		Last Modified: Tue, 12 Sep 2023 18:24:42 GMT  
		Size: 448.7 MB (448675362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19f19fc66ee381d7fb9811b24aea9ed1dff8ef483bc0e019d3c24c09fb8fbecd`  
		Last Modified: Wed, 13 Sep 2023 04:35:02 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a56c66a8cf45d7652b52c245710bc1da6a5aef797abbd42e9ba22a48accf974d`  
		Last Modified: Tue, 03 Oct 2023 02:22:56 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97f6b1fc860a699cb650495157e61b5a2978aad717f972ce40a570420e1faea`  
		Last Modified: Tue, 03 Oct 2023 02:22:56 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3570f9e94b154586d81b11fba9b9f2327c80c3183bd70252313e5240dd4c195`  
		Last Modified: Tue, 03 Oct 2023 02:22:54 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f4ea4b0cba8d370f60a269b4c29b965b9a8dcaa80670a8b0b9ec70eed1f41e`  
		Last Modified: Tue, 03 Oct 2023 02:24:26 GMT  
		Size: 611.3 MB (611288621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10acef1a0b5b4fe5916560bfdfa448b7007352de3c375cd2b0f85b4791e2c05b`  
		Last Modified: Tue, 03 Oct 2023 02:22:54 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b8d7983739211df2c5785a982564971e24776ff5a45b87789a3b473847fedd6`  
		Last Modified: Tue, 03 Oct 2023 02:22:54 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4de6dfc9c6efdf31f876f2630e90d5d7d8a4c243885cdd1bde4348ee41c47e07`  
		Last Modified: Tue, 03 Oct 2023 02:22:54 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
