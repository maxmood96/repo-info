## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:201e7d7be0f0deb24f6fcde92267b648699dcf62ebee8f5bfc105e2c114f2399
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull caddy@sha256:320259941b6014cfa574f06de15e018d8d172e07d8d019841dfb7d56453d3b23
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2494974705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:680760c3966ab47e95360816575a80e7850473cd6d4c547d1c9e4eb5fc82f7e9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 12:11:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 12:49:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Aug 2022 12:49:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Aug 2022 12:49:47 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Aug 2022 12:49:48 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Aug 2022 12:50:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Aug 2022 12:50:19 GMT
ENV GOPATH=C:\go
# Wed, 10 Aug 2022 12:50:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Aug 2022 13:08:28 GMT
ENV GOLANG_VERSION=1.18.5
# Wed, 10 Aug 2022 13:11:33 GMT
RUN $url = 'https://dl.google.com/go/go1.18.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '73753620602d4b4469770040c53db55e5dd6af2ad07ecc18f71f164c3224eaad'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 Aug 2022 13:11:35 GMT
WORKDIR C:\go
# Wed, 10 Aug 2022 18:09:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 18:09:58 GMT
ENV XCADDY_VERSION=v0.3.0
# Wed, 10 Aug 2022 18:09:59 GMT
ENV CADDY_VERSION=v2.5.2
# Wed, 10 Aug 2022 18:10:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 10 Aug 2022 18:10:26 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 10 Aug 2022 18:10:27 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a5e3787c778295a5877e0381020b02273a985f7db2dd483ddff586869546e4c`  
		Last Modified: Wed, 10 Aug 2022 12:42:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89a6a7fe48246bae14c787b3f68ad97b9d649ad0f0ebc9d654eefa90a681bc4`  
		Last Modified: Wed, 10 Aug 2022 13:24:02 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700d78f1a37edaf812b6b377963b4ad46402a067ea09535d282788b017da5ce1`  
		Last Modified: Wed, 10 Aug 2022 13:24:00 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97de872a1f90401514b1fd4224785cb2d6301b849142a6612abe22f91f6bef42`  
		Last Modified: Wed, 10 Aug 2022 13:23:58 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89af222c4e6bc5d4bc31acd2d1cf98a0258bcacf3d9a8ecd43f1705eac313351`  
		Last Modified: Wed, 10 Aug 2022 13:23:57 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a406a2386e04b60cf969f8eb5872e6749e87b083a11e09bf35dc23634c489`  
		Last Modified: Wed, 10 Aug 2022 13:24:05 GMT  
		Size: 25.7 MB (25713776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810a29e3add75397336456fd6d35a417140bcfa4ba740025ae5377ffd17b83b`  
		Last Modified: Wed, 10 Aug 2022 13:23:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8ff3f35e00b20d78e9808298cedaf198a5e5733be3735faa63d2784a0c5848`  
		Last Modified: Wed, 10 Aug 2022 13:23:56 GMT  
		Size: 558.2 KB (558170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f0aac69813ccbb95698e409e49283b7c71dfeaaf6c3e28205e539f412e4a854`  
		Last Modified: Wed, 10 Aug 2022 13:28:27 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1cf31b6930fc42ccfa72580824ff8157474e5864871b1fb2dcc8377e07bb731`  
		Last Modified: Wed, 10 Aug 2022 13:29:17 GMT  
		Size: 149.9 MB (149863933 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a70e1e7e80b5673c395003f3bc2d5ace7373d46a6f337a2fdb6795dea4483f8`  
		Last Modified: Wed, 10 Aug 2022 13:28:27 GMT  
		Size: 1.5 KB (1539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73b0e93b422de18d3b99dee38fdec7fd8dcdf18beb14f081f771bc961502e647`  
		Last Modified: Wed, 10 Aug 2022 18:11:56 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7f39e7f2bf16cc3d0d970731bdc403d6e73271dde016a4fe03ca070d367af91`  
		Last Modified: Wed, 10 Aug 2022 18:11:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f53a239aa20c6e43ce77e69830dbb99d1303b10c58eb287c4e829bbbead94ba`  
		Last Modified: Wed, 10 Aug 2022 18:11:53 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:583fecd9f11e29ddf2479d8702f4f23faa998949a3d951e59ca8203eb1ee5ebc`  
		Last Modified: Wed, 10 Aug 2022 18:11:53 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ac316b75f8238892f9d6248ea6d0f03225dcd9c47498222eb8c6a1e07ae1c6`  
		Last Modified: Wed, 10 Aug 2022 18:11:54 GMT  
		Size: 1.9 MB (1931169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0211c69362d49512e039d8fded28ad083cfd7a6b44b95a4acc04e3a4c44506`  
		Last Modified: Wed, 10 Aug 2022 18:11:53 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
