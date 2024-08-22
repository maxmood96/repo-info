## `mongo:6-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:d678fcdebe8f798a7fd187e826e5aac7bfcf4bdce329773f8ff5e50c5200a8b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `mongo:6-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull mongo@sha256:349ae3448d817118ff177bd1006516495cf741de91791996f657314617bcea95
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2666544330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01f543e88a1620ed0fa8f89dab53a4390c65c62b0673a119f1c77c1a8606c7bf`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Thu, 22 Aug 2024 01:04:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 22 Aug 2024 01:04:11 GMT
ENV MONGO_VERSION=6.0.17
# Thu, 22 Aug 2024 01:04:11 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-6.0.17-signed.msi
# Thu, 22 Aug 2024 01:04:12 GMT
ENV MONGO_DOWNLOAD_SHA256=90c6014610d9351763c59985460c915bb87227ecea619cb2d93e962787b87cc1
# Thu, 22 Aug 2024 01:05:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 22 Aug 2024 01:05:18 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 22 Aug 2024 01:05:19 GMT
EXPOSE 27017
# Thu, 22 Aug 2024 01:05:20 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a8315f53301084b43a50318487428ca5804096081244b2aa9b7cbebc1f31b7`  
		Last Modified: Thu, 22 Aug 2024 01:05:23 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7988fbee27a64204e4962eefb401f4554c5e894de2befa9451c0a6337151e497`  
		Last Modified: Thu, 22 Aug 2024 01:05:23 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8daebc6bc8f8d5477f8a442183fdfc0f842e9301456d047522ba9307a4281c3`  
		Last Modified: Thu, 22 Aug 2024 01:05:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbb8faddfae033ef0791993f71833d6048528302807fe9211b107cd3116e5074`  
		Last Modified: Thu, 22 Aug 2024 01:05:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d36438aca96357a052a4695edb33eef97a0c7587919c6fe565d102a59216ac9`  
		Last Modified: Thu, 22 Aug 2024 01:06:10 GMT  
		Size: 524.8 MB (524770346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727f04d0e83791c87e9ff41e838c98b29a21720a7366b32b66b2566e189f62ea`  
		Last Modified: Thu, 22 Aug 2024 01:05:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:729ef3e33cc52071d566589968f3748e3f55dd73f32e5c9b0ebfdb0450966461`  
		Last Modified: Thu, 22 Aug 2024 01:05:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a618985ad7f72b88373f3b3d54736015dd9c48a2523a97012e6492eda5d6228`  
		Last Modified: Thu, 22 Aug 2024 01:05:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
