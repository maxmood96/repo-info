## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:cd3e5f1fbbdb34f337954a1b3271a893835b528629f4a1fe753293e833305ac9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2031; amd64
	-	windows version 10.0.17763.4974; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:b965cd15054bf87218a356f2183ac6c30ce086f0c21daca9205290d7fc4175fc
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2173224359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1826e29b655e9024f0fd0b0515f7e5828c6ae8cddb0b977f7edf2effd7185f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 02:54:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:18:28 GMT
ENV MONGO_VERSION=5.0.21
# Wed, 11 Oct 2023 03:18:29 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.21-signed.msi
# Wed, 11 Oct 2023 03:18:30 GMT
ENV MONGO_DOWNLOAD_SHA256=3f8bff0f584ff8270b1164aaf130ad26578723a4bdcddaf001b361ae4e46e308
# Wed, 11 Oct 2023 03:20:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 03:20:13 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2023 03:20:14 GMT
EXPOSE 27017
# Wed, 11 Oct 2023 03:20:15 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c131d94d08cb023367d3fd8434c336e9d07495660367cc521ddff869fb44dc7d`  
		Last Modified: Wed, 11 Oct 2023 05:52:07 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba02f19a0f5f2b483ddb10339d2aec391fa3054bd55b5911d3663d9ad6b0f28a`  
		Last Modified: Wed, 11 Oct 2023 07:49:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1868a2debc099c26143ac4865a7a7162740e46feac09676bbcbbc63fbe121c22`  
		Last Modified: Wed, 11 Oct 2023 07:49:54 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d5446ee563750a713884e4d7654db0fb714f967d6db580185e0326f3b7b6ce8`  
		Last Modified: Wed, 11 Oct 2023 07:49:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32106c4ba20dbd847d4a489f038a878960342985c9cb49283af7fc46a31e932a`  
		Last Modified: Wed, 11 Oct 2023 07:50:44 GMT  
		Size: 313.4 MB (313372045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad633eb4b8425ef20358014a83d3ed28cc0b4c33f1e5027d1a85267f5881af2`  
		Last Modified: Wed, 11 Oct 2023 07:49:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30ba1e165ff8125aa1a57bc1a4a3c234c758f91c7697ecb689fdbe1d0061ef5`  
		Last Modified: Wed, 11 Oct 2023 07:49:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8972d2f6fdfac90b869a3b425d8fb06643829e883b23d259a920faee237ba7c7`  
		Last Modified: Wed, 11 Oct 2023 07:49:52 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.4974; amd64

```console
$ docker pull mongo@sha256:32486bd7fa3f05e3129ddc7436341bf49ffea88914fcc241256fda0a898e4c8f
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2345013305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45998a8c6bfcff88298dd4aa999891ac9f4d403e2463eaaa4d67527d4f75f35a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 02 Oct 2023 08:29:38 GMT
RUN Install update 10.0.17763.4974
# Wed, 11 Oct 2023 02:58:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Oct 2023 03:20:26 GMT
ENV MONGO_VERSION=5.0.21
# Wed, 11 Oct 2023 03:20:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.21-signed.msi
# Wed, 11 Oct 2023 03:20:28 GMT
ENV MONGO_DOWNLOAD_SHA256=3f8bff0f584ff8270b1164aaf130ad26578723a4bdcddaf001b361ae4e46e308
# Wed, 11 Oct 2023 03:22:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Oct 2023 03:22:36 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Oct 2023 03:22:38 GMT
EXPOSE 27017
# Wed, 11 Oct 2023 03:22:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af2bcb37edaec1dd87fc4a6f7c9129ca37bf1f91b65eb365ba9d4c70473beea`  
		Last Modified: Tue, 10 Oct 2023 17:51:10 GMT  
		Size: 381.0 MB (380970130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a4919cd870c32d33d8113b108e3e6ea2391bbbc70b2cf7e9febeeee307b1a4`  
		Last Modified: Wed, 11 Oct 2023 03:40:35 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9faf2d00f7019520382149c6bba4b9412b715ff8371f42c3a1a202a8272bd64`  
		Last Modified: Wed, 11 Oct 2023 07:50:57 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32a36d9785a6712b868c88a1ce0250e2c9b9c66a45440addffa2d7c02c74a51f`  
		Last Modified: Wed, 11 Oct 2023 07:50:57 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b46ff223dac17519a55ed78fbbdf526be9c5cb07d585d3ff9761094b18519a`  
		Last Modified: Wed, 11 Oct 2023 07:50:55 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee23f953e05b5d4ce4772c64fb9ca56a293a7414f7dfef56f4973557aa1e02ca`  
		Last Modified: Wed, 11 Oct 2023 07:51:42 GMT  
		Size: 313.4 MB (313413348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ff4fa07dd333daaff8cbad971b32c77523eea82fcd4c8698bb03257facb29a3`  
		Last Modified: Wed, 11 Oct 2023 07:50:55 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22248de47d8bcf326535b3f80945bfea068b21b2262a3989e031012ddc09c21`  
		Last Modified: Wed, 11 Oct 2023 07:50:55 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322112dafb9044a2f1afc131afa3bbbfdda84f35c0c7f3d76f3592d004ef2cfc`  
		Last Modified: Wed, 11 Oct 2023 07:50:55 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
