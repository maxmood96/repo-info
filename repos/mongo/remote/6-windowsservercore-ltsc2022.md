## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:c9e80df28a378f0a7c4c5beb6c5755e69c72bf0dd60f37ba1c2a884f74574073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull mongo@sha256:46e310a6f5f8d551dcda5f490db83fd34d9e2561ffcd08f56c3f8df1a6ae9adb
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2635590069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05dbfbf21359595e9335cf57a8f3759163d24ae4bb97f6129ca319f6d1238282`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:03:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:03:34 GMT
ENV MONGO_VERSION=6.0.15
# Wed, 12 Jun 2024 18:03:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.15-signed.msi
# Wed, 12 Jun 2024 18:03:36 GMT
ENV MONGO_DOWNLOAD_SHA256=a59408edea70438c1c9793ecdbc8b2111e44f10dd90f1ed0d2cc8071ae1cc95f
# Wed, 12 Jun 2024 18:04:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:04:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 18:04:42 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 18:04:44 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d74b26c9f06ce059b51b251fcb653bb4ab32cc521097ca425519f3b1af642f8`  
		Last Modified: Wed, 12 Jun 2024 18:04:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:123ef57a8a046349d723c4b9aec6a0e162e4146a4fd8386a88eb5951339596c5`  
		Last Modified: Wed, 12 Jun 2024 18:04:51 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dea9b3ddd0a033622ddd5da4bcc76d55c784d5d2d82c98582d8020e4910b95dd`  
		Last Modified: Wed, 12 Jun 2024 18:04:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9333329224bba2594b491534b638047f22db422eef0afaedd079f1dc1d84a96`  
		Last Modified: Wed, 12 Jun 2024 18:04:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2921edaaf27bab48144676fc6f4627c4f26e2dca20c862265004a90ef7863a`  
		Last Modified: Wed, 12 Jun 2024 18:05:32 GMT  
		Size: 517.4 MB (517402376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90f9ee9cd29fd0a28901bf48ae7784d2c04cf55996393c1817458b597131db51`  
		Last Modified: Wed, 12 Jun 2024 18:04:49 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe204bd4f63efddc11c0d7735566d7deed4b5efdaa9ed645875823c74955174`  
		Last Modified: Wed, 12 Jun 2024 18:04:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24301ffeb191b37211e9c047d7022067b5a6c157ebacf6ac2b0f3fa31b92b0ce`  
		Last Modified: Wed, 12 Jun 2024 18:04:49 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
