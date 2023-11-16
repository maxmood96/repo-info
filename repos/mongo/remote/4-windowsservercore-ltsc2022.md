## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:0f04d583f3c9d34ece73197900aa2fa43115cb38dbdce693ae80b606c2e8621b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:1808f6123d1856675aed931e4c8ba9d30d6e298784a161e5932076c4752cf6d4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2132343767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f697d2cee94ad7c8ff98e0d1402fa188f4ccaab72f912d1e0bca5068b26b0ddf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 03:18:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 04:11:06 GMT
ENV MONGO_VERSION=4.4.25
# Thu, 16 Nov 2023 04:11:07 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.25-signed.msi
# Thu, 16 Nov 2023 04:11:08 GMT
ENV MONGO_DOWNLOAD_SHA256=e9158fe81fd49b1e0bb121c5505e674864587e78b72683d8b477b4326da8472a
# Thu, 16 Nov 2023 04:12:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 04:12:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 04:12:27 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 04:12:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7989ef2c4cfb06d845746a3c3660481ea84d3f5c8216041855ce528f0ac4015c`  
		Last Modified: Tue, 14 Nov 2023 20:43:13 GMT  
		Size: 498.2 MB (498182566 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a73dc3dec59ae25ff1232f5fdf2ab39df387f3bf86ba48717ff271d76c2feb`  
		Last Modified: Thu, 16 Nov 2023 04:19:26 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eaf10a0998ecbf0cd8382ad3ec12655400017897128ef1b7a79bd9ee4366d42`  
		Last Modified: Thu, 16 Nov 2023 04:58:10 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0787607031a7dbd536f157f6c20dc82998aada5610dba8c1523981d2fd5dc6a4`  
		Last Modified: Thu, 16 Nov 2023 04:58:10 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bdcba1d3b70c570d30cfc4f2d095eb6c00978b1e6ae1c6d33a7f216c952088`  
		Last Modified: Thu, 16 Nov 2023 04:58:08 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec28ae0b6b9e078510bca4f94f2e6063dd61574ca6546a382f1c8258540a4a6`  
		Last Modified: Thu, 16 Nov 2023 04:58:53 GMT  
		Size: 245.6 MB (245552496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7013c4da9067188df3593242c8f98b058574ac28fe554b04bfdd9aadf8e63cb`  
		Last Modified: Thu, 16 Nov 2023 04:58:08 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c775083f4ff437058e9488b272a33a9b8bb206e552c51ad73a57c7f444d52fe9`  
		Last Modified: Thu, 16 Nov 2023 04:58:09 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0efbb6f29c03b5dd240f4d02b06e293d082815a05388855395d40c263d5c77a7`  
		Last Modified: Thu, 16 Nov 2023 04:58:08 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
