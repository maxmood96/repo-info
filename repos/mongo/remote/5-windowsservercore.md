## `mongo:5-windowsservercore`

```console
$ docker pull mongo@sha256:a056a37db8ffab1f2777b205fff5f098f7351f1c0f934da8bc44cfdb79d18f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2966; amd64
	-	windows version 10.0.17763.6659; amd64

### `mongo:5-windowsservercore` - windows version 10.0.20348.2966; amd64

```console
$ docker pull mongo@sha256:07e1297850df884e52f7e1a6b25967ac28ff8a843d37c75225f777c9ee8ec24a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567263775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94246bf35bfb6c5af761b1163d7e05333e6c46ba5f296d7dee153a7d34626a7b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:39:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:39:12 GMT
ENV MONGO_VERSION=5.0.30
# Wed, 11 Dec 2024 20:39:12 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.30-signed.msi
# Wed, 11 Dec 2024 20:39:13 GMT
ENV MONGO_DOWNLOAD_SHA256=acabc07cba2e1b4a8bc2a852715a21ca29cae0f08a0dc157d54c1049f586fe45
# Wed, 11 Dec 2024 20:39:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:39:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 20:39:55 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 20:39:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2df3558b34df995cffeece81ee91e9e5f79722e5cb6731965876cd84b6092c8`  
		Last Modified: Wed, 11 Dec 2024 20:40:02 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d66768fc9fb85f49440733638ad03a099008af17c6ffcef31e9892b6acf7ae8`  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d36754eed9e6f7e68b4cab6721f45ea65dea096027d71502cd88ec4c75a3fca`  
		Last Modified: Wed, 11 Dec 2024 20:40:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99f28dfc33d6df945b393df6098a2ccd1658839e6aa330711bd86fc645e4dc52`  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6de970fa26cb95c601ef71963cafb133a7cb6398708134cd35114f4823334a5`  
		Last Modified: Wed, 11 Dec 2024 20:40:30 GMT  
		Size: 313.4 MB (313381159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0937e8808b14bf185095f2e060220eb4b9f4d8b14cd373c8575974fcbe03bca8`  
		Last Modified: Wed, 11 Dec 2024 20:40:00 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dd8cfa1333b1c76b05e981a582034ab8f9b9471a09723307ab42db83cce3bd8`  
		Last Modified: Wed, 11 Dec 2024 20:40:00 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71621aae74e37518756b4aa6c7dc4a585ebf20b55ee2824496aa964400622974`  
		Last Modified: Wed, 11 Dec 2024 20:40:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull mongo@sha256:363d069647be65e68da9e23c8ae8212789762a45e3de93e35d4d01eecbcb77b4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327705401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76086c04b94614775522d4f6bd00721b9bb089694a03084dbb4d010cca97f79a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Wed, 11 Dec 2024 20:44:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 Dec 2024 20:44:31 GMT
ENV MONGO_VERSION=5.0.30
# Wed, 11 Dec 2024 20:44:32 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.30-signed.msi
# Wed, 11 Dec 2024 20:44:33 GMT
ENV MONGO_DOWNLOAD_SHA256=acabc07cba2e1b4a8bc2a852715a21ca29cae0f08a0dc157d54c1049f586fe45
# Wed, 11 Dec 2024 20:46:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:46:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 11 Dec 2024 20:46:03 GMT
EXPOSE 27017
# Wed, 11 Dec 2024 20:46:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5c02ad4669cdbafd6c74a1aa59aeffa9999e6e902762621c45d1d2592989b5`  
		Last Modified: Wed, 11 Dec 2024 20:46:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c935b859ab340107e48506a667e7b476b1d48d1e67fd9890939c4208c2a117`  
		Last Modified: Wed, 11 Dec 2024 20:46:12 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7321368db53f0e22d2f7d2625c1c12b4716dcd3920a4da33038782b413b3e5bc`  
		Last Modified: Wed, 11 Dec 2024 20:46:12 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39174507c7f54a643e5a757897db7858804e0bb3b051c7814221ada748075d29`  
		Last Modified: Wed, 11 Dec 2024 20:46:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5380f7ba49f7c786b5d01058f1d46d99ef6b184ad18844fc21ed8384778bfca`  
		Last Modified: Wed, 11 Dec 2024 20:46:41 GMT  
		Size: 313.5 MB (313526099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8381e4b77c6776c2aee44bca56d7ca462da8b917a6babe5c52de2e837b87a822`  
		Last Modified: Wed, 11 Dec 2024 20:46:11 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d837e090cf344cb87462db6c8f9c7b1a4c27ebd071d9ad75890700514b35168a`  
		Last Modified: Wed, 11 Dec 2024 20:46:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dbb7c131b7606ca813f75f5c6aad8349dc4404be9e4b497fe3d201d22241d19`  
		Last Modified: Wed, 11 Dec 2024 20:46:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
