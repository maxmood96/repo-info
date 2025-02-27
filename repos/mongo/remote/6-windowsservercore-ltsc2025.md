## `mongo:6-windowsservercore-ltsc2025`

```console
$ docker pull mongo@sha256:1ec88665ad186baf0a5f506252521071eb524547c76ca967c6da54fd4cc57ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `mongo:6-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull mongo@sha256:c1a683605dbe74924db1575ba148a902295091011c1be867dfc442820277efd2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3343646749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aa208a6c79806fbe2b120ea3e0111380724b244019e1bfd8c8e2fc30668e9c6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:18:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 27 Feb 2025 18:18:56 GMT
ENV MONGO_VERSION=6.0.20
# Thu, 27 Feb 2025 18:18:56 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.20-signed.msi
# Thu, 27 Feb 2025 18:18:57 GMT
ENV MONGO_DOWNLOAD_SHA256=518cf974540402bd2992996372d29dd13912e2662d2288649e7984ed091a5e5c
# Thu, 27 Feb 2025 18:20:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 27 Feb 2025 18:20:07 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 27 Feb 2025 18:20:08 GMT
EXPOSE 27017
# Thu, 27 Feb 2025 18:20:09 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c7cffb015dd0bbc3cb3a6bdc87583003ced666c7e884ed5d90402622e140459`  
		Last Modified: Thu, 27 Feb 2025 18:20:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d901324cd787cd8f256160071a7b8aecdd52d54d30791beec72599d522cf89`  
		Last Modified: Thu, 27 Feb 2025 18:20:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9306133314e40c122488f73fe40333f6d1cc8e0a15e5f2a4a163f204ab0a01`  
		Last Modified: Thu, 27 Feb 2025 18:20:14 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4aef4b609292cace1760d0f02a5bb3962ab816fed260ba45ff3d124d95142f`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6ecc7f892abcefca956b11f83f3debccce1f727f850d97e18c006d45499974`  
		Last Modified: Thu, 27 Feb 2025 18:21:02 GMT  
		Size: 527.0 MB (527049985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec70e518058761a833b4fd94b0a00132397e5a00987ea78a2b1ac707c2b4cb9b`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf30942b85f4b5a03323c46d30cc861d44fc53479f5985dea086be1d3e5a813`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f060071df79fddf203fa976dfea6656f2ba912962065986b16f9d35b0dc31f9a`  
		Last Modified: Thu, 27 Feb 2025 18:20:12 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
