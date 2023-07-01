## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:74d09bf21bd28b51238275c1041f09a727ddb0c11ea50ba76decfb363012f8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1787; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:95c6f22ec2e7af02a5c4722fc1a9f7c4c8c7e8bf2bf8fe964e73a8f21e038b28
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1943939131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7db203ec18ecf5a262b98a2a93b335bcd0b7844782e796094e90b4d90bf31f8d`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Wed, 21 Jun 2023 08:51:34 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 02:25:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 30 Jun 2023 23:30:05 GMT
ENV MONGO_VERSION=6.0.7
# Fri, 30 Jun 2023 23:30:06 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.7-signed.msi
# Fri, 30 Jun 2023 23:30:07 GMT
ENV MONGO_DOWNLOAD_SHA256=41dabd0f59813c675f6973201374800b300800060839968b9fda7371423061b1
# Fri, 30 Jun 2023 23:32:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 30 Jun 2023 23:32:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 30 Jun 2023 23:32:05 GMT
EXPOSE 27017
# Fri, 30 Jun 2023 23:32:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0ce49598e7371c2c318cfa408f639c917d1f43843fb9e0a3316db1ba7fbb14db`  
		Last Modified: Fri, 23 Jun 2023 03:10:46 GMT  
		Size: 1.4 GB (1426298723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:369acdd1cf7c4d89f87cf3df6c1a935d83dad0afd57c96dcd7251a04481546a0`  
		Last Modified: Sat, 24 Jun 2023 05:25:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb8d6c89a14c30237871e39cf3fb9e6ebf20a331973fab79d4a7a98714b5b0aa`  
		Last Modified: Sat, 01 Jul 2023 00:31:34 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c254845ec47c413241173bdf59339bc56c2dd26a30308558c9c0f9fc6fd48cde`  
		Last Modified: Sat, 01 Jul 2023 00:31:33 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2c2d139fff533ed1908f21e68492f9ec30f537caf88bb70379859b9abab3fa3`  
		Last Modified: Sat, 01 Jul 2023 00:31:32 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc860035266b47b92d958e403fc6c52ca1dcfdabf7e94dee077874c00d9b7c2`  
		Last Modified: Sat, 01 Jul 2023 00:32:51 GMT  
		Size: 517.6 MB (517630677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7705f73643deac226b5539bc789b822605f98879a0832121274cea3734f5bac1`  
		Last Modified: Sat, 01 Jul 2023 00:31:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c62323e440122f72ec31fff1e4654cda6fe3c1517f6bd45c052d044abd5bce5`  
		Last Modified: Sat, 01 Jul 2023 00:31:31 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b844def3e97542d3e176c0103a4fee6b482a10366c7c7dc17399038577cd3938`  
		Last Modified: Sat, 01 Jul 2023 00:31:32 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
