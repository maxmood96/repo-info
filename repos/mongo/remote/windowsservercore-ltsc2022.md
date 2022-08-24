## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:28def291af8cf3fa0aea27ee5680ef329cc31cf81e9e56ef3fe72928b55db323
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull mongo@sha256:eb780ace213935639b0c52fd1d0126a96baa7769980dd8874513551c194adc64
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2827459434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a068a5ef96ae377d29f507455d6d31d4be40947e02f02b57d5fae93ed56d8caa`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 13:33:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 24 Aug 2022 22:20:28 GMT
ENV MONGO_VERSION=6.0.1
# Wed, 24 Aug 2022 22:20:30 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.1-signed.msi
# Wed, 24 Aug 2022 22:20:33 GMT
ENV MONGO_DOWNLOAD_SHA256=999b39df67a77eda3198f8412dc159b0cd8aa6677b901a0cf287921884306ac3
# Wed, 24 Aug 2022 22:22:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 24 Aug 2022 22:22:47 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 24 Aug 2022 22:22:49 GMT
EXPOSE 27017
# Wed, 24 Aug 2022 22:22:51 GMT
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
	-	`sha256:64dd7efca209e774c4a36672309ba8ca7bfb3b19ff678b88b29e8ae6b4a4f6f1`  
		Last Modified: Wed, 24 Aug 2022 22:50:29 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f42c41de4d0146e05d2f121ae0d1f7dcf762c8693c19a905fb57aa4634f226d`  
		Last Modified: Wed, 24 Aug 2022 22:50:28 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3aa1a73ee48e9a6d45d98005c080b190c68e7bcc42f9f07a25113dced65f6c`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8379514e18c1f59e19da84edc7704dd411bdb705b14b9921e1518a2bd6fa91e`  
		Last Modified: Wed, 24 Aug 2022 22:51:42 GMT  
		Size: 510.6 MB (510560384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:619dcf50ea0c5d58a23998106214de32df475d2ef6effc1c7814401d0002063b`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5583d44b6c97384a6373b070c5e5f20890efc1a546cf0d1c46bb3cde19b78`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14524abd86317864e27bbf69b26825dae062a1b7c7989cb60339627c5e2d4c36`  
		Last Modified: Wed, 24 Aug 2022 22:50:26 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
