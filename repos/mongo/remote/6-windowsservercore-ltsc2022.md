## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:07addde2f7cd36a9d3f9656315206552fc0ea04bc18622ab884adce9411eb8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull mongo@sha256:dc0558869507ef862d8302245401cf5bd78ed40ecea2161ecef9d445c6266b5f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432721126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0cf1f8a6eb0c5ff42a19bf921f222d1ff227456ce5779bc9d6728ff2c0070a7`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 01 Mar 2024 00:49:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 01 Mar 2024 00:49:31 GMT
ENV MONGO_VERSION=6.0.14
# Fri, 01 Mar 2024 00:49:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.14-signed.msi
# Fri, 01 Mar 2024 00:49:33 GMT
ENV MONGO_DOWNLOAD_SHA256=871a352e6eb31f2d4d74816b6511cc350697c2004580f79f652f1a9237ea15c8
# Fri, 01 Mar 2024 00:51:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 01 Mar 2024 00:51:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 01 Mar 2024 00:51:51 GMT
EXPOSE 27017
# Fri, 01 Mar 2024 00:51:52 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47c3bbe53a3bfeb7f0c027c2325a5dd42be28db2b2e053da19d304582f6395fd`  
		Last Modified: Fri, 01 Mar 2024 00:51:58 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c077e4ad5374569d747d5e360cfd19eb51c8c9eb11c37a7e93ef907837c11419`  
		Last Modified: Fri, 01 Mar 2024 00:51:58 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03718ce91fc257c03ed6195cb5e7cc2df29c1009f96bce0d1617e997819b3116`  
		Last Modified: Fri, 01 Mar 2024 00:51:58 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b99b0b2ff476521a5ef8859db439ea9849290eb6c1044a28abe30f919c2baac`  
		Last Modified: Fri, 01 Mar 2024 00:51:56 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8ec74e6ca0078631773807a37b5b1e8054e9a74bdca4f83d60c1ad043b2990`  
		Last Modified: Fri, 01 Mar 2024 00:52:37 GMT  
		Size: 522.1 MB (522057904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81696c4b2f33e63d99ef155a4ee229d5c287aa5eb3fd4c2dd83ac29412fa276e`  
		Last Modified: Fri, 01 Mar 2024 00:51:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099d34dbd53c3702d8a2f8f5f2575ef6922c6003f17d928edf7b81e9b1420463`  
		Last Modified: Fri, 01 Mar 2024 00:51:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1296f48c9b891aea0d1f3e4179230218ed49beeaab16f26740df43491d6b56bd`  
		Last Modified: Fri, 01 Mar 2024 00:51:56 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
