## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:22c05d31cec697fde069c1d168e8430dda0d935c5743c70108b27cb2d6e1d52f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull mongo@sha256:6b6fc85583e79d9ebcc51c7ccd6bf0ef4f9e820a93a62fc162ed4acbbc01b3d0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2882456907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a331d251925348a4af1eff87a132d96e9f9c9f2f7bbf608a6f85adc4e1c2431f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 19:04:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 12 Mar 2025 19:04:56 GMT
ENV MONGO_VERSION=7.0.17
# Wed, 12 Mar 2025 19:04:57 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.17-signed.msi
# Wed, 12 Mar 2025 19:04:58 GMT
ENV MONGO_DOWNLOAD_SHA256=4e289d657aea36ecac5fa05a5d82cd1cc377efd75f682a2126ac6473d3a22d12
# Wed, 12 Mar 2025 19:06:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 19:06:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 12 Mar 2025 19:06:15 GMT
EXPOSE 27017
# Wed, 12 Mar 2025 19:06:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:818c6589114883d9608e7f6065d2c7a2499bb981854b4718ed0fd45d363f1c98`  
		Last Modified: Wed, 12 Mar 2025 19:06:22 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63f112f3e9de2b71c3c122b196414ab56617e68ee58831529c6f5661b54d1b42`  
		Last Modified: Wed, 12 Mar 2025 19:06:23 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa930a69b3d2efb696a57f670e27fb5b30d6da5dcb7a7f9e679b03379d4100aa`  
		Last Modified: Wed, 12 Mar 2025 19:06:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b874177f51169cc79ef03bf750cdd9287e987661b1b780f438ff29234efd5`  
		Last Modified: Wed, 12 Mar 2025 19:06:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ffaafb3b279a3a2d09dfe77826b6a8108ff090bbc545c957a9dddaf123fcf1`  
		Last Modified: Wed, 12 Mar 2025 19:07:13 GMT  
		Size: 612.5 MB (612506705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8de71033eb92680ec18c17e2b72529b7380ad2408f25d29ebb3b9c5c2aa55d4`  
		Last Modified: Wed, 12 Mar 2025 19:06:21 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f96621ebcc05d83d68ecb43223b4a4480e031b5dc2abc8a645cf026188e9b2`  
		Last Modified: Wed, 12 Mar 2025 19:06:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ec3e055fe646dfb1db733f1ec0dec5dc96dceeb55da1df8d646311d05a2441`  
		Last Modified: Wed, 12 Mar 2025 19:06:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
