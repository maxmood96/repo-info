## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:9065627b0559db0ab4d315a43a9af096813766d813a85a3ce51504d4b194b314
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3566; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3566; amd64

```console
$ docker pull golang@sha256:6fb5b29ef73003c0cdb9cc2bec53467b1551da607b184a05802bcd05d4aade88
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407368561 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a42821dff4015b8ec20e30195d59a362bbf64fda243e2cad70b9a33dd20dd1c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:17:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:17:14 GMT
ENV GIT_VERSION=2.48.1
# Fri, 18 Apr 2025 03:17:15 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 18 Apr 2025 03:17:16 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 18 Apr 2025 03:17:16 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 18 Apr 2025 03:17:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:35 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 03:17:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:17:42 GMT
ENV GOLANG_VERSION=1.24.2
# Fri, 18 Apr 2025 03:18:53 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:18:54 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7730b2c4130290a6a7782657e4fa7874c68dc3d507fb226a5c3ed6c17b4e7387`  
		Last Modified: Fri, 18 Apr 2025 03:19:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d464ee4544d62317748a4d40a12da1c38d123b60f6d0397b63ca590b923c9162`  
		Last Modified: Fri, 18 Apr 2025 03:19:01 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d57ad739ecc0e279d8c43ed614977201d2eb658353f6975ad55a5eb81ea447aa`  
		Last Modified: Fri, 18 Apr 2025 03:19:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2992d5b9b9c4cbe569b5ba863677e5bcba7b3680245ac8ae092209404c91d725`  
		Last Modified: Fri, 18 Apr 2025 03:18:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5f30f7602fc70cb61cd2d483ae2cc23f535bc2fa031005dfd02aaaece61cdf`  
		Last Modified: Fri, 18 Apr 2025 03:18:59 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddf6184cae4009f90bee4942bf8c24fc54f5f28f50a92c432bdb4a8ec6b837a2`  
		Last Modified: Fri, 18 Apr 2025 03:19:05 GMT  
		Size: 51.2 MB (51194664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:497faa1f844159d04f681f84bcd71693fbda6803bf45a8e162e6972fab360e81`  
		Last Modified: Fri, 18 Apr 2025 03:18:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:166d2f2706f92d28da7cb6c7652846e3b038216e802715e282a991532e84f58e`  
		Last Modified: Fri, 18 Apr 2025 03:18:58 GMT  
		Size: 336.2 KB (336229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b776843821c297979d9d1984a3a3805f82bafadd3dc6e8a99e2fddf3ff41e246`  
		Last Modified: Fri, 18 Apr 2025 03:18:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0bfbf6817e83c91fffcf8b7b541928cf69441bc905c1b7ad7c81fba5240593`  
		Last Modified: Fri, 18 Apr 2025 03:19:10 GMT  
		Size: 82.2 MB (82244732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d89f410e033a7059832d65dae970a4f5d0f67044976a9588820634e66707e07a`  
		Last Modified: Fri, 18 Apr 2025 03:18:58 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
