## `mongo:windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:e1912f9472edbf9f4996882cf11701b3d8b46cc2994a46c3537d20050912dd5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `mongo:windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull mongo@sha256:8f7c9735624ddf9d5b67e51ecd831255ba579011c0af552ec96357854016515f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3268989100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:956e2b03ce62058872e3e33f18069da7912ae04c1e1f996ab4110bac1bfa455d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 22 Jan 2025 20:35:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 22 Jan 2025 20:35:37 GMT
ENV MONGO_VERSION=8.0.4
# Wed, 22 Jan 2025 20:35:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.4-signed.msi
# Wed, 22 Jan 2025 20:35:39 GMT
ENV MONGO_DOWNLOAD_SHA256=52d30392e6767eb48c03fc9886b831da5a282af7aba49cc46f45c6b0f85280cb
# Wed, 22 Jan 2025 20:37:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 22 Jan 2025 20:37:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 22 Jan 2025 20:37:22 GMT
EXPOSE 27017
# Wed, 22 Jan 2025 20:37:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b12b56c5fd6794c07fefaf0232dd4a4029649ef5aafad03b3d876da0984dc2df`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd8c121d958eda51211881df659ba4a3c567827216e786eee9b1c6ff12a39fd5`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f8092e5dd1bb09ad612b643d4055b4bb34fb7d25f6b4150e626569296662e79`  
		Last Modified: Wed, 22 Jan 2025 20:37:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c392de1897e918f2a1056e13fcc94d9c6d1c66195da9e827c80d8589cc437c`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e502a895b6f681c6b079586ef7c6669574a6195e010cf7d5e63b7b0cc40557b0`  
		Last Modified: Wed, 22 Jan 2025 20:38:35 GMT  
		Size: 768.7 MB (768702153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d76470dc3e7660d9fa033ce776b68d4c7f3dd2170283cfba127e9d932f4a23`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da3ff8753e952f28001ff9b3f6e88cd03cbac0e32a9832b2e9b41e15f4f12a7e`  
		Last Modified: Wed, 22 Jan 2025 20:37:27 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d3ab988655e45e1a4a8df1efc3d73ad38cf43c5899e5a4e00cbf8a78b856cd`  
		Last Modified: Wed, 22 Jan 2025 20:37:28 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
