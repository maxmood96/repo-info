## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:3f2cbdef2154acec02b66d900d7a3f467dca17c217182d329681bb26f1071469
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3930; amd64
	-	windows version 10.0.17763.1457; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.3930; amd64

```console
$ docker pull mongo@sha256:912c28626ca278864ed31cada2e9697bc01e7d665b404afdac85b07531b646a2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5831709507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5027008de96ac2601d20dd0db3b06efda7fac0af30487ef771ea1e1b53b0b1f3`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 01 Sep 2020 19:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Sep 2020 13:23:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Sep 2020 20:38:23 GMT
ENV MONGO_VERSION=3.6.19
# Wed, 09 Sep 2020 20:38:23 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Wed, 09 Sep 2020 20:38:24 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Wed, 09 Sep 2020 20:41:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Sep 2020 20:41:25 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Sep 2020 20:41:25 GMT
EXPOSE 27017
# Wed, 09 Sep 2020 20:41:26 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bc202b498d589027cc702b23cf959b8842907508b3465b9d6ff739c9668e5134`  
		Size: 1.7 GB (1669268544 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c1d56eeebea105bba2dd1879a89adb012f98cf42708c0f36ca4af683db7162a2`  
		Last Modified: Wed, 09 Sep 2020 16:49:22 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a978721fa010ac9a32ed265f4f4741f0ed2f4b33705c4b7f6b04a252e855f1ab`  
		Last Modified: Wed, 09 Sep 2020 21:05:11 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee72aced194911cf459b6c847db2752917a452301285360bf24b07c92ce5370`  
		Last Modified: Wed, 09 Sep 2020 21:05:11 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91d6b3ad4b814837d7b6badb22247dcf546aa2bb34b45ca5e6774d696bae540`  
		Last Modified: Wed, 09 Sep 2020 21:05:08 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306da4882447b21efa56c66e49c00f44017e5053a352b91f25a31e97dbfedc26`  
		Last Modified: Wed, 09 Sep 2020 21:05:27 GMT  
		Size: 92.4 MB (92447106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1846b69ee2c5b4e604aced82fc1ad22e73b4f666c172f75163578308c44e89f2`  
		Last Modified: Wed, 09 Sep 2020 21:05:09 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2daa82c02b6f1a9c9b7e6dd9b7bc9668e5bf38e24767f9d77445a86d76af595`  
		Last Modified: Wed, 09 Sep 2020 21:05:09 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842f76cd30b4fb83cdb60b7d65823791341813064a2602c0561bd8aed25848ac`  
		Last Modified: Wed, 09 Sep 2020 21:05:08 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-windowsservercore` - windows version 10.0.17763.1457; amd64

```console
$ docker pull mongo@sha256:9227de1cd5fe97557888ac0504ff66dcb1b5a5f65c8900ce269b7ade7864c73d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2443020718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86d615af6a6e251ce271ac49c175c0ccf31bdd929ec5dbc714852ed873f658fc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 03 Sep 2020 05:59:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Sep 2020 13:15:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Sep 2020 20:41:34 GMT
ENV MONGO_VERSION=3.6.19
# Wed, 09 Sep 2020 20:41:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.19-signed.msi
# Wed, 09 Sep 2020 20:41:35 GMT
ENV MONGO_DOWNLOAD_SHA256=4375a8fa0d87dd0b16ab40a20487ddb5870d6f056d42ef654debf3e7fab6ae40
# Wed, 09 Sep 2020 20:43:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Sep 2020 20:43:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Sep 2020 20:43:49 GMT
EXPOSE 27017
# Wed, 09 Sep 2020 20:43:50 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c3aff44502467b94164764856a6feb805fc5c79ff66012eebdd7da3f180e3138`  
		Size: 632.9 MB (632939341 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:1df31adcc7026c3bf0cb32832a3f307dd6e1e54b8b3e050f8a73b5caee674d88`  
		Last Modified: Wed, 09 Sep 2020 16:48:51 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a1aa7beacb3c01eb97a75bcf3fbf2d6b9990a2c4427a2e87f3aa299d7c4f3b3`  
		Last Modified: Wed, 09 Sep 2020 21:05:42 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c5d71baad1176ea57cd07c3a1393b7237d5e30d51b46a5094c7879a67fadba`  
		Last Modified: Wed, 09 Sep 2020 21:05:43 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e9a58cd18c7fc5ef6e7584fa7668c5b030b1fbbbc2e8110267bf54f01c0c040`  
		Last Modified: Wed, 09 Sep 2020 21:05:40 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea0a9858bcb87ec8b0c73687a3126bb852164082007278af551312da5fe1af4d`  
		Last Modified: Wed, 09 Sep 2020 21:05:58 GMT  
		Size: 91.7 MB (91740535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d714ff4dbd547362ff2b30ed507a44e29c15dfe8e499c87c7c4b9efe3a5358f`  
		Last Modified: Wed, 09 Sep 2020 21:05:39 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f7f628bb4b5bbe757d1f992ef40c3c8321d9e12eef7585a3eb6c5f61038b79`  
		Last Modified: Wed, 09 Sep 2020 21:05:40 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56261e1d20be7dedf9e2bbdf9b7451061ac8e1e88543f3309fcc7e81dad80e84`  
		Last Modified: Wed, 09 Sep 2020 21:05:40 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
