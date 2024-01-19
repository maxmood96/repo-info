## `mongo:4-windowsservercore`

```console
$ docker pull mongo@sha256:2eeee02be6b722c7410c751da6415666d9d1814f9e913c0804f140475ddbb187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `mongo:4-windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:87ce7a567bb70be160fa781a1f6dedd20b0636beb006e5ec8b775091c66a08fe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2146039484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffda89e37680d564e9032fbdc979ec84464b4889a1b6858d644e2cb2ca92c983`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 18 Jan 2024 23:58:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 18 Jan 2024 23:58:36 GMT
ENV MONGO_VERSION=4.4.28
# Thu, 18 Jan 2024 23:58:37 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.28-signed.msi
# Thu, 18 Jan 2024 23:58:37 GMT
ENV MONGO_DOWNLOAD_SHA256=406d5f9411419c0fbe9174462e2af29760ad32b877845b42ec77592acba02a36
# Fri, 19 Jan 2024 00:01:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 19 Jan 2024 00:01:02 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:01:03 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:01:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f6bd60c23ec6d4454803b2ea199d86440a4ddcbd5057cda4b3a68c6c114e109`  
		Last Modified: Fri, 19 Jan 2024 00:01:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b3baf611a22d340799e9e0e189d9cd0b6a731a401108efdf388d81054e04e4`  
		Last Modified: Fri, 19 Jan 2024 00:01:08 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a8aebd96fa6c06b082052630b8735962538ec7d7ec3bdfc498e63876f2eb689`  
		Last Modified: Fri, 19 Jan 2024 00:01:08 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804a8886b4d15b9d9a7261532e7c582d0df65f8ed027d0017662bc9a462ff41b`  
		Last Modified: Fri, 19 Jan 2024 00:01:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef57236ef48865766caec17b7187a4d99f4883da843ef602e1dbe85a7073f037`  
		Last Modified: Fri, 19 Jan 2024 00:01:30 GMT  
		Size: 245.8 MB (245817734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff73b6d3d2733549d9b1b7eb9fb9f872b93704fc2b8e3ceb426813bbb3aa4ba1`  
		Last Modified: Fri, 19 Jan 2024 00:01:07 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ba833b4d665f8a1944003f7a3625a0a6b2804c904dc3e8d32aaf043211717d`  
		Last Modified: Fri, 19 Jan 2024 00:01:07 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ad182db38ee7d25f8b7d105f45b1ab719a9e82a9a6d8480614f46de6f41e74`  
		Last Modified: Fri, 19 Jan 2024 00:01:07 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull mongo@sha256:894cb5a8005019c39ed2bdaaccfcb09e284a9af22e4e1575fb2122806f73defa
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2315572368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51e317fc89e63b3029f27d86b4f6724c78d7dddf2d2886e1887af347dc6cc89`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Thu, 18 Jan 2024 23:58:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 18 Jan 2024 23:58:33 GMT
ENV MONGO_VERSION=4.4.28
# Thu, 18 Jan 2024 23:58:34 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.28-signed.msi
# Thu, 18 Jan 2024 23:58:35 GMT
ENV MONGO_DOWNLOAD_SHA256=406d5f9411419c0fbe9174462e2af29760ad32b877845b42ec77592acba02a36
# Fri, 19 Jan 2024 00:01:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 19 Jan 2024 00:01:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 19 Jan 2024 00:01:19 GMT
EXPOSE 27017
# Fri, 19 Jan 2024 00:01:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25c543cf49fc04c1850fa7ce2acb3f750a4eb5fec8215a15d292000507ab5947`  
		Last Modified: Fri, 19 Jan 2024 00:01:25 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ca35a87925e5a4c3a54f14b767f3c2cb4eb33ea2d52f688fdde3318822d76dd`  
		Last Modified: Fri, 19 Jan 2024 00:01:25 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebe92b7b486092b66d51f45562fe43a1a2aadfbbf3f60f0e5f37ab6093a664e1`  
		Last Modified: Fri, 19 Jan 2024 00:01:25 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb08bab08de23f3af4801fcdf651f335f932453e8e41d829e0a96bc001065c72`  
		Last Modified: Fri, 19 Jan 2024 00:01:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a078647c5245d73a34de9ce463e8c126c326bb4097da5cf708dc27de8fd18bb`  
		Last Modified: Fri, 19 Jan 2024 00:01:46 GMT  
		Size: 245.8 MB (245840762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6b8d3770e27f866d8380ba6ab5e9fa90ee6464a937cfbca220f4e440bc1aa2`  
		Last Modified: Fri, 19 Jan 2024 00:01:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee41ccc071eb953f0fc8d6710cb202f7a6ae3eb153b8334581db3dcb8665a2e0`  
		Last Modified: Fri, 19 Jan 2024 00:01:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87fa7fab1200b7499633b3b17353aabb1989a7271859db3e29d26eff280b1b37`  
		Last Modified: Fri, 19 Jan 2024 00:01:23 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
