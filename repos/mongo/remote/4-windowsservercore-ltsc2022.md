## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:cc17487cb3f43d5b3865c6aefa14a26c52b81b44bdc2ecbd653a4407335c7a11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:a4b098fbb3e65f6247d19d4c89d4c49658b568e5e2e78469492562da2a6f0892
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2203960017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4501933e7aef0f71cbb49f2df1d3e03719b6da25de70f06f6d199847fe74b4a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:05:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 00:05:32 GMT
ENV MONGO_VERSION=4.4.29
# Wed, 13 Mar 2024 00:05:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.29-signed.msi
# Wed, 13 Mar 2024 00:05:33 GMT
ENV MONGO_DOWNLOAD_SHA256=1b4803a76653736297a96a6232774d0ce869162797ee7b628dfaecac9b36d3b5
# Wed, 13 Mar 2024 00:06:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:06:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 00:06:16 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 00:06:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc95501357532f8a5f255f06725b229b24f93de4a0ca9a048d88a0c8e987c1f3`  
		Last Modified: Wed, 13 Mar 2024 00:06:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d539b52efccb0d41a3665ae3fc8328c48b543709f6e672c72dca7a3f4de0b2ff`  
		Last Modified: Wed, 13 Mar 2024 00:06:22 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a48fa8eb5adffbb24f07c1f2c8517c0f435fa3d60e79c8b38c3ef7ef4e4a69f0`  
		Last Modified: Wed, 13 Mar 2024 00:06:22 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ff9424ed3b5d786d91abfb8f1ecf3285a8b6c3dc1c671372e1a74c8dbb8b60`  
		Last Modified: Wed, 13 Mar 2024 00:06:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7090ba404b718c8681f1039f23e80204bb80d67c04bfbf49d3c607dfbd6dc7`  
		Last Modified: Wed, 13 Mar 2024 00:06:46 GMT  
		Size: 246.5 MB (246491993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75aff0914daebc985fae0be45708efb55559180e3ac2b86f4bdf8a2b136c4237`  
		Last Modified: Wed, 13 Mar 2024 00:06:21 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5638ccfeedb1df2720dc41a4cd247e3d9409bf55b568270fbad87bd6862bbf80`  
		Last Modified: Wed, 13 Mar 2024 00:06:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e599c0735e1e5fc4e9956f901ba604c2c927f34abb13ad098e2747917b0843`  
		Last Modified: Wed, 13 Mar 2024 00:06:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
