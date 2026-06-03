## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:c8bcbbec6d95bb5ec6f39e0ef60c0709c2b14cc6a2c5d2d454ce38ad3997f85d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull caddy@sha256:b1e6e0e3a414c859fd3564da761650c264999740300c425af42f2a5119dfb085
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2335210962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89de694fba58a02d470737acecb575a06bbdae1ebbe864d1b10c37ea1042cfa7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 02 Jun 2026 21:46:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 21:47:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Jun 2026 21:47:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Jun 2026 21:47:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Jun 2026 21:47:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Jun 2026 21:48:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:48:54 GMT
ENV GOPATH=C:\go
# Tue, 02 Jun 2026 21:49:02 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jun 2026 21:49:02 GMT
ENV GOLANG_VERSION=1.26.4
# Tue, 02 Jun 2026 21:50:55 GMT
RUN $url = 'https://dl.google.com/go/go1.26.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3ca8fb4630b07c419cbdd51f754e31363cfcfb83b3a5354d9e895c90be2cc345'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jun 2026 21:50:57 GMT
WORKDIR C:\go
# Wed, 03 Jun 2026 18:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Jun 2026 18:02:47 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 03 Jun 2026 18:02:49 GMT
ENV CADDY_VERSION=v2.11.4
# Wed, 03 Jun 2026 18:02:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 03 Jun 2026 18:03:39 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 03 Jun 2026 18:03:40 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03db002b9e59a168b97269178d3cea6be969a491719ca1c8d3f4c33ad9ad07f7`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b9c42b86ca2e7aa4eb41766a6f755119c65c8b2c03b320ba0980b9d2f6547a`  
		Last Modified: Tue, 02 Jun 2026 21:51:10 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69c8f4def2bce82d1e544606aaf3e5895ae29437220f1b41211727fbeff83ac8`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16228e0f3edb3815e34fd2d8c6d575e9ed737e1d5cc07909e430d670860bc7cc`  
		Last Modified: Tue, 02 Jun 2026 21:51:09 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fca5f94c0122485a7417a90a87018bf739ef6ef80f60454b5258cefa6a58eed5`  
		Last Modified: Tue, 02 Jun 2026 21:51:08 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1397a64df19d921e6ad74f8c6ca0ea5b401c7731318c4dd85002c5dbb6df922c`  
		Last Modified: Tue, 02 Jun 2026 21:51:15 GMT  
		Size: 51.3 MB (51286214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:871cad50024619c7f067652dc3cc2e678a8c70180235a578d249123c21479637`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:007a76e9414e0db486efb9ff5a4409e15cef9f66f3c19a6efc5d554db55f0e4b`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 367.1 KB (367144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6fea8e7d4ba560522bf09b19a63fc47cca6a724baa7e90623086a8d46f1d8f2`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb44107094e22c635252ccb6df8685c7968f63f084760fcbec0f4cb08857a74`  
		Last Modified: Tue, 02 Jun 2026 21:51:19 GMT  
		Size: 75.3 MB (75252822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f35936631b6cd9bd6e5cf14e0cb4f8a287786047d069c23d09ed69d69e5672e`  
		Last Modified: Tue, 02 Jun 2026 21:51:07 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68070051b7986b4e6b07bccc3e9501ff364fc1d5bdb35447c750f3e1027b3502`  
		Last Modified: Wed, 03 Jun 2026 18:03:46 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f67c24fad992d14f537f7ed989eafa0d11a8498ea7c6760ad5463d8ae49da3`  
		Last Modified: Wed, 03 Jun 2026 18:03:45 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5b24066d680cabeeaba97068b98e30bc24a904d46e012ce07e6169082c7381`  
		Last Modified: Wed, 03 Jun 2026 18:03:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8a694b764934ab54045a5cb2e9b94ea6d542990443e3ca718d67f585678069`  
		Last Modified: Wed, 03 Jun 2026 18:03:45 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0ac56b3368a68b5ea928c2a38ff830ee76456e9d260514630f8eb73e49859ce`  
		Last Modified: Wed, 03 Jun 2026 18:03:46 GMT  
		Size: 2.3 MB (2345943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26fc4fa45ed157ce4b27336ba174dd3fdd91247c542f483cf5f057330a8b9560`  
		Last Modified: Wed, 03 Jun 2026 18:03:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
