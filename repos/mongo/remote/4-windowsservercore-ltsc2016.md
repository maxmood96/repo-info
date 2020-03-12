## `mongo:4-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:252d9092a44cb76ce1978defc409db903e14ffa2b022b7a58293c4583db38a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:4-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:ffcd7945296fd6bf2d492a8fbd2d76b87b4d700b617a3dbc3113ad3609dc1e99
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5823379228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14b1841c6da45b9f09da659b319ee3ec76161c255d3a0299c744e58541cf1d5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:31:28 GMT
ENV MONGO_VERSION=4.2.3
# Wed, 11 Mar 2020 22:59:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2012plus-4.2.3-signed.msi
# Wed, 11 Mar 2020 22:59:47 GMT
ENV MONGO_DOWNLOAD_SHA256=234f6abf9c4947df94428f6ce648905dbf6b1269f48cc3239ebd4990bde1ca2a
# Wed, 11 Mar 2020 23:17:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 23:17:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 23:17:18 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 23:17:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:846a2223e9e7a88a2a07d706553f144d380483d72fb9f0697c4fcd71773a8693`  
		Size: 1.7 GB (1657079102 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:0961c48658cd7865bcf6c05285dfbe8ad89cd52059088d7f4eed6fde1bb2b385`  
		Last Modified: Thu, 20 Feb 2020 05:18:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53763da721aa3ae58cd704805589abe169e1d3d28218280db0ed4045881d52cc`  
		Last Modified: Thu, 20 Feb 2020 05:44:18 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28575cbb1dce05be3e8ec069dac86a4ae8b751008d4f0c9654ea8a5adb6a05d`  
		Last Modified: Wed, 11 Mar 2020 23:40:27 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b0fd752a2977b6c56e9008cdf13c5221932c0fa7d04c8b82af7b1e365d7dcb`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a599774a11cf582afd1c631f47ee898b2d7b7bd6c85e6a169f55999aebaf3f`  
		Last Modified: Wed, 11 Mar 2020 23:40:50 GMT  
		Size: 96.3 MB (96305864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158acd728c1a7f81dc5ab0e6ab015b47dbfe43d906b6935e6b3fb5af9ac717c9`  
		Last Modified: Wed, 11 Mar 2020 23:40:25 GMT  
		Size: 1.2 KB (1221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1207ac339b253e1f2d5d984071f0cd6b1c14321de6258b95f05756828577ef`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7bafe8e7fe89107a1cc111971c17ff5bfed4f23c13b7e8351d50dfedc51894`  
		Last Modified: Wed, 11 Mar 2020 23:40:24 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
