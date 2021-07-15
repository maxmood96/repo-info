## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:b6be4840e58e4e222837daa8beee4d4b183a758fb2f60cad30da9d21a73cff60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.2061; amd64

```console
$ docker pull mongo@sha256:583073797eacde924c96f95aff64c579246fa495549d10fb677bb37ea6cff4a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2975832945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c8a7ccb1909c83580f8c8769a2da646baf187cbdca1ba4ffc64ae7a74f6d8f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 06 Jul 2021 20:34:18 GMT
RUN Install update 1809-amd64
# Wed, 14 Jul 2021 01:07:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Jul 2021 01:07:30 GMT
ENV MONGO_VERSION=5.0.0
# Wed, 14 Jul 2021 01:07:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.0-signed.msi
# Wed, 14 Jul 2021 01:07:37 GMT
ENV MONGO_DOWNLOAD_SHA256=26920cf86cf1eea8acbf395ad12b0b94631ca4175dc47588a5dc4d9221f014cd
# Wed, 14 Jul 2021 01:13:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Jul 2021 01:14:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Jul 2021 01:14:07 GMT
EXPOSE 27017
# Wed, 14 Jul 2021 01:14:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f143c6fed32d477c35b660b2e108ea62e3593c03e44bd9ced208ce52b26b0841`  
		Size: 967.1 MB (967113907 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:adcec6ff907307155c0652222cc9b95a0cc964d4c371e02767e72a5c90472192`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ba00b69bf586531acf7efc20fc81dc4999d814cf0569cc072e1302492e3f11`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62d00ee3059d4a1d94509843dca7851a95b814976100864963b647f52607358`  
		Last Modified: Wed, 14 Jul 2021 02:02:19 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:357882103d154942b3e8762c0dedc4c830de99023e0ecb345fb8fc9fbdeb4dbc`  
		Last Modified: Wed, 14 Jul 2021 02:02:17 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a8938c18426de8f03985c6d625d449b206a37bb87d01d3b00cd6c6fdd57aa9`  
		Last Modified: Wed, 14 Jul 2021 02:03:18 GMT  
		Size: 290.4 MB (290376267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bbcf6b6079d1ac7b75f7374484401ce5170d6176044d1f158ebcef72c0ba92`  
		Last Modified: Wed, 14 Jul 2021 02:02:17 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:766e672045b350b08cf7fcd9b8a6f01ab8af895b5cdfd81871e314ccb4d28efe`  
		Last Modified: Wed, 14 Jul 2021 02:02:17 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec691ab2f20fd8c0fac35aeecf30f62d30572db0b0966f5338fc68386e7e266`  
		Last Modified: Wed, 14 Jul 2021 02:02:17 GMT  
		Size: 1.4 KB (1386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
