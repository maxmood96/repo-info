## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:cbf77948007fc2cbbbd824c226739abe78b0c2079e47bfb59593c988d96c2704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64
	-	windows version 10.0.17763.1098; amd64

### `mongo:4-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull mongo@sha256:51247f0989f85aa06282e26bdef38ef82bd090adf0080f1890eac6f8bdf77d40
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5825104776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95edaab6ef371408b1619dc10527640da55e7c27b4fe99f1046bcbbe832d212b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 18 Mar 2020 12:27:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 18 Mar 2020 15:29:30 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 18 Mar 2020 15:29:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 18 Mar 2020 15:29:31 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 18 Mar 2020 15:44:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 18 Mar 2020 15:44:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 18 Mar 2020 15:44:04 GMT
EXPOSE 27017
# Wed, 18 Mar 2020 15:44:05 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8cd5aa189dca96a2d4bcc0e2516d85f8a69d277957f44aca08575ecf42e5bc2f`  
		Last Modified: Wed, 18 Mar 2020 13:22:17 GMT  
		Size: 1.1 KB (1107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0999df35d8fb5dd399c53e54439a7db91402a4bf545c8c889d72d501b9a9c562`  
		Last Modified: Wed, 18 Mar 2020 15:47:41 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5ff07621b1d4312c93fcd13fc9ebdca8bd52201578b10f463790495782d6a1`  
		Last Modified: Wed, 18 Mar 2020 15:47:41 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dcc198f35743e5d704adf34dd765aebd5e4426126c09a9f129b22bbdc2c768c`  
		Last Modified: Wed, 18 Mar 2020 15:47:37 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:554b279b4fc5a5007413ec72b594d1edcaeef1cc46d3a433a43680f719168100`  
		Last Modified: Wed, 18 Mar 2020 15:47:57 GMT  
		Size: 96.3 MB (96335695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64e01bd5719c67eaa1dd3048c9e79e2a33d92115d882caa5a8912a1a266abe3`  
		Last Modified: Wed, 18 Mar 2020 15:47:37 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de485c8b832707950af0e576071151f000a5956c57fc0a4e724b41c3e027fc8`  
		Last Modified: Wed, 18 Mar 2020 15:47:37 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce79855eb1f746b2d2c30400b9e49d94f7682f5cbf08584851cb33cc859bab`  
		Last Modified: Wed, 18 Mar 2020 15:47:37 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull mongo@sha256:aac754de81af2f5d162c77a945382332cffd5575897c7601ef472343cb844896
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2720597037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0aaebe9da6481c2ac37ceef6336551122a88bb8c6e0f0273b2b1408c89f3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Tue, 10 Mar 2020 23:23:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Mar 2020 23:17:35 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 23:17:36 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 23:17:37 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:37:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:37:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:37:08 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:37:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb49f89affc2d69b541463d095fdfbe61fa62e02b0aa5fa6d26bc134fb66bf35`  
		Last Modified: Wed, 11 Mar 2020 00:30:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a556cdd1dac3043338300637cf3645822f875ee02355952ab1cd7751e1b68bc`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dcc51a0e27cfe040ead7b64a7c6a800c4c738b534689744bc5736c486935beb`  
		Last Modified: Wed, 11 Mar 2020 23:41:10 GMT  
		Size: 1.2 KB (1220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f7203b7c8fc0a4e01010792bc0a916bb1d80725bd8a4e8f11428ee3160d35f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22af9a292df27880e2bdab8b6325e55b0ca496959f7b3cbc864addc1d08d102d`  
		Last Modified: Wed, 11 Mar 2020 23:42:15 GMT  
		Size: 455.3 MB (455252292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb17de172b016b72e14b1ad1dc7b0d91f65115cd25a7268d5758b93956a3298f`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0a4339164f7d75bf46ec45b216b30960178423acd470a8d3f7fa23bcadb1e05`  
		Last Modified: Wed, 11 Mar 2020 23:41:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29d93e6248494f3397e2328ebfe14d053d0679135d2853daa7460ecf197df7`  
		Last Modified: Wed, 11 Mar 2020 23:41:08 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
