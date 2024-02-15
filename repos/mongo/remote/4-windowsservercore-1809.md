## `mongo:4-windowsservercore-1809`

```console
$ docker pull mongo@sha256:8593c27bbe4c7c52609219ff2dce0ea66826558c49d8d788adb515fe0aebf67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5458; amd64

### `mongo:4-windowsservercore-1809` - windows version 10.0.17763.5458; amd64

```console
$ docker pull mongo@sha256:419d10ba842927a578e0de677a2809ef1ea6b8015971d9c2addfb9283f7d209e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2326307013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa6ffadbd5fb69a1046df8f9b5e0e826a02999ebc12f86b9beb2b9d29da3981f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Wed, 14 Feb 2024 20:01:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Feb 2024 20:01:51 GMT
ENV MONGO_VERSION=4.4.28
# Wed, 14 Feb 2024 20:01:52 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.28-signed.msi
# Wed, 14 Feb 2024 20:01:52 GMT
ENV MONGO_DOWNLOAD_SHA256=406d5f9411419c0fbe9174462e2af29760ad32b877845b42ec77592acba02a36
# Wed, 14 Feb 2024 20:03:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:03:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Feb 2024 20:03:33 GMT
EXPOSE 27017
# Wed, 14 Feb 2024 20:03:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d908ab3e309f3ce320c85f39a9ca216455e949311e56a57e5f7c6c3b425c89`  
		Last Modified: Wed, 14 Feb 2024 20:03:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:860119508d392ee2fb75912e0baeb0c308e0f42a332260b9573b94c7cfebbc68`  
		Last Modified: Wed, 14 Feb 2024 20:03:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b544efbb45583935fec393ce8da01e63b009b24360b9995c7bc6df449cd2679b`  
		Last Modified: Wed, 14 Feb 2024 20:03:39 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34c1b0fbedbe1722c8043e4ed90165e459f7ca03e14ddc7f1691605ec401a3f`  
		Last Modified: Wed, 14 Feb 2024 20:03:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afad106e6eeea9d8f3222d59cc549ff03f252a730ddaef39ad70bb461081282`  
		Last Modified: Wed, 14 Feb 2024 20:04:05 GMT  
		Size: 245.8 MB (245849167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0dd2f016785bae39f58547359b61c1ad40603ba9c98c121c4fcae2e6808bbbf`  
		Last Modified: Wed, 14 Feb 2024 20:03:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5986836aa3ffdaa606e6de29df915ebc86f3bc8ed537fe54829c3537e45f74be`  
		Last Modified: Wed, 14 Feb 2024 20:03:38 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5dace45f7ddcb1bec53a51db170488ce479c1778a1d6689e19db7e962d0e91`  
		Last Modified: Wed, 14 Feb 2024 20:03:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
