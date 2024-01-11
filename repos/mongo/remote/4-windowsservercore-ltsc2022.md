## `mongo:4-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:fe987e9e22baf45567f6b0ee11af0a4725ebf61fa880d4bb16b562d3808502a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `mongo:4-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:ce85c5260f9131564b95e045a6daae879e04eab8dcb9976edea9dcb206960a07
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2146399186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e8f71317bc02ee35cec5c8144ca08d0b0d33a73defe4e3e0e61b7b524df949e`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:02:52 GMT
ENV MONGO_VERSION=4.4.27
# Thu, 11 Jan 2024 00:02:53 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-4.4.27-signed.msi
# Thu, 11 Jan 2024 00:02:54 GMT
ENV MONGO_DOWNLOAD_SHA256=ab6b645db3ec289fb199a5ee2e1d99704add3fb9e801ebe4d87158eb2716aeb4
# Thu, 11 Jan 2024 00:03:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:03:48 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:03:50 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:03:51 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb4bf8f745808cffd1989f0f834d490e4fb0cccc95fd38d6c8ab536bc7fdfa0`  
		Last Modified: Thu, 11 Jan 2024 00:03:58 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bab618b86153d35db38da850130d14bcb6eeac51b980b92c0917829253d876c`  
		Last Modified: Thu, 11 Jan 2024 00:03:57 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d700e3c11e39d71ac056c0754c612b4dd6557d16b534e7058fca827a7853a0b`  
		Last Modified: Thu, 11 Jan 2024 00:03:57 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e6439faed54e0e6e7cc8a27172ae011f9ac8ab46f4ce7a9b6638f34cba9ea95`  
		Last Modified: Thu, 11 Jan 2024 00:03:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41080ac0a22b915fe44e5bacfcd8e273b2051605ea141ed1a5773b2cc3f4fbd2`  
		Last Modified: Thu, 11 Jan 2024 00:04:21 GMT  
		Size: 246.2 MB (246177436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc7af7e2e92549239cd2189abc7bc5b680946b3a7d14f10cdad60435bd6fa72a`  
		Last Modified: Thu, 11 Jan 2024 00:03:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a877ce2a07af500b29b06062a79c327d8bb3cc5b65bcb959b9f987f1d983c434`  
		Last Modified: Thu, 11 Jan 2024 00:03:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7c468f4378a6a7ccd71b4446ae05f31a19081bdaf4d258a3b9e7a90bbdbb2e`  
		Last Modified: Thu, 11 Jan 2024 00:03:56 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
