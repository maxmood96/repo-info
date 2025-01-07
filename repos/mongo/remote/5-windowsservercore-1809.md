## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:4e2449b67bbdeb8f4718cf59778c046d5f7e9dc7edcbea7bd37e584c433badff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.6659; amd64

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
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
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
