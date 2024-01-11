## `mongo:7-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:a0b6161b251428cc6b4783f244e5b0f29d460725d3ca1d0bb6a76198ec565384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `mongo:7-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull mongo@sha256:f6e3f95455279cff22b21bbd8e34f8b891c39b22cd795bda3ea4d2cd3a4ea665
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2513074958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6094f7ea2a542c5d94f12af1c92eebbccfe0ff1b0174d0c747961290d4a6700`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:08:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Thu, 11 Jan 2024 00:08:13 GMT
ENV MONGO_VERSION=7.0.5
# Thu, 11 Jan 2024 00:08:14 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-7.0.5-signed.msi
# Thu, 11 Jan 2024 00:08:15 GMT
ENV MONGO_DOWNLOAD_SHA256=96441addde451b9d81dfaa10aca9678ada35d17d02a9a07481c6137d3df55e2b
# Thu, 11 Jan 2024 00:09:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:09:52 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 11 Jan 2024 00:09:53 GMT
EXPOSE 27017
# Thu, 11 Jan 2024 00:09:54 GMT
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
	-	`sha256:23a6ec03c2a160ba4b038ddae483ec907f1d72e641ae96db10132cd265b8341f`  
		Last Modified: Thu, 11 Jan 2024 00:10:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead4f04e23ba3df03b8407f5af834ecd48b89240e35e0bfd35a395bf5fb730f7`  
		Last Modified: Thu, 11 Jan 2024 00:10:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:187c8c1e4e77012d4d3c4269ba2d3c0f277fc3243676da8d948ad3b3504f9c51`  
		Last Modified: Thu, 11 Jan 2024 00:10:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a72b64df9937ffdab47c1c017459a0e37a7f555bdc2e73b618f6d09369a4429a`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bc67b2fbe2158d8a244db4c307638df622abbaf6d5114ae6e87a7c84683ee0`  
		Last Modified: Thu, 11 Jan 2024 00:10:52 GMT  
		Size: 612.9 MB (612853259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863a185ce32d5e0f6fcf2e1a8741e70092ba0ff337858530fc67c1533a219f2f`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c00cfce2f9415941a60e5433f970a60f76c2a8737d4a5bd19c0592786fbca5f7`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e7f9045d893218c6eb72f02afde0edfd960a6fdb99bd93f38ac9be07dbc6f0`  
		Last Modified: Thu, 11 Jan 2024 00:09:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
