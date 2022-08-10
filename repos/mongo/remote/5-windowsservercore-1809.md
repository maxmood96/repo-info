## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:ba3e3e04ac8714c04207a35bdf98dc78ffec1c8b9e28368bb3346bbcce3b7bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull mongo@sha256:bcf43907ccebcf71d49b118e4e8f1e048ad5463985e6d471e79b7b372fffec3c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2985903984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3618c094006b3aaa0684aa5fc3db1333f51d0c8e9a76a84ab74960b697cf2be0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 13:44:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Aug 2022 18:18:56 GMT
ENV MONGO_VERSION=5.0.10
# Wed, 10 Aug 2022 18:18:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.10-signed.msi
# Wed, 10 Aug 2022 18:18:58 GMT
ENV MONGO_DOWNLOAD_SHA256=5feeaf02c6a1a9125565de2e3e44a6c11d920427db31d2ef3b516e2832dcff9b
# Wed, 10 Aug 2022 18:21:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongo.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Aug 2022 18:21:05 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Aug 2022 18:21:06 GMT
EXPOSE 27017
# Wed, 10 Aug 2022 18:21:07 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:da71148bcd96afa7027d6172acee93aad6002bfbe87cadf468260667c09b3a89`  
		Last Modified: Wed, 10 Aug 2022 15:05:54 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d000d409b0c20e6ed52ccc332cfba1c8ae7a69df54fc78c122816419e86e1ae`  
		Last Modified: Wed, 10 Aug 2022 18:52:57 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea827f4a68208178e83cd57647defeeb7f040c0a69d14dc5708f755560e1c33`  
		Last Modified: Wed, 10 Aug 2022 18:52:56 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6936957f917fde2ed8b116a4d7cca6869057da7ba74cd2716bfe87e37d8e61be`  
		Last Modified: Wed, 10 Aug 2022 18:52:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca21056c7818e683a0ade00d3a00e1ca5e05df68ad7219e94999b89847aa1150`  
		Last Modified: Wed, 10 Aug 2022 18:53:46 GMT  
		Size: 308.2 MB (308181285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b92a6a429dc44c98385948197a7b7be913c5d27bf78fb59eb44e0de78fce845`  
		Last Modified: Wed, 10 Aug 2022 18:52:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1de289bef0e3bce3d04806858eda60ea6916eaa4e9bf5675d8727fe4da0c6e`  
		Last Modified: Wed, 10 Aug 2022 18:52:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03b13d3ccb392e6df64fb0ad6b61fa92294d4a1b14989538aa0ba45f0151d3d`  
		Last Modified: Wed, 10 Aug 2022 18:52:53 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
