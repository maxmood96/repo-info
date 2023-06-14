## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:c075c23211e55942fcdde5c5593492b5f26a1d3818fe354a141a6a5709ac148e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:e228fe5b3674618df7769f757850344758752d407e8b17f502f8e4b29691d35d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1904729856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a084709faf06b2b756b920c919dfd025b9b0ab44e9763b11eb3cdc1f961d3b01`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 14 Jun 2023 19:16:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jun 2023 19:25:22 GMT
ENV MONGO_VERSION=6.0.6
# Wed, 14 Jun 2023 19:25:22 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.6-signed.msi
# Wed, 14 Jun 2023 19:25:23 GMT
ENV MONGO_DOWNLOAD_SHA256=585afad69ec57040b1a8f502a039c3fef160dccbe6c48c53e15adde9976724a6
# Wed, 14 Jun 2023 19:27:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Jun 2023 19:27:33 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jun 2023 19:27:34 GMT
EXPOSE 27017
# Wed, 14 Jun 2023 19:27:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c45a9c91ac9cf27bb12f7baad712822dbb1e41b172e97946a8d48287c1570eb5`  
		Last Modified: Wed, 14 Jun 2023 19:49:55 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94a8b14c0a3d4c07cb84d06d39233ec5289acef9c336519bd5e97ac73b4faf0c`  
		Last Modified: Wed, 14 Jun 2023 19:56:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67c16f46f78d5d430633964dfdda09cc7dca7398fce10509df1e01d3a764af1`  
		Last Modified: Wed, 14 Jun 2023 19:56:44 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d2e92cc1b722ecac30ccbe937d4392ae5d27254ab9afbb171360507e618416a`  
		Last Modified: Wed, 14 Jun 2023 19:56:42 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d6b51a3648d3b18dbe64644a6e4b97daa11af6f93fd9fca302976bc08025e0`  
		Last Modified: Wed, 14 Jun 2023 19:58:03 GMT  
		Size: 516.1 MB (516121765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbd6ae7574a30275bb1a02b8a217d58a2bbd47bae631d980a1ecaa515b5c688`  
		Last Modified: Wed, 14 Jun 2023 19:56:42 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab32a7ccf6585d9bbaa9b7dee7439091920abd68cae0ef7dcf1ad407d19160e2`  
		Last Modified: Wed, 14 Jun 2023 19:56:42 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f3946f6b6968597f88486a5abbc1092d7d7d27efb7feb2f53086a77db49edf`  
		Last Modified: Wed, 14 Jun 2023 19:56:42 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
