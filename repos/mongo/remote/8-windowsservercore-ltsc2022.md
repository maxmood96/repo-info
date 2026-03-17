## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:a3c4666eba12ff7f563d7b76f470ed90cad4d4c7412e277bc994a9a2219b913e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull mongo@sha256:2bddc1202f7d5f0275bcc884ad482372b715e56161b168477fceb1e131f402bb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2799555230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9b72ee36ebeaea5b4e62e3d0ad20db9134ddca2ab092f09333952d6243e6d9`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 17 Mar 2026 18:05:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 17 Mar 2026 18:05:32 GMT
ENV MONGO_VERSION=8.2.6
# Tue, 17 Mar 2026 18:05:33 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.6-signed.msi
# Tue, 17 Mar 2026 18:05:33 GMT
ENV MONGO_DOWNLOAD_SHA256=a6672561354b1bd37c5ba8d7dd76b66bfdbd28baec6fd8eb2b7eb2b32eaf344f
# Tue, 17 Mar 2026 18:07:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 17 Mar 2026 18:07:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 17 Mar 2026 18:07:58 GMT
EXPOSE 27017
# Tue, 17 Mar 2026 18:07:59 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62430fe0975ecfdad77ac0cf66b918cd69edc36a8b48e0bbed20b0a612b2cf35`  
		Last Modified: Tue, 17 Mar 2026 18:08:13 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e551441cbadd370dd75ab0f9e96a3ba577871c0d919aec1f92880588c48c8ca0`  
		Last Modified: Tue, 17 Mar 2026 18:08:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404a5794660fbb5b6d7af22cd39d2d70fb8d7704ca52ad286e5eb70c192045f3`  
		Last Modified: Tue, 17 Mar 2026 18:08:12 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff55011c515d23bc6eb501efe52e72b599716ed0bc6b049667d25a614104caeb`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4074d47cb546f2a399f03a0489132de7160f4aa8cca8c529b4981f5dcd0e80`  
		Last Modified: Tue, 17 Mar 2026 18:09:31 GMT  
		Size: 817.3 MB (817264643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86dbb13ac1d3e15b791132a7470f6578826f8fb2a5b2cf59b0d4310c11373e`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4519129b8b4a6fc4078f8a2189660ca379ccf761a45f886509f806bf8dc99993`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1492217039ef3d5728ef075dbe9713f8bd05833a9a6bc54b0b8f76f6938c935f`  
		Last Modified: Tue, 17 Mar 2026 18:08:11 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
