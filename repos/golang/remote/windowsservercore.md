## `golang:windowsservercore`

```console
$ docker pull golang@sha256:1f1a604e38a2fc2dcdf15cc2a50619e70adb242168fd4adc00a5511e83b84af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `golang:windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull golang@sha256:030667e5ceecfc2e2948d7850afa343b4097759b8adf637499fcab0c21468cb3
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3529277358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f5782696663c3ac32f48ef8d8c1556487e2fc8ab55a9b65211b5c92c8cf499`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:15:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:15:05 GMT
ENV GIT_VERSION=2.48.1
# Fri, 18 Apr 2025 03:15:08 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 18 Apr 2025 03:15:11 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 18 Apr 2025 03:15:14 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 18 Apr 2025 03:15:35 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:15:38 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 03:15:48 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:15:50 GMT
ENV GOLANG_VERSION=1.24.2
# Fri, 18 Apr 2025 03:17:14 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:17 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1daf6675ce10a0559ec62812ad0aadc43f55d1a34e20b8de22931c38f6f1e4da`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e761867a4906d3f8b2cbcd5d522446280febb3a53b20c842e97241cfdc0dac`  
		Last Modified: Fri, 18 Apr 2025 03:17:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22099f8a4f2821804cf09a92787bb244f437a2cac28af859bb8e888fca99fd69`  
		Last Modified: Fri, 18 Apr 2025 03:17:22 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5943a664a12d35530cfc923922496d0f091679f3ce0f0674f14cb1a225429c67`  
		Last Modified: Fri, 18 Apr 2025 03:17:22 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc3e6420c54e8b509d77b592f76198e261c743fce705dd9e9960c6c1a102c6e4`  
		Last Modified: Fri, 18 Apr 2025 03:17:22 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2155ea7bdba24f3b6a7b3ac9398a260a73e21faf7158af46061176493362731`  
		Last Modified: Fri, 18 Apr 2025 03:17:28 GMT  
		Size: 51.2 MB (51246233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc35397c468cb2b8419d8d220edd5aab4991c97984a9a5c36aa656dc965b9ec9`  
		Last Modified: Fri, 18 Apr 2025 03:17:21 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0251c2d9cfbed0e0af8acc336a2b8ba7aa88b727ddd815039f749d630ced72`  
		Last Modified: Fri, 18 Apr 2025 03:17:21 GMT  
		Size: 364.0 KB (363993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a47e2ccfdd852ac856e5a666673557a793a93611e7bf92373b5221fc834f52`  
		Last Modified: Fri, 18 Apr 2025 03:17:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b0b21a9b9ed4b8caa4d4142cc4a7d519369f645957d8a85e89e12c6db0bdf04`  
		Last Modified: Fri, 18 Apr 2025 03:17:35 GMT  
		Size: 82.5 MB (82495001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65af914b8f9fb38e22c8a67ae2479d5dfc534706ec2680d84291cc87f5c761a7`  
		Last Modified: Fri, 18 Apr 2025 03:17:21 GMT  
		Size: 1.5 KB (1516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.20348.3566; amd64

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

### `golang:windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull golang@sha256:0472297c5b24b78afcb12e71cad03f4f9b6b555874352cf4697336b0336fbdc1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299426798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da6d98f817289835f3bdb2013f61b92428307ab1e89700e883f9502ae556a40a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:17:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:17:59 GMT
ENV GIT_VERSION=2.48.1
# Fri, 18 Apr 2025 03:17:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 18 Apr 2025 03:18:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 18 Apr 2025 03:18:01 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 18 Apr 2025 03:18:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:18:51 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 03:18:58 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:18:58 GMT
ENV GOLANG_VERSION=1.24.2
# Fri, 18 Apr 2025 03:20:12 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:20:13 GMT
WORKDIR C:\go
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
	-	`sha256:2007307e4ecd50600708f1cab8aedbfdcbca2e92658f21511381cd1ec6a5516a`  
		Last Modified: Fri, 18 Apr 2025 03:20:18 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e8c0619555ba0560a08d4179ff21f7eade08d885bbf8b918582235038187ce4`  
		Last Modified: Fri, 18 Apr 2025 03:20:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6694c9163bda0957a67c7c9839ee55288d0f8dd694ed5f097d687ca57c7ff49f`  
		Last Modified: Fri, 18 Apr 2025 03:20:17 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a25107b9ffd1f1f16073c3a9a2a4f59a052fd45d760392969964af009266b4`  
		Last Modified: Fri, 18 Apr 2025 03:20:17 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4a3973cf1b13da1846375eb14c7c7157cb702424db45af5e76e38bda1d750d`  
		Last Modified: Fri, 18 Apr 2025 03:20:17 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a8a036b328e6fba5a810bc5a429316a4d47713d271d48e989d89de39e09bea`  
		Last Modified: Fri, 18 Apr 2025 03:20:23 GMT  
		Size: 51.2 MB (51198275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c5a874903032432586f249197c2cd2f6bfadd2a60f5d40baa28614921723be4`  
		Last Modified: Fri, 18 Apr 2025 03:20:16 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e710a041267439b5262691e2d30ecff2fc0b3c650bf2212f5feb37737c1a5699`  
		Last Modified: Fri, 18 Apr 2025 03:20:16 GMT  
		Size: 334.1 KB (334145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:620a13358b585e65ea11446d5830b867c3039fe75352bf22966fef50b0d06904`  
		Last Modified: Fri, 18 Apr 2025 03:20:16 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff53b162c16818dcab696fbf825c35a86febe48b53a58948469824bdd2c4978`  
		Last Modified: Fri, 18 Apr 2025 03:20:29 GMT  
		Size: 82.4 MB (82357934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08468895804da1b9e2e696b68db7f3f2b6c5a1f9599a3a5176e5192308ca5111`  
		Last Modified: Fri, 18 Apr 2025 03:20:16 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
