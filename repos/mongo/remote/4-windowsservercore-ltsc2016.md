## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:9b465214c1a5519ea93ce8e61cf0a33f388b46c157984807f8e596a5665b75ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull mongo@sha256:f085fb326183128e5fe322894def5a10dda6318c7e2f74c1154c949d712da161
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6190835990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7596b2a81f99a099b5cc99c2e9a3d55672efb2d6128350d64d2c4b4982d1bde`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 13:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 26 May 2020 22:25:26 GMT
ENV MONGO_VERSION=4.2.7
# Tue, 26 May 2020 22:25:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.7-signed.msi
# Tue, 26 May 2020 22:25:28 GMT
ENV MONGO_DOWNLOAD_SHA256=d085db55ea34452617e73a5d7ad80fbc4b9eaf75990e49080a7c3ced13fbb42c
# Tue, 26 May 2020 22:43:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 26 May 2020 22:43:46 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 26 May 2020 22:43:47 GMT
EXPOSE 27017
# Tue, 26 May 2020 22:43:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:78d9ecf24b3b7ef3e61c8b38d40e28e57a80552d6c97884f4cc142af2110ddff`  
		Last Modified: Wed, 13 May 2020 14:28:09 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640e7a63c9aec24a469438efaa13fc121aaba0353301bc0c9ce413287c5150fb`  
		Last Modified: Tue, 26 May 2020 23:00:44 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bafbea768cc18739ff7e474820256298a49d05507183a84cdb810a21c76b4c`  
		Last Modified: Tue, 26 May 2020 23:00:43 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76418b70f7bbd1bb3a2a30f5565beb763a89566d6d01b14447e3f9ceba2e9a2f`  
		Last Modified: Tue, 26 May 2020 23:00:41 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c5be6494c2d31b3360315d66448589e34bbbddca7d7d38ca9efcf52e1e8916`  
		Last Modified: Tue, 26 May 2020 23:02:07 GMT  
		Size: 458.9 MB (458938127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:417ee012d50e96e3efb3f1b7446eeba4248b20c46dc6b74a313de76e4f06bb52`  
		Last Modified: Tue, 26 May 2020 23:00:41 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65bf0b68ed52d45bba2dc25884be14ad40e6f686a4d3e8e0f21142aa4c131abc`  
		Last Modified: Tue, 26 May 2020 23:00:41 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9edc3fe665f0e36f2337433e1aec7ab91290ed0c391725e2973a78a498eaac6`  
		Last Modified: Tue, 26 May 2020 23:00:41 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
