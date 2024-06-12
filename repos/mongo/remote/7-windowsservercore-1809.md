## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:9ed6832adfea2ded6a0ee8a913083688ba22f17ba62fc7f08ac0e0d02dbe1088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull mongo@sha256:9c5993594a0b95c6f3b7482d128db6d9fe8d359e4096d49f706340ae29d01b72
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2840056848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:069746ca6e5ca1cab6a4d73bf34cbfc36749142b458ce9ab73a0820ffd4acbda`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:12:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Jun 2024 18:12:38 GMT
ENV MONGO_VERSION=7.0.11
# Wed, 12 Jun 2024 18:12:38 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.11-signed.msi
# Wed, 12 Jun 2024 18:12:39 GMT
ENV MONGO_DOWNLOAD_SHA256=80e1e9806e02a95c0365509ec3a4e83b8771da09a1c4df9f7d1dfbe4516a07f5
# Wed, 12 Jun 2024 18:15:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:15:16 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Jun 2024 18:15:16 GMT
EXPOSE 27017
# Wed, 12 Jun 2024 18:15:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eeda944b1e59ee631ff37afe9229f7dc647c6e816d063a5bacf59c88ce1d276`  
		Last Modified: Wed, 12 Jun 2024 18:15:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80d456b62a17a84d4f8a3224068c88b520290f4c36a8b60867def416983f2082`  
		Last Modified: Wed, 12 Jun 2024 18:15:21 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97fe44d721820e708630910cfcf25bcc9af8abff2968c1ad59b5b3e5f482266d`  
		Last Modified: Wed, 12 Jun 2024 18:15:21 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6804744b6117f3ddfa362ede394df1fde63b8d816d7b98ee8726c115ba044ee6`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9286690f3b7551208aa124931f97c81df466af93eae21988017dcdfede1adb17`  
		Last Modified: Wed, 12 Jun 2024 18:16:10 GMT  
		Size: 619.4 MB (619366551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:982a3253ac8ca5a10d9ad11939bc6db5cdbfd7c5e0ccc77e4f4fcc85b011f385`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf98e6905b7e4c6151e4288bf5ea689a2521e800f2b2625919a46ab278f2f7c0`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f63e8c7af8c9ac0d653a551b3431a46eae9238a4c2f898ee278fea559ee17f7`  
		Last Modified: Wed, 12 Jun 2024 18:15:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
