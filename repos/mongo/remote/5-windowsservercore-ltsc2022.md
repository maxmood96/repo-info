## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:6fe58237fad4ac531a1a3dee941d7eed87959f87434ef9dcf6e6c180911cd4ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2762; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.2762; amd64

```console
$ docker pull mongo@sha256:2f584a3fe3397650aa43a02bcbb9a1c454a68003c2f0b55d47794fa3de79ca6b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2111978302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8642f63932624f0b75af114beb107a5cc56c827e8e30c93f2d9b12914f11b901`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:08:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Oct 2024 23:08:52 GMT
ENV MONGO_VERSION=5.0.29
# Wed, 09 Oct 2024 23:08:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.29-signed.msi
# Wed, 09 Oct 2024 23:08:53 GMT
ENV MONGO_DOWNLOAD_SHA256=3188d1a49244ce4a6bc4d853a3d79c178a9d0ae5e6613e4f42cf4156e6b25178
# Wed, 09 Oct 2024 23:09:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Oct 2024 23:09:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Oct 2024 23:09:52 GMT
EXPOSE 27017
# Wed, 09 Oct 2024 23:09:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe9fc17f5b4c0fb65223612ebfa62d59ecf01505d339da94b0faae63016194d`  
		Last Modified: Wed, 09 Oct 2024 23:09:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a46d55ca95960b0e155b22048e17b71885956061269c6eb7cd50eadc2a9aa33`  
		Last Modified: Wed, 09 Oct 2024 23:09:57 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394de4aece79da05623e09fc999e3e5433f8835458d17d181ea65d41685d5247`  
		Last Modified: Wed, 09 Oct 2024 23:09:57 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18f05b80d8c637a82e91bfd203b1a6953e84b003852d0f846356af2abee0711f`  
		Last Modified: Wed, 09 Oct 2024 23:09:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21eb272bb4161d167d04d28655406a6b2af4c05cfa88cdff99585cd5356787e0`  
		Last Modified: Wed, 09 Oct 2024 23:10:27 GMT  
		Size: 312.6 MB (312627782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b265dfbb83adb70672d1dd603405d80aa69208f500fd6394abcd78db6bb7245`  
		Last Modified: Wed, 09 Oct 2024 23:09:56 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e075f22259380827d334eab9516eba02b071697d5203617345bc6b7d3b4cfd`  
		Last Modified: Wed, 09 Oct 2024 23:09:56 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4831bf069888cbdc3f0fa143fddddd9b8888c40ad324404ae13d6eea867f68`  
		Last Modified: Wed, 09 Oct 2024 23:09:56 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
