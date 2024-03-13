## `mongo:5-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:7197400fb69e9b5957d7241b2ed105726dacb2f6926f1c840052c6a42fc4cb75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `mongo:5-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull mongo@sha256:3a0da7660bf54eb615f68c4946d5f7cab6d005cf56ca0358d0354635d58bb08d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2273595031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d0dd023ac52efe6f911c455d8e0a1044e388d7126a15429ea1cdec2382e8a2`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:06:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 Mar 2024 00:06:33 GMT
ENV MONGO_VERSION=5.0.25
# Wed, 13 Mar 2024 00:06:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.25-signed.msi
# Wed, 13 Mar 2024 00:06:34 GMT
ENV MONGO_DOWNLOAD_SHA256=65f3fde2ddadbf61dc5895d54670bbbd6febf8b4f7c3a081d1012038452011b2
# Wed, 13 Mar 2024 00:07:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:07:31 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Mar 2024 00:07:32 GMT
EXPOSE 27017
# Wed, 13 Mar 2024 00:07:34 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95e067bd012d81a8b3ca5b457bf5e489340e1933e5dc0b90678db0e849034a81`  
		Last Modified: Wed, 13 Mar 2024 00:07:38 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79e62c7cb840f6acc07d3cec942a95a000a3dbaf812322a7580cd76eae69d2e`  
		Last Modified: Wed, 13 Mar 2024 00:07:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cae990d5e93e58969c84710e1a42ad029d09f623ebfd518ca5d017d1c74e704`  
		Last Modified: Wed, 13 Mar 2024 00:07:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42a0beb6ae9b2d2c9fd6d615cabd0810c1472db223c7332dbfcc99691b6c393e`  
		Last Modified: Wed, 13 Mar 2024 00:07:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17f0b60555018db151505eef3bd5f329de8a7773aa8d96f2589bb8112327d40`  
		Last Modified: Wed, 13 Mar 2024 00:08:09 GMT  
		Size: 316.1 MB (316127003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255ed4f8506b36e4cdec89e71532b46429ac1c89273afd687eb20647ab769b2c`  
		Last Modified: Wed, 13 Mar 2024 00:07:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6fb9e4e7851c7def5cdd0edde2d7c424a387eb7df08ea11dbd7124cd04e6dd9`  
		Last Modified: Wed, 13 Mar 2024 00:07:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:377e1ff22a2b683320fb362c320d53bfc2ec4b7df24764382b3804c111a972f0`  
		Last Modified: Wed, 13 Mar 2024 00:07:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
