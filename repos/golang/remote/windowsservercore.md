## `golang:windowsservercore`

```console
$ docker pull golang@sha256:9e0c1bccbaa6b4ccf430544fcdbc7f0128e052e982f192e956ae402941bc0b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `golang:windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull golang@sha256:f307bd0533599086230361ab216ca80ec6b7f64137cdee3c65d9af0f1d00a553
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3349663141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f25abc6494d3bb721d52b9336c7ddbdc318a8d0a3832d2efa73e014e9e621343`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 17:47:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 17:47:47 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Dec 2025 17:47:48 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Dec 2025 17:47:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Dec 2025 17:47:50 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Dec 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOPATH=C:\go
# Tue, 02 Dec 2025 17:48:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 17:48:33 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:51:00 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 17:51:02 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038179540c4b5bff54de1043c1801d521b53ebe92fd131623177c8ab3e5b6d87`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac94f8017cb2897ec8c7b4a364d24e0de9b6ac03074907bedc69cddc08b35da`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f554ee569e72050d229b07d0ae457307eee760a7c8c947c44f4c392f33a5e9`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9856541e5702000461917f2b88924a9219eba9858435827133c1889a768779a8`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3f1f2051dfeded04719c7da15c10f4446ed60a2bd37e1af4dbf690bc9d3529`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758542b365d1f7a0b7e649d055d124d6e79bce402223c28a0db8b57f362c3ca4`  
		Last Modified: Tue, 02 Dec 2025 18:00:15 GMT  
		Size: 51.2 MB (51240483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8698f68d7d54c14ad9ac4657eacdda4a694c31726d4b17c82ed06aa3644cc5`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f08a1e7f7944207640262ae0124487391591ee14934148ccd95ff257223e071`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 364.9 KB (364909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325f8a13aba0057ad7964f76545732ab485ea8a4db4231388fbc70ee772a4aa`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4129a1f5bd9a814437667d1fc8b72a89fd849469d76b6d7ee78c3eaf4d0d52c`  
		Last Modified: Tue, 02 Dec 2025 18:00:20 GMT  
		Size: 62.6 MB (62591300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7d867d536660e28f9277f6eaf18168efe5500e4880a872afd740e3b92da532`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull golang@sha256:2774c03dc2c34073265b8ad0082a8f9713fc6ae260afdd132d07d09ca950981f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1884362436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f511a66f4ea9fefd92fb48fa14de824a7d23a7d21b7a77da8c4af236132be9d1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 17:48:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 17:48:30 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Dec 2025 17:48:31 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Dec 2025 17:48:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Dec 2025 17:48:33 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Dec 2025 17:49:06 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 17:49:07 GMT
ENV GOPATH=C:\go
# Tue, 02 Dec 2025 17:49:12 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 17:49:13 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:52:23 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 17:52:25 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bce81da939692e168b7638f0ac7b2b7766788141093905c4de23d3b234a5ec7`  
		Last Modified: Tue, 02 Dec 2025 17:58:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a8bb1d9915d509f670ce429fd84a1776bf068ab11ce6e204c401abfaae24f4`  
		Last Modified: Tue, 02 Dec 2025 17:58:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea753fe4e5647090b254a168a932e80f110a2748eb3eaa99b09a77f735fcf8da`  
		Last Modified: Tue, 02 Dec 2025 17:58:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bbfa0f78ff2e7aa83698eccfa4adc9a4467facc4372686f11e06c6e233a5a49`  
		Last Modified: Tue, 02 Dec 2025 17:58:19 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e68dca8c954af734aad5d5a16a9fef5733785c20e95ef4920f9d4883220e5cd`  
		Last Modified: Tue, 02 Dec 2025 17:58:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09045c385dbfcf94702959cfa5cf7bd769384fd0b458c47aeb9d4a11a1b0c3a0`  
		Last Modified: Tue, 02 Dec 2025 17:58:26 GMT  
		Size: 51.4 MB (51355829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70bcaffc2ef89b15efd8b35737c5349b63f358d2471a826ff01681ffcaa33ddf`  
		Last Modified: Tue, 02 Dec 2025 17:58:19 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:546d110eb3fac017fa5892c100ad2c265b1325bd5761786fc4b0583c202d3728`  
		Last Modified: Tue, 02 Dec 2025 17:58:19 GMT  
		Size: 352.6 KB (352591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c79d338ecf88d0b596111a887a53b10d00eeaae93748d5779d3e143c69601ab`  
		Last Modified: Tue, 02 Dec 2025 17:58:19 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77135a41217b6f7cec8dc8ac51b4ef53de671b4bd785c24f21bb7f7c12478612`  
		Last Modified: Tue, 02 Dec 2025 17:58:30 GMT  
		Size: 62.7 MB (62681952 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9bd9fdbbbb3c6202fb7adbd8ad4a125d49c493ae7dab10f5d6c81e948c15d42`  
		Last Modified: Tue, 02 Dec 2025 17:58:20 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
