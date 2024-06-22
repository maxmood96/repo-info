## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:9bf2c458fd5144ce640099d4acdd4eb52d58b785aeada12a6a7db1641c621998
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:928c5c43fdf513225b67fb76aefde0d9258935ac75ec907ccb3e1b9900b86c2d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2430717790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047d1cadcfbae002ae1d134b464cd96f0895eb94231d722ea875b4b52a7c6931`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Sat, 22 Jun 2024 00:02:57 GMT
ENV MONGO_VERSION=5.0.27
# Sat, 22 Jun 2024 00:02:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.27-signed.msi
# Sat, 22 Jun 2024 00:02:58 GMT
ENV MONGO_DOWNLOAD_SHA256=3da3dc8c13ddb8405c230c8495d4412d9a847b6c24e937b63c6b67437984a175
# Sat, 22 Jun 2024 00:03:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:03:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 22 Jun 2024 00:03:46 GMT
EXPOSE 27017
# Sat, 22 Jun 2024 00:03:48 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2657548b9787066876e82e04b0bfba729a63fd6532b2060d35d0e03308225325`  
		Last Modified: Sat, 22 Jun 2024 00:03:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0e19c0c2dcc5b10b36c1fbe872b8d9840a4bad55818b585c8e194d84081833b`  
		Last Modified: Sat, 22 Jun 2024 00:03:54 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95236217757c1ee51e49bdb46e9192bca515aa352dab49374cd207ce19b0b144`  
		Last Modified: Sat, 22 Jun 2024 00:03:54 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be7cd8d5829bae5a242af21639248e34da2c6d1741bd444ceaabe1491111aa`  
		Last Modified: Sat, 22 Jun 2024 00:03:52 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6af44dadfbc89d31188176ce4ab9e3693e407cb29d3cea08db017c88ed3c7c5`  
		Last Modified: Sat, 22 Jun 2024 00:04:22 GMT  
		Size: 312.5 MB (312518505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e772850e20002f148a183f21732931dc3471ff3f1640c6a6feb2d011ce3b604`  
		Last Modified: Sat, 22 Jun 2024 00:03:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a0f0c5927dafc0b6659d5b5bd09329f2781ac2f185410cd071c817bca0b5f5`  
		Last Modified: Sat, 22 Jun 2024 00:03:52 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bc71dabd705a7a074a29bb0f89daee9127565beb733310ab823a348e08be5f6`  
		Last Modified: Sat, 22 Jun 2024 00:03:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
