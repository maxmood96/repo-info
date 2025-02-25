## `mongo:7-windowsservercore-1809`

```console
$ docker pull mongo@sha256:b0bde1a026744e532e6dcf4d8ef11d997a0b848c3e0c5ef5284cc3d60d346412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `mongo:7-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull mongo@sha256:95e3ad61e914fb21069287f48e3c510ebac855b1098d0ce27b2730d94a755033
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2749458202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4733623c532b3149731c485160d6e708feb940d0d20b23a9e75fb528e3bf6a3b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Tue, 25 Feb 2025 01:32:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 25 Feb 2025 01:32:35 GMT
ENV MONGO_VERSION=7.0.17
# Tue, 25 Feb 2025 01:32:35 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.17-signed.msi
# Tue, 25 Feb 2025 01:32:36 GMT
ENV MONGO_DOWNLOAD_SHA256=4e289d657aea36ecac5fa05a5d82cd1cc377efd75f682a2126ac6473d3a22d12
# Tue, 25 Feb 2025 01:33:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 25 Feb 2025 01:33:59 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 25 Feb 2025 01:34:00 GMT
EXPOSE 27017
# Tue, 25 Feb 2025 01:34:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fee8ec9b4aa77bfdbfa11a8f1d11f05367012dcfa653e0993a45fb232038bc4`  
		Last Modified: Tue, 25 Feb 2025 01:34:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222002ea51bd5d8d052d04d27b37b5d07ffeb6c706d52731e16c76942af27ee2`  
		Last Modified: Tue, 25 Feb 2025 01:34:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7cdd4471ea1c6d73fada3d317e05d35bce03c5b7a2a284027f385c4062783a`  
		Last Modified: Tue, 25 Feb 2025 01:34:06 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc29d0a5ce3233d032c38c8fc2c74dc496384cb7914dd6c3db04ead54fe02c6`  
		Last Modified: Tue, 25 Feb 2025 01:34:05 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb55773d6fc38cb7a96c7516a42822b2ef13fdda097b82c749d1452792325de9`  
		Last Modified: Tue, 25 Feb 2025 01:34:54 GMT  
		Size: 612.5 MB (612540350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4af10a9c2d5bf92db810d21d5d3785d76a6c92972e60a3918138c330f3b492de`  
		Last Modified: Tue, 25 Feb 2025 01:34:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d5b5b3a40e655a29f8eb2a441b0aa5ea6e2462a90292b23943564420441937c`  
		Last Modified: Tue, 25 Feb 2025 01:34:05 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a646a34e85d41ee57d11ad268ecf56e3c3a7c620d40d292a47c87507f2e3176f`  
		Last Modified: Tue, 25 Feb 2025 01:34:05 GMT  
		Size: 1.3 KB (1274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
