## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:e0434b306359b6de5e487addb31931f175481fe451b48ab16bbda7bacae5497c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull golang@sha256:6fe31f5059b8373c41cdefa307d79894ffaea6c67159f37c9afaf01e768fa864
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3685619545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ac9285870ca0881e4d8a21c8798940deca3ad2f5f643aac8d11bdcc5093054f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Tue, 07 Oct 2025 19:33:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 Oct 2025 19:33:56 GMT
ENV GIT_VERSION=2.48.1
# Tue, 07 Oct 2025 19:33:57 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 07 Oct 2025 19:33:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 07 Oct 2025 19:33:58 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 07 Oct 2025 19:34:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:34:33 GMT
ENV GOPATH=C:\go
# Tue, 07 Oct 2025 19:34:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 Oct 2025 19:34:39 GMT
ENV GOLANG_VERSION=1.25.2
# Tue, 07 Oct 2025 19:36:19 GMT
RUN $url = 'https://dl.google.com/go/go1.25.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c18b46f6aa44dbfcd54a9db19dd2fcc5ad684819addcfcf968aa75dad89a89c8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 Oct 2025 19:36:20 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c930722fa7c27b5f2ebcabd1d48f0ae46ca0f73ac356015926639bd386b929`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f28534faffd08baac64096bd10b6745e014b7345aa17e28356aa9db4ff8fcf8`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:829a0f666da6074e2b2d567760a1c76ed46b9da380d7ceadb553a8ff3e3c728b`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec59792f5ba5dfb0c092b355a01157fa49d5881b9558abb40f0cbcf7e144c45`  
		Last Modified: Tue, 07 Oct 2025 19:45:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888bb4f563cdd2d81289f9ab878ad6566ef787bbae76c658fc98d85d3cb2598d`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac4ce5bd76392c952d3a401ad4ff2c1028c1cfaa77a6594dc331317b2e5a6097`  
		Last Modified: Tue, 07 Oct 2025 19:45:11 GMT  
		Size: 51.2 MB (51237312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccf4b274abdacf8985b388b8c531bcb842d9e84a3a790ecc872d9be15580667`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5490d449e6678ba6cbc1af67fd8e2a19ea2e0e33e61e92de62454328c02474d`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 353.2 KB (353221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3babdd19ee1f6f0d71eaf042b33d45818541c9f05cb69ea225a414f423538a1f`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0abb5f4d05f51b0eed124d4766c0914601db8a25f062531d1db8aed39da68eb4`  
		Last Modified: Tue, 07 Oct 2025 19:45:21 GMT  
		Size: 62.6 MB (62578590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78b07091315c7619c64765c65e948733b3b88385392d329c100de65fcf269bc`  
		Last Modified: Tue, 07 Oct 2025 19:45:04 GMT  
		Size: 1.5 KB (1505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
