## `mongo:8-windowsservercore-ltsc2022`

```console
$ docker pull mongo@sha256:3db644c6c4363f959f2660e3e2f1f0738a13ac196970f4cb3fcefae938fc659c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `mongo:8-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull mongo@sha256:57ca68b4c13cc2137fe699c9e1c99c64ef4767d8d73dbda84f28d01eaa4ad77d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2797930393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fa592677550dc8f3745c4ccfd0941d90b94badac863878b730d601198dafb18`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 22:08:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Tue, 10 Mar 2026 22:11:17 GMT
ENV MONGO_VERSION=8.2.5
# Tue, 10 Mar 2026 22:11:18 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/windows/mongodb-windows-x86_64-8.2.5-signed.msi
# Tue, 10 Mar 2026 22:11:18 GMT
ENV MONGO_DOWNLOAD_SHA256=02d42062a64b88b68b385dbd723fc2110ef2d43a83642324d94f2f2a6268befb
# Tue, 10 Mar 2026 22:12:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'/l*v', 'install.log', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=MiscellaneousTools,Router,ServerNoService' 		); 	if (-Not (Test-Path C:\mongodb\bin\mongod.exe -PathType Leaf)) { 		Write-Host 'Installer failed!'; 		Get-Content install.log; 		exit 1; 	}; 	Remove-Item install.log; 		$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:13:01 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 10 Mar 2026 22:13:02 GMT
EXPOSE 27017
# Tue, 10 Mar 2026 22:13:02 GMT
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
	-	`sha256:c7844febc2b3fc230db18cb213fc8393b6e366b0df81fa90676409b67dd0c203`  
		Last Modified: Tue, 10 Mar 2026 22:11:02 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f108226ea6de24bdbbf312738f16cc310896fdd798863c92a05b7fae14d7adcb`  
		Last Modified: Tue, 10 Mar 2026 22:13:16 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2656a028d718ce2f9cb83ccadf96306625cbd90d2b3895686c224034736e86e2`  
		Last Modified: Tue, 10 Mar 2026 22:13:16 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f022db29ffdb891255f7215ba57b95819445dee96e0238450411e8052ca4b6c2`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb695cf5356292eb6d8e85928094844b3b956355636d411e82dafeb315cf19a8`  
		Last Modified: Tue, 10 Mar 2026 22:14:32 GMT  
		Size: 815.6 MB (815639834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6151f826a95d1c0d56289a6a08b6f82e231dbc90867bf024fb86d3d1143bcb`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c748d3175b6620afafe10a51b08c289298cf11bed8e7bbde3d0012fa29a5f99`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2c67705fb982354c7f5773644772e8d86416efba04a1f7e1fb3e88f0a2c7c8`  
		Last Modified: Tue, 10 Mar 2026 22:13:14 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
