## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:b21f945f75a0af5f372c03cead52a84f725ba635c6f414ff9bcdfd81c64008c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull caddy@sha256:44aba8da329d3ea3489327b5c94e41477f815f943659f4464a2c859ad400dcfd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1933815424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d095c2914283b4b75e4dbb95eb3e7f5ff6db80079dc6981bf1c5fa8355036c99`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 00:36:23 GMT
ENV GIT_VERSION=2.23.0
# Thu, 10 Aug 2023 00:36:24 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 10 Aug 2023 00:36:25 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 10 Aug 2023 00:36:26 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 10 Aug 2023 00:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:37:00 GMT
ENV GOPATH=C:\go
# Thu, 10 Aug 2023 00:37:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 10 Aug 2023 00:50:52 GMT
ENV GOLANG_VERSION=1.20.7
# Thu, 10 Aug 2023 00:53:17 GMT
RUN $url = 'https://dl.google.com/go/go1.20.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '736dc6c7fcab1c96b682c8c93e38d7e371e62a17d34cb2c37d451a1147f66af9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 10 Aug 2023 00:53:18 GMT
WORKDIR C:\go
# Thu, 10 Aug 2023 03:06:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Aug 2023 03:06:10 GMT
ENV XCADDY_VERSION=v0.3.4
# Thu, 10 Aug 2023 03:06:11 GMT
ENV CADDY_VERSION=v2.7.2
# Thu, 10 Aug 2023 03:06:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 10 Aug 2023 03:06:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('542b4c083852d41081186c79757b66ff3c26248f72ed461dbc038b51687d0a8a8ce8eee69e3b5a1d43360c48b3405b611b940fa378debe98aaa0b3c5aebfa218')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 10 Aug 2023 03:06:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:877256a6389e5e2563da79ad5bd201e7ee136abf14ff7cb0d4efbf3b24e5f127`  
		Last Modified: Thu, 10 Aug 2023 01:02:20 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a39df29b3c0b2f7e691c47273110db4a46e5c8e299f6bb95f77a9c61f79872`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8574d63bce1547e3177d0b76237a782a9b016d4880375dcd1a7b6a1c5dee3dc`  
		Last Modified: Thu, 10 Aug 2023 01:02:18 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef34b3c96316bcdd92e24c8c4eebdc3a35f245c013ef87edfae0dde091a305`  
		Last Modified: Thu, 10 Aug 2023 01:02:17 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a481babc5b629f694446a96dba8d77c020257c98334c605aff94162b9a917279`  
		Last Modified: Thu, 10 Aug 2023 01:02:23 GMT  
		Size: 25.6 MB (25554169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:281178ea1c103ff07ea7e4fb647eb0dbe4f865742da6ef9944e04f37974fc27c`  
		Last Modified: Thu, 10 Aug 2023 01:02:15 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6b5d34adf2aacfe87580143f3e17c635dc8dbd4068377b79b35d665f49bbad9`  
		Last Modified: Thu, 10 Aug 2023 01:02:16 GMT  
		Size: 275.9 KB (275946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a02a2e79b5a05c2145c733eefb2add45d1ebefb7a16b93c321f5883c8ced6f1a`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dd9991b8cfbc481c153abf1625143209f4c4fd40d9443a5a19f4e3613336ad2`  
		Last Modified: Thu, 10 Aug 2023 01:04:53 GMT  
		Size: 108.9 MB (108927695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85dc6778f41c3c7d50b8e71668e22880153d6c6794f24c4661fc3d6aa089d0a5`  
		Last Modified: Thu, 10 Aug 2023 01:04:30 GMT  
		Size: 1.5 KB (1547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8c5985f015e143065716f5aabf0ecaed537103c5ec07e6c57360204a7787d02`  
		Last Modified: Thu, 10 Aug 2023 03:08:23 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd9cf527e30318df5bccd0be2c9a9716dc073b1f84c1d2c5cadc85adcf2af02`  
		Last Modified: Thu, 10 Aug 2023 03:08:21 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604bc0fdaac29b943186656363f9267b86b2744da35d6b519a428d494d0a6bd3`  
		Last Modified: Thu, 10 Aug 2023 03:08:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b527a45b48b4328e0ea94e3e2d3f239ed4f960d30ea0b9272cd902aec85c8b`  
		Last Modified: Thu, 10 Aug 2023 03:08:21 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9ae10f93498ae3f8bbfef69dd561e41337584fb8dcc09fe82ed4971f9787be`  
		Last Modified: Thu, 10 Aug 2023 03:08:21 GMT  
		Size: 1.7 MB (1675642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6218363385083ee3dbece9e5e2fd5c9086be201ca76bd6818b46bb6e591688eb`  
		Last Modified: Thu, 10 Aug 2023 03:08:21 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
