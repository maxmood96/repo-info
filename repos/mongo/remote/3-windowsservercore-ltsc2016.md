## `mongo:3-windowsservercore-ltsc2016`

```console
$ docker pull mongo@sha256:119864376569cbeccbb83d4eec939c7439dd733f57d970246b3998b5dc9dce7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3506; amd64

### `mongo:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3506; amd64

```console
$ docker pull mongo@sha256:6763381f4a67ddb7df259a4187887006e19ee9253e592ff2bb60c1059bfcdf31
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5820567995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26b0054534cef77b808f6755003209a9fd4a5056f058edad907cc6c50409ffd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 14 Feb 2020 21:42:00 GMT
RUN Install update ltsc2016-amd64
# Thu, 20 Feb 2020 05:12:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 20 Feb 2020 05:19:42 GMT
ENV MONGO_VERSION=3.6.17
# Wed, 11 Mar 2020 22:15:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.17-signed.msi
# Wed, 11 Mar 2020 22:15:39 GMT
ENV MONGO_DOWNLOAD_SHA256=b20b72d5366a7a00cb85245ebedd01b665bbac4f918dd5fac7a7c5eb68477c26
# Wed, 11 Mar 2020 22:28:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\mongodb\bin\*.pdb -Force; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Mar 2020 22:28:24 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Mar 2020 22:28:25 GMT
EXPOSE 27017
# Wed, 11 Mar 2020 22:28:27 GMT
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
	-	`sha256:4863e5701bfa2388492681880718703eecf4360e943021e702f897bc078de68e`  
		Last Modified: Thu, 20 Feb 2020 05:40:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8875ee76ce08286dab2e650f9808e785bc0f79acb4c15382048735765497b07`  
		Last Modified: Wed, 11 Mar 2020 23:38:14 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa284f8065be9eb03e643bb9dd50a603c5b6e8813bb0d4ddb7e75987fc5b4d`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae68ba460a8f3dc989becee8ef2d59e650742bc77ba74a98d0c8e12ace493d19`  
		Last Modified: Wed, 11 Mar 2020 23:38:54 GMT  
		Size: 93.5 MB (93494538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead5918efa91f150d4991d381d85158e23cdab0f832fd73a318fb4af300348d1`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b8dc5e80e6329a94b954cc8673d91fa2222d35ee9569178e1e0502c6ed2d14`  
		Last Modified: Wed, 11 Mar 2020 23:38:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a47d981e96991c1baf1c50d2090a8accbe1a377c893fd4d7aa22e580bb24e35`  
		Last Modified: Wed, 11 Mar 2020 23:38:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
