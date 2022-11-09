## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:8ffd0d6bcf9779531786820d7123b83ab6072e174e16849188e0d16495b225d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:78b2e7438587e7a5653fb03bb8a5c25d280e8597f02a25939de96e6921b697b7
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3291082908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eecef695ec74bd59d29fd578d4be6f56a5fd070d32351df46f030ab2a53a807`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 18:24:30 GMT
ENV MONGO_VERSION=6.0.2
# Wed, 09 Nov 2022 18:24:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.2-signed.msi
# Wed, 09 Nov 2022 18:24:32 GMT
ENV MONGO_DOWNLOAD_SHA256=964a7e33927a8c01a6177daf0bf49f3ec17560b1b78f8be60ec641a03c55cb18
# Wed, 09 Nov 2022 18:28:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 18:28:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:28:03 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:28:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26cc6e4f9eb1ae415a5ead6f884cac597bbd57efa6cd042c878d5b54c9d2091`  
		Last Modified: Tue, 08 Nov 2022 19:44:35 GMT  
		Size: 854.3 MB (854317461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99941fb33972e616b231a8aadd93463fdfd5de6aece4aa6c470d2feec31839be`  
		Last Modified: Wed, 09 Nov 2022 16:48:23 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0fec38ff3c242baf141e10c6a5b81f008c9915acd4dd9cc327eaf296892c96`  
		Last Modified: Wed, 09 Nov 2022 19:04:32 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:537c68971b182ddb518477c6993accb024778f71f16894ed90390301eb7a7dbb`  
		Last Modified: Wed, 09 Nov 2022 19:04:32 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f07b977aece83110fb1358d8b0863f8ae2635c61e505e11cbc078e175a12c50`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17aef8040e1f6a5348317cc5430061159238fc4f6004b23714a8a5b6a5b50e91`  
		Last Modified: Wed, 09 Nov 2022 19:05:56 GMT  
		Size: 512.5 MB (512486276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7866b495e26e50fe549700b9f846f7f279dbd5e27aaa6901017e8a414412681`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e8a72583964e2d9524c834c0288f7032834759c8d3f683776c31e66ab24423`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b494701b847f8225f597c05baec6c20bcd3464f492576d85be3260aff75ec192`  
		Last Modified: Wed, 09 Nov 2022 19:04:29 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
