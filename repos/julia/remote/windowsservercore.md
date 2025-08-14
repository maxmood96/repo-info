## `julia:windowsservercore`

```console
$ docker pull julia@sha256:bedf8d56cd80d6f940f3968e4757cf8318e26ef3f7486f91bc45dcf5958129b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.4946; amd64
	-	windows version 10.0.20348.4052; amd64

### `julia:windowsservercore` - windows version 10.0.26100.4946; amd64

```console
$ docker pull julia@sha256:a6ca77b846485402d9950608eb819fde3cfda919bbc6f54207182abd058303e5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.8 GB (3784792637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3476c17ec709837053fee107219021712ea6e966861e14786e39e0be7f59738`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Tue, 12 Aug 2025 20:27:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:27:13 GMT
ENV JULIA_VERSION=1.11.6
# Tue, 12 Aug 2025 20:27:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Tue, 12 Aug 2025 20:27:14 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Tue, 12 Aug 2025 20:28:16 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:28:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1042898b3767cfa18658c36d43106dfd885fd235a9a37b20d94db5b83621d5eb`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c36cc967029541dde2878411b74bacd9137a1726cb9723e89f7bc39c214146`  
		Last Modified: Tue, 12 Aug 2025 20:32:55 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58db27e15a646db31132da1d269e94474027004b1e464dd96add2c12426f4cfb`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a491dcb2c710748d811db63bed2f7b0d3903b70db7cfce4505630047daee9074`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:917425fa28a9788603f41520ba1e89b12fb63caa8301d5a060250ccc23385c5a`  
		Last Modified: Tue, 12 Aug 2025 23:03:54 GMT  
		Size: 286.0 MB (285955536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafd846427380492feeb94da22ba7c6739f4c2b1b95739af0808407d74bbbf9b`  
		Last Modified: Tue, 12 Aug 2025 20:32:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.20348.4052; amd64

```console
$ docker pull julia@sha256:625447d3dde2bd9c7972879d208c9a0f1304e474077c34ccb074cf3c263abc31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567555274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee7473c348a9a50005201b43a4097f500923821d90cd8da9dd6ffa74ad9b9cf5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:31:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:31:53 GMT
ENV JULIA_VERSION=1.11.6
# Tue, 12 Aug 2025 20:31:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.6-win64.exe
# Tue, 12 Aug 2025 20:31:55 GMT
ENV JULIA_SHA256=fc9148a3e27308ef809c936ed80043a5e43ab76f34910f13efd0c5d3ab5ef9de
# Tue, 12 Aug 2025 20:33:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:33:21 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8663c4d2d36718aae1a419811e3600ed879d9244dc2e62a0de02522fc61245`  
		Last Modified: Tue, 12 Aug 2025 20:35:09 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bcaca73cdc24156b5bf4135eb5726487883d8e47fb96541f9e68c05d0df559b`  
		Last Modified: Tue, 12 Aug 2025 20:35:09 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca570c3f6615c5bd81b96869e558a33852ed19e96d5b9d70a12b218b739cbc6`  
		Last Modified: Tue, 12 Aug 2025 20:35:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71971d011d5acccae7591a17d16a43c9c9e1c1b75eacf47b43ddb4ba0c8d8a58`  
		Last Modified: Tue, 12 Aug 2025 20:35:03 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368098632db31528abe917b1e3b08f8d7e01930b928be89059c13df00977b956`  
		Last Modified: Tue, 12 Aug 2025 23:04:43 GMT  
		Size: 285.9 MB (285856859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff9f044d4f7b2ed5beebbd8ef7693d2c740455ab29f250364880b8808e57cfc5`  
		Last Modified: Tue, 12 Aug 2025 20:35:04 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
