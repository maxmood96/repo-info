## `mongo:5-windowsservercore-1809`

```console
$ docker pull mongo@sha256:2c57587302aa21b0b9e000732f687f700c8aff19611af72dc81629e0c2511bca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `mongo:5-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull mongo@sha256:df40d312d57f336bfe20626e23ffca780e08ac6e53e7906c51e8a59370ea0bf2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2558538729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a7f0dd80f9b16e2f59296a7bcf9241c3698ffb03094f06f694ab52af145f23`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:19:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 13 Aug 2024 20:19:49 GMT
ENV MONGO_VERSION=5.0.28
# Tue, 13 Aug 2024 20:19:50 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-5.0.28-signed.msi
# Tue, 13 Aug 2024 20:19:51 GMT
ENV MONGO_DOWNLOAD_SHA256=db9caacfb85f9f37f7621759d0fad008b9d575c9974bf3e25fa0d4b243000e89
# Tue, 13 Aug 2024 20:21:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=Client,MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:21:32 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 13 Aug 2024 20:21:34 GMT
EXPOSE 27017
# Tue, 13 Aug 2024 20:21:35 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ced34c34bf975d27f35b685137d9dff87024646f6b9f753c0fd967e6f7bf4`  
		Last Modified: Tue, 13 Aug 2024 20:21:39 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208c43d24908f6c16b857a6adef09d5984a94e2a45f81be6060d787a33f222d8`  
		Last Modified: Tue, 13 Aug 2024 20:21:39 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce33b47a60a0edcc0ae4e0e2ad7e84d06418efb7f5a18949fb71375b074be23`  
		Last Modified: Tue, 13 Aug 2024 20:21:39 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf94cc71b89c5eec42b513860c78bed50614e2b584405844498d91395227921`  
		Last Modified: Tue, 13 Aug 2024 20:21:38 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53c75cbb4480b6fa277f6ebe029453122fa725e094fe9a1f701df1382590f2e`  
		Last Modified: Tue, 13 Aug 2024 20:22:09 GMT  
		Size: 313.3 MB (313326275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655155ea524e47ac41a61658008caae815583484ecd60c32938a6d3aa61029d5`  
		Last Modified: Tue, 13 Aug 2024 20:21:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fb96a6335aa5d5a2788bf1711ea5290fba594040a965537f49a5bec35c343a1`  
		Last Modified: Tue, 13 Aug 2024 20:21:38 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40e0d4e779aa56ec33785a5c033144da1b5367582a59edbe0071287954245b7`  
		Last Modified: Tue, 13 Aug 2024 20:21:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
