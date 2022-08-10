## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:8a09f6818013cfc92fb3b3bde9c9a39c20ef06ea609c592ef619150d5eb5554d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull mongo@sha256:0b5ce0487bd821fba60c6a5e326c6b11e62f0b6235f2b5280a455449da6ec951
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2625315716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38a008f6aa6545cfe415a3538ab965f73690ac3a0f4de4d1bae5af11194fd1c6`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 13:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 18:17:14 GMT
ENV MONGO_VERSION=5.0.10
# Wed, 10 Aug 2022 18:17:15 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.10-signed.msi
# Wed, 10 Aug 2022 18:17:16 GMT
ENV MONGO_DOWNLOAD_SHA256=5feeaf02c6a1a9125565de2e3e44a6c11d920427db31d2ef3b516e2832dcff9b
# Wed, 10 Aug 2022 18:18:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Aug 2022 18:18:43 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Aug 2022 18:18:44 GMT
EXPOSE 27017
# Wed, 10 Aug 2022 18:18:45 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ff9b89cbdb5f88cb926263140643eb2bfad61fb092119830e290c8f8ff711c8f`  
		Last Modified: Wed, 10 Aug 2022 15:05:31 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e64d0e88767877ceca6b0591d8eb47280dc873f332aeb3abd054e02cb6b4ff`  
		Last Modified: Wed, 10 Aug 2022 18:51:37 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:442571a80c8dc53fbce6b88a7fd1a1e66b6d2c1a3b8c25a8933795db453951d2`  
		Last Modified: Wed, 10 Aug 2022 18:51:36 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423ee96e6534948f66b36d13643818768b77d283694e87a2f92e0c6127b9572c`  
		Last Modified: Wed, 10 Aug 2022 18:51:33 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84a22df0fbf3eb9b5cea82c70861ace6e11ec03b004f98e99ca1855033733cc0`  
		Last Modified: Wed, 10 Aug 2022 18:52:29 GMT  
		Size: 308.4 MB (308416699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbfe58e998ba9acdfc945d58da78bd25624edfdcd07807852f3cdd6deecca73`  
		Last Modified: Wed, 10 Aug 2022 18:51:33 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306cdef8bbe3b39478586ea07544bdc2ea572a96411b018735fa7d8c83574ab6`  
		Last Modified: Wed, 10 Aug 2022 18:51:33 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:606a4f2afa7c2bd2ae0937c8660665bea6824c991b7432b1c63f581ba9d9530a`  
		Last Modified: Wed, 10 Aug 2022 18:51:33 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
