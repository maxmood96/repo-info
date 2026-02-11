## `mongo:7-windowsservercore`

```console
$ docker pull mongo@sha256:d3921c4016d0261efacc807d01b461ccf6db53069ee321a32a762d8c2d3fcb8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32230; amd64
	-	windows version 10.0.20348.4648; amd64

### `mongo:7-windowsservercore` - windows version 10.0.26100.32230; amd64

```console
$ docker pull mongo@sha256:b27b3f72b6dcd43cef9fb3a68d0e4ecb0ad02ed817f00fcadd107f5807cfcf9d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2115293074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1feba4880cd34c4878dde3ff24ff6d257cc01c6d387d9281ed19fff6eadbf01c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Tue, 10 Feb 2026 20:08:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 20:08:32 GMT
ENV MONGO_VERSION=7.0.30
# Tue, 10 Feb 2026 20:08:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.30-signed.msi
# Tue, 10 Feb 2026 20:08:35 GMT
ENV MONGO_DOWNLOAD_SHA256=bfdcc24c27082a220867a139aad04d734eead0f85e8caacef135bb2a4810f9cd
# Tue, 10 Feb 2026 20:10:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 20:10:50 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 20:10:52 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 20:10:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d6db8aeaf4baa0c63fed6cbe7a5c79a58adaf8785da6d48e7d057054c6612ae`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55cde9f39c63c39fadfba8b211ad603f933075901cc233e1dd1b0f801301b44b`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ad094cd7fa71f697ec3925996971f05d217342ba57ecd9d4e3bbf26b84479b`  
		Last Modified: Tue, 10 Feb 2026 20:11:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc27bedca6dd6cad91b259c21865b0b082788bd8beaa0e97150dd90d27322b5e`  
		Last Modified: Tue, 10 Feb 2026 20:11:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b7de25763b49b27d4d903491c673b9d6af5b236b855e6ff93cafdbb7a5708b`  
		Last Modified: Tue, 10 Feb 2026 20:12:07 GMT  
		Size: 619.5 MB (619523609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ec8c368640eae4ec8029e1b56f4101517899582cd09eb37917d44875a4b292`  
		Last Modified: Tue, 10 Feb 2026 20:11:06 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf88bd8b8f27c81600119299f9910e05def1a21c74838009567ac2fcd0aad66`  
		Last Modified: Tue, 10 Feb 2026 20:11:06 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99c191d60103ffff2d7f248615bfe496cba32595b6d57bd306e862025c4df2b`  
		Last Modified: Tue, 10 Feb 2026 20:11:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:7-windowsservercore` - windows version 10.0.20348.4648; amd64

```console
$ docker pull mongo@sha256:b27a6b4600593c8222debb703fbd3ea084f57a53fb70c21aee7762cc8cce2b11
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2455321329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e9cf8f5ab9e96bd7a96af94631d44e4a76e3a6be8db22141d5a5a1d37c9d3a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 10 Feb 2026 20:30:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Feb 2026 20:30:14 GMT
ENV MONGO_VERSION=7.0.30
# Tue, 10 Feb 2026 20:30:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.30-signed.msi
# Tue, 10 Feb 2026 20:30:15 GMT
ENV MONGO_DOWNLOAD_SHA256=bfdcc24c27082a220867a139aad04d734eead0f85e8caacef135bb2a4810f9cd
# Tue, 10 Feb 2026 20:34:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 20:34:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Feb 2026 20:34:40 GMT
EXPOSE 27017
# Tue, 10 Feb 2026 20:34:41 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:19:49 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0214f37800630b733a97dce03888c3b8b806ebaae5e7c13cfc84abe540ffe5c`  
		Last Modified: Tue, 10 Feb 2026 20:34:55 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80878449b1e5a8ccc8c076bdeb13b4c309fd5718d03cda748d291e4f9a87ef0e`  
		Last Modified: Tue, 10 Feb 2026 20:34:55 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100bed44038aceca69701dda3a4a705eff5dd93167dd8b477cf23c41b66a2afc`  
		Last Modified: Tue, 10 Feb 2026 20:34:55 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:801ec8937146dba08c611dc71af56db392bf148b3af2fa1460294afc887ea61b`  
		Last Modified: Tue, 10 Feb 2026 20:34:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22c3cc867f7745f76f051952324bc8ece9c45e3da94056d0e3b8f32cd5900546`  
		Last Modified: Tue, 10 Feb 2026 20:35:53 GMT  
		Size: 619.7 MB (619652956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05672765d1da2f714e8a67678e06ab5cfa9dad55765bf1648c3de82204be184b`  
		Last Modified: Tue, 10 Feb 2026 20:34:53 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03dfb0d0e4624f15c99b10af976401ca7b60f4fa1ce997dc24bdf026a6df207`  
		Last Modified: Tue, 10 Feb 2026 20:34:54 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83398db7f2343ac8158bb7a160494da317e8fd4b98734cfd405a048cfd72edee`  
		Last Modified: Tue, 10 Feb 2026 20:34:53 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
