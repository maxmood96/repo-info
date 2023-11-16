## `mongo:6-windowsservercore-1809`

```console
$ docker pull mongo@sha256:dfba6544f248fc5f8892b5093855ea349fc38e07666a03f4169b0d3e5ec36af0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5122; amd64

### `mongo:6-windowsservercore-1809` - windows version 10.0.17763.5122; amd64

```console
$ docker pull mongo@sha256:aa23bac14c94d6b0b46aca0903ead1191ba8060bb36bd4c1fcba262576a8c1f9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2575654388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e3c383d2ac6b2dc277b957112ca003fb18f24820e70df2b1de724d1e77e48a9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Thu, 09 Nov 2023 17:56:40 GMT
RUN Install update 10.0.17763.5122
# Thu, 16 Nov 2023 03:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 03:46:44 GMT
ENV MONGO_VERSION=6.0.11
# Thu, 16 Nov 2023 03:46:45 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.11-signed.msi
# Thu, 16 Nov 2023 03:46:46 GMT
ENV MONGO_DOWNLOAD_SHA256=178b163aa3a663766a792cce4eec0ca2624392bd82eb1274b91aa00f6345c34a
# Thu, 16 Nov 2023 03:49:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 03:49:35 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 03:49:37 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 03:49:37 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f7bb9e009deb881cb90e8b4318258e03882de9bc9b312b763654b59cd13d0bb`  
		Last Modified: Tue, 14 Nov 2023 19:53:30 GMT  
		Size: 406.8 MB (406811201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e4111e1324ff2110def2382c3796071edd92a76a262efa6c0657d549b64496`  
		Last Modified: Thu, 16 Nov 2023 04:21:07 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d700e6f387ca777f3718472c2f1bb858cc8fd51cc2ccc7cc4164925843c7cea0`  
		Last Modified: Thu, 16 Nov 2023 04:41:05 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4027837ff9901bf8e9b9f0494324b0f5ac6b004627f38ab852778ffadda6e7dd`  
		Last Modified: Thu, 16 Nov 2023 04:41:05 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f0b431fbca51167ebd31a4cbae4e3772e52b6dbb2f2aff54d3972b54758488f`  
		Last Modified: Thu, 16 Nov 2023 04:41:03 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d91de5442a939e96d2c2009dbf50bf0b3713e55caeb5b19d637cc01e6a7a13`  
		Last Modified: Thu, 16 Nov 2023 04:42:21 GMT  
		Size: 518.2 MB (518213394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b24a9c0d04b32dbda585c162faac63200c81668743ce6185422e7f29231ff`  
		Last Modified: Thu, 16 Nov 2023 04:41:03 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef3aa783a122513df5e32bc70aa519eb3a843f6eeee719b1ca8a3370fd56574`  
		Last Modified: Thu, 16 Nov 2023 04:41:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51def281b28880baf3fb2865ac0de8f2ea094e79bec9d607f7234f00127dc56c`  
		Last Modified: Thu, 16 Nov 2023 04:41:03 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
