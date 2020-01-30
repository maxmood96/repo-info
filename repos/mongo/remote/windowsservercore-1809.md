## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:bd39390b6519087d0ddbf88f2a2507a1c862fb1291c1242f374eed548d968048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull mongo@sha256:82e0212010b311c4704f3a4c5c4347f73390f43dd7397731199d6f100852529e
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312774548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8192bb9f0da25e0e29250ff4b3f4637022693add2e3d1628164af6e981678d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Wed, 15 Jan 2020 14:40:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 30 Jan 2020 02:40:52 GMT
ENV MONGO_VERSION=4.2.3
# Thu, 30 Jan 2020 02:40:53 GMT
ENV MONGO_DOWNLOAD_URL=https://downloads.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Thu, 30 Jan 2020 02:40:54 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Thu, 30 Jan 2020 02:58:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 	if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 30 Jan 2020 02:58:08 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 30 Jan 2020 02:58:10 GMT
EXPOSE 27017
# Thu, 30 Jan 2020 02:58:13 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2397868e5c7aa285f662aaa9309fa4756277739e11d589a663a204df80595f2c`  
		Last Modified: Wed, 15 Jan 2020 17:10:53 GMT  
		Size: 1.2 KB (1192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acd3b7a9f94cd4847b23feea2d66056638a96579a12f2aca4ce6db62bad1400`  
		Last Modified: Thu, 30 Jan 2020 03:00:39 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cee225391f6150c2df6a9470a43f853102a9a26abe48b8dde07411c1efb4097`  
		Last Modified: Thu, 30 Jan 2020 03:00:39 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed31d13c841b18e284be544cbb1084cc67495084c17d75709c946eba8d144ce`  
		Last Modified: Thu, 30 Jan 2020 03:00:36 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1330d377aa125f4cd5675297276723b1c0ae8bd82660d6e5159fb9053c588e1`  
		Last Modified: Thu, 30 Jan 2020 03:00:58 GMT  
		Size: 95.4 MB (95355063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee4a619d46b3b1ff2193252e069ec00318a79bdaadde3597cc3f76a5a88f0e45`  
		Last Modified: Thu, 30 Jan 2020 03:00:36 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96674978117b44d3d970d26ce120cc2ca8782354d80bd8e1ca394dd16b8b4d42`  
		Last Modified: Thu, 30 Jan 2020 03:00:36 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff87f3703a281dcf98a28f065abb2bd3fff49c131c4577238e36e22b4f8c2c4`  
		Last Modified: Thu, 30 Jan 2020 03:00:37 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
