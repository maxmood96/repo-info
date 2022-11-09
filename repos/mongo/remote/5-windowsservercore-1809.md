## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:d5ecc551d87a2d81ad6b6dbde3a9c07f2500a81861b4da5f99fe8630a6fc4d27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3650; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:0b262de63d652445da58212aebfd948e1e7863809911b81c811c8ca8a325b90c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3089660187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33ad86705ba21bbf2a5e686833710d42d81e44632b2e3e73d4a6f152f0c2cacc`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 05 Nov 2022 18:29:26 GMT
RUN Install update 10.0.17763.3650
# Wed, 09 Nov 2022 14:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 09 Nov 2022 18:33:42 GMT
ENV MONGO_VERSION=5.0.13
# Wed, 09 Nov 2022 18:33:43 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.13-signed.msi
# Wed, 09 Nov 2022 18:33:44 GMT
ENV MONGO_DOWNLOAD_SHA256=f9b1e144822887bb361ad218967f4cbfdedb6d59e70b12b564b4b63a4d5cbf6f
# Wed, 09 Nov 2022 18:36:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 09 Nov 2022 18:36:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 09 Nov 2022 18:36:19 GMT
EXPOSE 27017
# Wed, 09 Nov 2022 18:36:20 GMT
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
	-	`sha256:f01c2ba8482092a442d0068bd41660e28e38bb439a5d100aad39c482ca731862`  
		Last Modified: Wed, 09 Nov 2022 19:11:00 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f94877b2329abb8eb1c778e441f24799ca7e9b4ff897ca023a25dbf84fb4830a`  
		Last Modified: Wed, 09 Nov 2022 19:11:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf54bf74a5c999c26c5e57322fcfdd4e6d6699cd6d68878cdef7e687daddec1`  
		Last Modified: Wed, 09 Nov 2022 19:10:58 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25098a9a92a79b96c0f825f171c8dfd75a7a9ced2a9e5ec56c14a81a5eafb4ac`  
		Last Modified: Wed, 09 Nov 2022 19:11:55 GMT  
		Size: 311.1 MB (311064132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08c43056087a3ad35bcae9b4f573e0b2965a9c4268522596f28405ea95f6cf8`  
		Last Modified: Wed, 09 Nov 2022 19:10:58 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75101d079246176e36ce0968969584c0a45ba144f46a4e4afd35fb8d460625fb`  
		Last Modified: Wed, 09 Nov 2022 19:10:58 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:852c2f05ebcfacdf9d549800915ff1801a7648c6a88077207ed71b9bf1be5978`  
		Last Modified: Wed, 09 Nov 2022 19:10:58 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
