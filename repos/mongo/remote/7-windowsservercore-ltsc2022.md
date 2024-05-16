## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:a38af72a6cde3a2068ddc142e72462ccb09fc563640a6c22394e8bc9b4885132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull mongo@sha256:181226e579d6652754a567be56ea5fa0a9fe0eb665f83402562cc4f7f4987145
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2730855601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3dfee0115022b40926d5c7971046a1071e67b952f9b97e4421d1e55d14926c4b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 15 May 2024 21:53:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 15 May 2024 21:53:04 GMT
ENV MONGO_VERSION=7.0.9
# Wed, 15 May 2024 21:53:04 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.9-signed.msi
# Wed, 15 May 2024 21:53:05 GMT
ENV MONGO_DOWNLOAD_SHA256=16be51285ed6042c39a8692b5cfed3413f53b37111f54861a72857af6e5cfa90
# Wed, 15 May 2024 21:54:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:54:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 May 2024 21:54:49 GMT
EXPOSE 27017
# Wed, 15 May 2024 21:54:49 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc181c61bb6197839d34e5e58f5efcb7632308a971973524da6bcf0b025ca2b`  
		Last Modified: Wed, 15 May 2024 21:54:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a1a89a1f9048d8ca81b2eeb03d691b73e022f18d7e68b615215c91189914f4`  
		Last Modified: Wed, 15 May 2024 21:54:56 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a9bf4f59df7a12fe2f8c0e94da97c35c37dbcd375d63a7a91524ec376f1427e`  
		Last Modified: Wed, 15 May 2024 21:54:56 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23995cc19a04bedf877c9134991dac2e23518f07b3534b7abf1d3eef0c82c257`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29e86efc42e159c66bccbf6bc9cb2f317f5614769fdcc815f69cb174b255b682`  
		Last Modified: Wed, 15 May 2024 21:55:46 GMT  
		Size: 618.2 MB (618175233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcab4707953b50aee36c96f8a41a82d13b654010aaa96f46e1c3ef539de6ef27`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0714ae8345915e9969e7901c905ecd4fc2164731820bcf6db13639a0224a42`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84520f94eafcc92344543dab13cfc52b8d29aaedce312c4077f3d643798caf3d`  
		Last Modified: Wed, 15 May 2024 21:54:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
