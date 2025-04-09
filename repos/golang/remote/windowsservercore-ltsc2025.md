## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:dc43a64ba8895f345e865040e00a5c07699851f584d0cef780075edad6694b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull golang@sha256:e29fa934998590e81186bb08c40a15164560e42544d807437c6f89eb5bc9fae2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3528792761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816853d92bdc97451867ed14d5a594511d44b99ac051a03661c3f2e86f17150b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:44:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:44:04 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:44:05 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:44:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:44:07 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 00:44:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:44:21 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 00:44:28 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:44:28 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 00:46:03 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:46:04 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672cf33de477ad825cbaa16a956e9d5d339db68a30efa7b3ff24ea6fbd02846`  
		Last Modified: Wed, 09 Apr 2025 00:46:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fc7c6dd17b7d72b3a1b65f71da98a86a10e9a2f62f51700a42682ce4268914`  
		Last Modified: Wed, 09 Apr 2025 00:46:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e132aab1dd805923e52f664ee264e6f42963c7e99a6037ab371c2d54ca76b32`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb12eeebab81f5162a35e2db0fc603735dbf320dfdbdc094656656cda055da`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27a60939c03ad6bcc785a1bf280189f4e112281d56c5356ca4876e4c7acd78`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a77c9a310a4f142c5098362986c6c9975ca2b1243431d56e12055fef19d49ea`  
		Last Modified: Wed, 09 Apr 2025 00:46:14 GMT  
		Size: 51.3 MB (51253178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0312c7451731be32488e49beb94106a26ff17993a360c0b06498474fa488521c`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8727a8f7c608ffd128685607cf14b845cd5148598a30250657b78a7727fce963`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 378.0 KB (378041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c156426602a359ef6dae2b64d5ce0a2145b84588c901063d41fd0f1713dd5eca`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7906439a638b42ec85dcdd3b2205effee08115f7f42d2dcf9f1a5f2103a07f40`  
		Last Modified: Wed, 09 Apr 2025 00:46:23 GMT  
		Size: 82.5 MB (82471510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e79a665256513d99d621933d5f1489cdfb9bab3495509e0ec43766fe85ced9`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
