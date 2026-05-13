## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:610e0fcd36d8f677517138373cee65fab94a89e7fd4438322245d3fc50548341
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull mongo@sha256:bcd91a88f4f98fb59c2c8c4125131720d6346fadc2e015bf3a981fcb46d82210
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2940378301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67bccfe37f10e70f3f31a37ceb4e301e447e4b1cc6ce7fe652300bd13036f1d8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:52:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 12 May 2026 23:54:39 GMT
ENV MONGO_VERSION=8.2.7
# Tue, 12 May 2026 23:54:39 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.7-signed.msi
# Tue, 12 May 2026 23:54:40 GMT
ENV MONGO_DOWNLOAD_SHA256=6a326fa3ea7f2013ef28247ea4e68faddaeffc5f19cabed1059e23488986379b
# Tue, 12 May 2026 23:56:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 12 May 2026 23:56:22 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 12 May 2026 23:56:23 GMT
EXPOSE 27017
# Tue, 12 May 2026 23:56:23 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b2f6b55dd239e49adc768437fc7e848b44ff5089c3bc59e41d8461e710120c`  
		Last Modified: Tue, 12 May 2026 23:54:23 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:652860b2c2092f55ff5e79112e2f13a5b7e7721a2945b0966a879cc7ef9936d6`  
		Last Modified: Tue, 12 May 2026 23:56:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c33dae96c5b39e94e3736fe9b0a99a04a9c9f49368ca593e906f6a8af0652eb`  
		Last Modified: Tue, 12 May 2026 23:56:37 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e969f8c432a70bfc7fd67d6b9d6f65dec52d2cdc2950f4c7af794f0731f00bf`  
		Last Modified: Tue, 12 May 2026 23:56:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1dcceab9b9bd0de285357ac90b49700edd045f65b88796998062f629200bb3`  
		Last Modified: Tue, 12 May 2026 23:57:53 GMT  
		Size: 817.9 MB (817948563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf6e00128bcc391535246867ace8da539573be7aa6973a33051ee56163706137`  
		Last Modified: Tue, 12 May 2026 23:56:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c83bd014d5a6c5ef531d168166223d6a61f52dd13e6d63893cde8142feb5158`  
		Last Modified: Tue, 12 May 2026 23:56:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6557e5c54a2d045da22bb9dc150b6a760c7f25e42c2326007e2f7ccbbccccf9a`  
		Last Modified: Tue, 12 May 2026 23:56:35 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
