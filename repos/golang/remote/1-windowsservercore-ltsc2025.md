## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:f722776abbdf05072f66999d6e4b2123d5fbc578db203016c16984d45b425865
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull golang@sha256:8f3365a166271d7450e49c1c20945352ec639e7fe204a96a5de2523f3b3f57d4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3610396320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0df2a9b3f0de901a90f0b1c5d5810cb15523597482c3210cde86afe7a696db4e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Tue, 10 Jun 2025 21:27:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:27:29 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Jun 2025 21:27:30 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Jun 2025 21:27:32 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Jun 2025 21:27:33 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Jun 2025 21:27:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:27:49 GMT
ENV GOPATH=C:\go
# Tue, 10 Jun 2025 21:27:56 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Jun 2025 21:27:58 GMT
ENV GOLANG_VERSION=1.24.4
# Tue, 10 Jun 2025 21:29:17 GMT
RUN $url = 'https://dl.google.com/go/go1.24.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b751a1136cb9d8a2e7ebb22c538c4f02c09b98138c7c8bfb78a54a4566c013b1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:29:19 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5ccfea208eb9bf515934aae7089e172864d48fd8d4317b95722e5ea8aea097`  
		Last Modified: Tue, 10 Jun 2025 22:10:14 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418ede0cd30146db1ebe1589b4c2c648477da99fab8bddb20266325d5c0ec871`  
		Last Modified: Tue, 10 Jun 2025 22:10:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd34f5ec8c3fdb74b6469c243475aebba6c35c91c3c8d3db0df96d1fc284f8d5`  
		Last Modified: Tue, 10 Jun 2025 22:10:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727e36afa13a8fd1b9c7ce603ab80222cba1c34acb544c7ff57ecfdfc37b8c0f`  
		Last Modified: Tue, 10 Jun 2025 22:10:17 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc16a23a79df7bde4d11b85c1a20ff1837ee023a7e0c6aa5ff35a1a07337ef0`  
		Last Modified: Tue, 10 Jun 2025 22:10:17 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b4900d45fc26136ec2ae5458effdb3fb7bd9d15ac007f893c95bf690ce42ba0`  
		Last Modified: Tue, 10 Jun 2025 22:10:21 GMT  
		Size: 51.3 MB (51262550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:399888b2e0deb99105e984b1a45f460cffebfde8e5c5e881e07cfaf20795d5dc`  
		Last Modified: Tue, 10 Jun 2025 22:10:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f75a11893d11103ce297e5f1c361b75b1abec6dd4779cab21e3a89817b3edc`  
		Last Modified: Tue, 10 Jun 2025 22:10:22 GMT  
		Size: 392.4 KB (392427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cea248e4ca2076025e65a30d5ee780a89240e9331937f372b6a4800713a620a`  
		Last Modified: Tue, 10 Jun 2025 22:10:23 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2415a76bfef4a575e23a137ac349e33ca5db05def0aa70ec9d63b3afd8806943`  
		Last Modified: Tue, 10 Jun 2025 22:10:29 GMT  
		Size: 82.6 MB (82556543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e12bb1f39fb6a6023775e15f267e6dbf093962598f3145c96baf15a9ad5d221`  
		Last Modified: Tue, 10 Jun 2025 22:10:30 GMT  
		Size: 1.5 KB (1529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
