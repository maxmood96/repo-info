## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:4d6df09d126c88c30961cef24215de0869b15a278882e8b141bf95f30739f4cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2113; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.2113; amd64

```console
$ docker pull mongo@sha256:39b88c45d64780aee7a6c198d8b2a463e225888ec2ed760b257b02b4898348ec
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404970313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e48b77a396ab235717e39936b6b53e8303b651f078b1f3e5b87592c6c15d3217`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 09 Nov 2023 06:47:20 GMT
RUN Install update 10.0.20348.2113
# Thu, 16 Nov 2023 03:18:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Nov 2023 03:44:31 GMT
ENV MONGO_VERSION=6.0.11
# Thu, 16 Nov 2023 03:44:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.11-signed.msi
# Thu, 16 Nov 2023 03:44:33 GMT
ENV MONGO_DOWNLOAD_SHA256=178b163aa3a663766a792cce4eec0ca2624392bd82eb1274b91aa00f6345c34a
# Thu, 16 Nov 2023 03:46:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Nov 2023 03:46:27 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Nov 2023 03:46:28 GMT
EXPOSE 27017
# Thu, 16 Nov 2023 03:46:29 GMT
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
	-	`sha256:9c6a2eb1682a96cceb7bab228efad120cad05912976be5ca9ace1a99e4bb6cf1`  
		Last Modified: Thu, 16 Nov 2023 04:39:36 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9439054c34c775f9b633a9755e2d431f8e46ce5614214817c7f5f79e6abd3ad`  
		Last Modified: Thu, 16 Nov 2023 04:39:36 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:711b22f8d7ca1085ca484d10447925bc78216c9d13a29f9ecd9d0f3d0ce2e3a5`  
		Last Modified: Thu, 16 Nov 2023 04:39:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38f928ffb90288a6972233fcec1583eb25f8f928ae6a7cfa7b85fed0faa7c2ee`  
		Last Modified: Thu, 16 Nov 2023 04:40:51 GMT  
		Size: 518.2 MB (518179685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bda43f406a367afcbc1841c429757d60c5f5fb1ef87008be2f1caab11c94014`  
		Last Modified: Thu, 16 Nov 2023 04:39:34 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345fcba1421f7acbfa07d252e5cb05eb093f2ac6841f93dd8f5a828305f683f5`  
		Last Modified: Thu, 16 Nov 2023 04:39:34 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea19a4cd49b7724cc5554826afc9c157c68bf614870dcb9ce21b6d66416a656`  
		Last Modified: Thu, 16 Nov 2023 04:39:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
