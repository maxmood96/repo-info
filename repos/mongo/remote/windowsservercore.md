## `mongo:windowsservercore`

```console
$ docker pull mongo@sha256:ee6ae85dc0bf19f473a9ccf0a5d6032909a1c0ffd5e376115f53544f375037db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `mongo:windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull mongo@sha256:a8b0e268528b5f6d218e35ad70ec89c96e2c25c2a4fed26517bd42c9412cc269
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (3023409886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0436e714e9abacae6624e161418509a8499dbbe559afd1b4f008a496c74c7f47`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Wed, 13 May 2026 18:08:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2026 18:08:29 GMT
ENV MONGO_VERSION=8.2.9
# Wed, 13 May 2026 18:08:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.9-signed.msi
# Wed, 13 May 2026 18:08:32 GMT
ENV MONGO_DOWNLOAD_SHA256=a23b5865415ab2d507823e64163e5f3b09a4118bd8ede539938673137faab690
# Wed, 13 May 2026 18:12:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 May 2026 18:12:03 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 May 2026 18:12:04 GMT
EXPOSE 27017
# Wed, 13 May 2026 18:12:04 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2e71fcfcdfe254acdf87925bb5a5e77fbd7dbfebd1a7c8acf08ae52d7fbe4a`  
		Last Modified: Wed, 13 May 2026 18:12:10 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe744cbc12304c7060b11d80ecb4bbd58293aca960c748d716774d1de861aa46`  
		Last Modified: Wed, 13 May 2026 18:12:10 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f545ef23daec859b93292fb34eb96cd3da0db3764b84db3ecfa7b3c6a94f92`  
		Last Modified: Wed, 13 May 2026 18:12:10 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5031d0fb24d43b7d05964284ea133a90ded3c72b3eb0f0ded1fc0fa3c8d6e144`  
		Last Modified: Wed, 13 May 2026 18:12:08 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2745f4b940463b5da7c1c713ed5a098edc11e5017789dd9f6375cade355c2abd`  
		Last Modified: Wed, 13 May 2026 18:13:19 GMT  
		Size: 817.5 MB (817459000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bcecd0543b7b801867a19822abf90b74f9b0ae02da602ff9fa563c8a692186b`  
		Last Modified: Wed, 13 May 2026 18:12:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43130c454ba54034d370470377f81027119eb28273af178aa7b9b995e1b9cee9`  
		Last Modified: Wed, 13 May 2026 18:12:08 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800ebb76b516f5dd3be3460aaa73ee0b2b8b6dc225058a2bc64e0609154893c1`  
		Last Modified: Wed, 13 May 2026 18:12:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull mongo@sha256:a035418461544e38ba99071e34c722a82334e460ea167ffd5ccebcad5dffb9fe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2939938805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abb83c987f09f9332c92e37b8fcdddf30bed70e68e2a1e901e832b7ec634bddd`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Wed, 13 May 2026 18:03:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 13 May 2026 18:03:59 GMT
ENV MONGO_VERSION=8.2.9
# Wed, 13 May 2026 18:04:01 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.9-signed.msi
# Wed, 13 May 2026 18:04:02 GMT
ENV MONGO_DOWNLOAD_SHA256=a23b5865415ab2d507823e64163e5f3b09a4118bd8ede539938673137faab690
# Wed, 13 May 2026 18:07:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 13 May 2026 18:07:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 May 2026 18:07:16 GMT
EXPOSE 27017
# Wed, 13 May 2026 18:07:17 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76407b7ee42fcdd4537d11a228402cf519502615467c560ff242ac7a8420b43f`  
		Last Modified: Wed, 13 May 2026 18:07:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71c04263b7043f2442cb331ec530e62dd1e7b7dd36294ba7cd292e1d323bbf06`  
		Last Modified: Wed, 13 May 2026 18:07:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd955c6af2065b51f3679f5b6b33f991b7a4871280270dfb2e9623b28224b510`  
		Last Modified: Wed, 13 May 2026 18:07:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28bc130b8ae93042cd19653d1788f6fa13a48e2e4f451e4c613d814b6da32f90`  
		Last Modified: Wed, 13 May 2026 18:07:24 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba88c6f856bd393fb20ce01a4ac0c5e6ed182da823db6b56e3cce42601c31f9`  
		Last Modified: Wed, 13 May 2026 18:08:40 GMT  
		Size: 817.5 MB (817509038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d4dbd15cf89827803b8571f449048d5b546d3933eb955641a24a43e26ab375`  
		Last Modified: Wed, 13 May 2026 18:07:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e04a20b0f5f0e05d9837f9f48bde8102c96dd05aff2450d43a040ef1dcb8a54`  
		Last Modified: Wed, 13 May 2026 18:07:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c8520fd57ba073953ecd51665fb5faa482efda0ce676f687f92f38fb9528c93`  
		Last Modified: Wed, 13 May 2026 18:07:24 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
