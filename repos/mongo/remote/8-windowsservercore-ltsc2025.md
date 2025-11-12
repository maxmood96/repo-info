## `mongo:8-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:4396b62e6b3c7b56e241a987652e3dc26d1efc56446322d7ac1eda594a10dde0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `mongo:8-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull mongo@sha256:5196b98d56d3dbd650553e7118e380436bf0ec7c65298e42683880159ab310bf
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.0 GB (4049094507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61f2aef3cc5e5baf61f7e42a2f147f71fc8468cc9eb2362d7242ca5ee4cf828e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 11 Nov 2025 19:13:19 GMT
ENV MONGO_VERSION=8.2.1
# Tue, 11 Nov 2025 19:13:20 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.1-signed.msi
# Tue, 11 Nov 2025 19:13:21 GMT
ENV MONGO_DOWNLOAD_SHA256=b005cfd5655f0e752d80fa83a6a37be231ab57639dd2f75cf9647ad315701386
# Tue, 11 Nov 2025 19:15:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:15:21 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 11 Nov 2025 19:15:21 GMT
EXPOSE 27017
# Tue, 11 Nov 2025 19:15:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a11b482cdbbd9cf312b1e0d9026213b5d5b39b8ffefbe9c9640f45b20de717`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d324e97395bc2f7d5615ad9b57e5688675f54818099d298e8e71035554bd19b7`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29d50e946ae69e7392bb1d6c6224a392a8d842df1b028153b52c7140c527822`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aab2b46fd1b3e3e4ce30c81ff962a4857e9717a541891b91fd2f074968acd9b2`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1acf713147ac1372e91e78e77f949dcd662980f4e254ae1dd7b0af883344d37`  
		Last Modified: Tue, 11 Nov 2025 23:09:09 GMT  
		Size: 813.6 MB (813629487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02451f60a0d1e0162fff09ded04bf246ebc8358162c4ecf8fb5c1139ff499c79`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd65160aea6d78bc0bf46197a4b2ace010eb8a30ebca2527ceebfee7ef3ac860`  
		Last Modified: Tue, 11 Nov 2025 19:24:27 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f86ca6d03d63a3e43f2a0455bc16d3b5d0d6669dc62e0d319e3a0e657452eb`  
		Last Modified: Tue, 11 Nov 2025 19:24:28 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
