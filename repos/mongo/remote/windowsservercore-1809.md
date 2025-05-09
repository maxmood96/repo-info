## `mongo:windowsservercore-1809`

```console
$ docker pull mongo@sha256:e3255abbf3483a267b34dec7af0e2f5c380b9d5d0a0527ff74d9bfe6e611ae5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `mongo:windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull mongo@sha256:ffd4fd8061fe7864dfb7af18a18a524a8079ac59fb2bf6c5575eedfdd6af8abd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2939031103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f07a1f6f17950ecfba01f2cc57df1e8e309047a4b1f4f445645b2c9708b6ff8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Thu, 01 May 2025 22:27:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 01 May 2025 22:27:47 GMT
ENV MONGO_VERSION=8.0.9
# Thu, 01 May 2025 22:27:47 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.0.9-signed.msi
# Thu, 01 May 2025 22:27:48 GMT
ENV MONGO_DOWNLOAD_SHA256=4acf24592a7658cc58b4293cbf0a3f42133c9c1d4f2234f1a249f74aa1c7d22a
# Thu, 01 May 2025 22:31:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 01 May 2025 22:31:10 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 01 May 2025 22:31:11 GMT
EXPOSE 27017
# Thu, 01 May 2025 22:31:11 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:258de7be8acc97d1226a3162840f8a807fb62a678b7514644a54a4badcb97e38`  
		Last Modified: Thu, 01 May 2025 22:31:15 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196c7dc57c27b6a4c68a74274af66a5c682ff5a8b320edc3a6b25769ba60974f`  
		Last Modified: Thu, 01 May 2025 22:31:15 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0798b44dadd77f2e5bb274203994fe57b21283891c7bdc7f6e0c3df6c7d5b098`  
		Last Modified: Thu, 01 May 2025 22:31:15 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c25021e3f57db7736128f272f1f529487909bd8709eebbdd8e630527839f1db`  
		Last Modified: Thu, 01 May 2025 22:31:14 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5fb2f7b46ba2ba952875271d296e67735ecb3de3e65d32af64cb93dd90ad78`  
		Last Modified: Thu, 01 May 2025 22:32:14 GMT  
		Size: 773.5 MB (773495787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bc983a66680377183653e75011df2c811fbe0486ea51feaaba47aa1adc72ab7`  
		Last Modified: Thu, 01 May 2025 22:31:14 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e76ccfcca0c27cf3fb11d0c23be73c9b68519aa168c8848fd06191e39b518dd`  
		Last Modified: Thu, 01 May 2025 22:31:14 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a55f3f7d938f160731c9acb2f6ef87f0e4878cddc8f5aadb7cc0cc57ec9ea25`  
		Last Modified: Thu, 01 May 2025 22:31:14 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
