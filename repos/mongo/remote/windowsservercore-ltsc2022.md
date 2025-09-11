## `mongo:windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:1abe2672bf38c292361ce7ab0fd68c4931f2127bbaa954dabd32deb83ccb8bce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `mongo:windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull mongo@sha256:6a8d394587e111b864815ae9ab4bcef8b27eb0761b8fb07862098759da2d09d7
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3063408160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f66167123271aa3a448447dba0e35b90e1d82f3ee669900d8512b19e867070a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 21:49:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 10 Sep 2025 21:57:19 GMT
ENV MONGO_VERSION=8.0.13
# Wed, 10 Sep 2025 21:57:19 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.13-signed.msi
# Wed, 10 Sep 2025 21:57:20 GMT
ENV MONGO_DOWNLOAD_SHA256=f301e2272fb222bf53b76883bbf95d07c54b116ad1e9e694234f002ad9abd0c4
# Wed, 10 Sep 2025 21:58:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 10 Sep 2025 21:58:55 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 10 Sep 2025 21:58:55 GMT
EXPOSE 27017
# Wed, 10 Sep 2025 21:58:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49765463c3d7d25619af165e8e9076efeb241b48967d5848f54537626c1e6386`  
		Last Modified: Wed, 10 Sep 2025 21:53:47 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2474f02a9e7c8941faf9bd97fe771b9a7ed7d17a8285e4b19312d5d0d4f8cfa2`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c036414891835c781dc73c856764ec587f7476ec7f55898a49d254dfa7fe90`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d443dc3d66fd7eaebe348446fb89e80efb84cf10a57b258913f2dd2de4019eb5`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d37c22f6d577f063c7615a6ae5af992eba34ce743228eafd44ae64a12a974f`  
		Last Modified: Wed, 10 Sep 2025 22:21:08 GMT  
		Size: 781.3 MB (781253986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27b326cab81aa625046008fb51a9422621658d3d4406f556c84042a4c63afa40`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba599e88fedc3ed5fd53d60025748338a59c3836545eb42eea61443f75fa05c`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:432d7db081762c31b02c1b6fb7d0dbff9b50a30bedd36adc6920daa18c34e002`  
		Last Modified: Wed, 10 Sep 2025 22:00:30 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
