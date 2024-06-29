## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:03e0fe023b0cc3266ed898f7c1cf2e2a3dbf518c3cf87ed029073b85b799d369
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull mongo@sha256:8f640739539be5ea1d314f483d7c0dfb09e2fb14b3948b7e156465eec4e9583c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2642313913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53cb5d5b79d396e8b74fc002c2ad255138035feb854106118c3788e2d186d59`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Fri, 28 Jun 2024 23:55:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Fri, 28 Jun 2024 23:55:26 GMT
ENV MONGO_VERSION=6.0.16
# Fri, 28 Jun 2024 23:55:27 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.16-signed.msi
# Fri, 28 Jun 2024 23:55:27 GMT
ENV MONGO_DOWNLOAD_SHA256=4a0da9d2a8e7151a2c7c8e68406dce00336f2bb2f6b9f1129184c9888c59e032
# Fri, 28 Jun 2024 23:57:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Fri, 28 Jun 2024 23:57:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 28 Jun 2024 23:57:53 GMT
EXPOSE 27017
# Fri, 28 Jun 2024 23:57:53 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63cedf27ea505d38055eddfbe9b5f3acba94e6081d27526859b52fca5d9841de`  
		Last Modified: Fri, 28 Jun 2024 23:57:57 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebb8f61484a99d2f7108cb19ee365de7335aadd741149dde19eba65561a5b08`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22585d71df7670e551835a7494a79ffe2481db52960df5b7e68da6204f1c5cd7`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a860f283feeeca96f6d40dfc3b44884562d4aa8e00b0996c44732fb652ef6c3`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80842bed74b1ca7aa0c237023a2bd8c7495d6c65015108c39bb794f5fe880f7f`  
		Last Modified: Fri, 28 Jun 2024 23:58:38 GMT  
		Size: 524.1 MB (524114592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7a96954185f83b17cc30dca60cf5f7b6511eef2f17e5924a93a448a2e88616`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf9809035cba6b39019aa12d5e1defa6ec2ddf7db8f48f459e1f3fc2aabd8fa`  
		Last Modified: Fri, 28 Jun 2024 23:57:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4e971bd9569e892af62b870066f253d972a361b8ac080c2cf4bd8f62dcb354`  
		Last Modified: Fri, 28 Jun 2024 23:57:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
