## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:d934c0075f6a09fef6cba2d002d7f37e28f70e2007cacaa1bff067a56a097e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.1098; amd64

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
