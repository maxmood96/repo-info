## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:d83496581700596cd5d203c9de11cfcdfd3938ff9951bbcd18f6fd3872a17c5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1607; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.1607; amd64

```console
$ docker pull mongo@sha256:fc77df164b0e7a939ea74ba8176ffb3b0f6ccf98e99375674a90865c757cb72b
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1959896518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad371dd947176b5d9dd4694f784e8c181bce58c56022c2d1836ce610c77ed7f0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Jan 2023 23:47:40 GMT
RUN Apply image 10.0.20348.1487
# Fri, 10 Mar 2023 06:37:36 GMT
RUN Install update 10.0.20348.1607
# Thu, 16 Mar 2023 02:55:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 16 Mar 2023 03:20:45 GMT
ENV MONGO_VERSION=4.4.19
# Thu, 16 Mar 2023 03:20:46 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.19-signed.msi
# Thu, 16 Mar 2023 03:20:47 GMT
ENV MONGO_DOWNLOAD_SHA256=91e83f2fc3ddd3ab0bb170d26b89d80e4268a563deee6ce72313de5774875f08
# Thu, 16 Mar 2023 03:22:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 16 Mar 2023 03:22:51 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 16 Mar 2023 03:22:53 GMT
EXPOSE 27017
# Thu, 16 Mar 2023 03:22:54 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:1a65b089bc835b0c3700397b1935e97cf469b0891bb4de3942c8dfbe4b672d47`  
		Last Modified: Thu, 12 Jan 2023 02:33:52 GMT  
		Size: 1.4 GB (1386029089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c921d7eac594f5e3ce3ef10adb8fd0f71bdbb713c4854336b995d25f89c44d42`  
		Last Modified: Thu, 16 Mar 2023 01:41:04 GMT  
		Size: 327.9 MB (327911088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d31bb6c06d038a3e1a69943be5f72e0ad656773c3f446d934ff816b71b0d631`  
		Last Modified: Thu, 16 Mar 2023 03:42:14 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0256cabc1a5102e77256417617198ad096b730aa15036f8e1c4bca4f26d30582`  
		Last Modified: Thu, 16 Mar 2023 03:54:27 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7daef9b52b9d6a3b860107a5e71e2fd91d5fb880dcca8a9e1330859f51e49c54`  
		Last Modified: Thu, 16 Mar 2023 03:54:27 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faea37820a0c4259f6de1c9905d618306b88ef707edad7c0e9bd1a4c36ff7d97`  
		Last Modified: Thu, 16 Mar 2023 03:54:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1955042e36e847da78aa3af8100333cb436061f54222c13e0fb38c9b090d2b04`  
		Last Modified: Thu, 16 Mar 2023 03:55:16 GMT  
		Size: 245.9 MB (245947031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d10c50aab4dcdcb5c62a1a85e105ba437e30e017a90c4b30c818b4cd08058df`  
		Last Modified: Thu, 16 Mar 2023 03:54:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df6b4d2a6fe54c785070112b54a04228395dacbc38692981228e5534295f23f`  
		Last Modified: Thu, 16 Mar 2023 03:54:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d36fae56c0c350a17017d996d1b7d82fd4a667e63e3fb6f38cefbbc0c58ea4`  
		Last Modified: Thu, 16 Mar 2023 03:54:25 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
