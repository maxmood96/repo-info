## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:9015e0b7d658a63c56ad5e565efd064a22394eea8ab02a01a878d8178bc84ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull caddy@sha256:6c22a120f1b7923b71dd23a0e40e041ad078b1f9c71be84bc3fefe434371407d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2881522636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a057732121a81d33eaf8e5d57227b2bf700779cd45c8acdb6e6269bcc1f676dc`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Tue, 07 Dec 2021 04:56:01 GMT
RUN Install update 1809-amd64
# Fri, 17 Dec 2021 23:26:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 00:15:38 GMT
ENV GIT_VERSION=2.23.0
# Sat, 18 Dec 2021 00:15:39 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Sat, 18 Dec 2021 00:15:40 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Sat, 18 Dec 2021 00:15:41 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Sat, 18 Dec 2021 00:17:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Sat, 18 Dec 2021 00:17:44 GMT
ENV GOPATH=C:\go
# Sat, 18 Dec 2021 00:18:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 18 Dec 2021 00:40:47 GMT
ENV GOLANG_VERSION=1.17.5
# Sat, 18 Dec 2021 00:44:39 GMT
RUN $url = 'https://dl.google.com/go/go1.17.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '671faf99cd5d81cd7e40936c0a94363c64d654faa0148d2af4bbc262555620b9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Sat, 18 Dec 2021 00:44:41 GMT
WORKDIR C:\go
# Sat, 18 Dec 2021 07:54:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 18 Dec 2021 07:54:49 GMT
ENV XCADDY_VERSION=v0.2.0
# Sat, 18 Dec 2021 07:54:50 GMT
ENV CADDY_VERSION=v2.4.6
# Sat, 18 Dec 2021 07:54:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Sat, 18 Dec 2021 07:55:53 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Sat, 18 Dec 2021 07:55:55 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ee7a7ea9cf22f75886179907a41810a992e21f3d0c57cc10d2147ce9237701c`  
		Size: 990.3 MB (990271574 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31b2acce136e44984ba36d64717a6a67fbf1a98ed7ffcf0a14df848c1502a345`  
		Last Modified: Fri, 17 Dec 2021 23:47:14 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80c62605b0c86ed37b9b47076c7a5944af667c8ce06e7c6a8509ced095cce159`  
		Last Modified: Sat, 18 Dec 2021 01:19:20 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60899de055c3fa34311259654470bdb9f4fae2bbe462783d8e2aee8b6e0b6cb7`  
		Last Modified: Sat, 18 Dec 2021 01:19:19 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536c6124f0e0905a38e8324ae686057b8d0a17aad59faf3c954b569f52851106`  
		Last Modified: Sat, 18 Dec 2021 01:19:18 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0e8769770a2b32ba2424d699b18ab6c4166ecd2c1125b1c191d522cc6fd51f7`  
		Last Modified: Sat, 18 Dec 2021 01:19:18 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c0c1d102127ee33e6999825a23a390dab7c3a328fff970083d7bdfe99537821`  
		Last Modified: Sat, 18 Dec 2021 01:19:23 GMT  
		Size: 25.5 MB (25462958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f8bef9894d29031a7a230102260249b6d03330b291463ae3bbca1ef5cd8da7`  
		Last Modified: Sat, 18 Dec 2021 01:19:16 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42b9032e958eb0bea7fe89c098d5e729ddc543cf6b86e2284ace9fc062aadc1`  
		Last Modified: Sat, 18 Dec 2021 01:19:16 GMT  
		Size: 340.6 KB (340572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22699dff9a66b55f4e6f3a6d740e29767995d4fd3c01701820e05433f01af0e1`  
		Last Modified: Sat, 18 Dec 2021 01:27:55 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c83944871ee1bb828d65dce68d6c6bc2e01dbbde7492b254695a0d4093a603`  
		Last Modified: Sat, 18 Dec 2021 01:30:40 GMT  
		Size: 145.4 MB (145422931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85fdb656c662d1af6f26ee03d8c4232f30475a97d5e75156e77bdb35da169ce3`  
		Last Modified: Sat, 18 Dec 2021 01:27:55 GMT  
		Size: 1.5 KB (1532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a33ac2e01da597afe7761dada95ee7cc9c8378ca509435767138d4812187439`  
		Last Modified: Sat, 18 Dec 2021 07:58:38 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfaa668bf2a290b447912b61157e6a0c6a2c62858448c19a4222f02edb88fd22`  
		Last Modified: Sat, 18 Dec 2021 07:58:36 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ec63b7d80aab902689c4fde35b67a5e5252a13673bf752c2b2c4f0a41a5255`  
		Last Modified: Sat, 18 Dec 2021 07:58:36 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefb65f3f1c07b8de2b21f0304a6944928059ecf4f1ba0b5f0824ca0b39a5d69`  
		Last Modified: Sat, 18 Dec 2021 07:58:36 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a76493d95d8af1725efa6e5b9166e4d6f5cfc2e1b5d4dee237bdcb4c361b04b`  
		Last Modified: Sat, 18 Dec 2021 07:58:38 GMT  
		Size: 1.7 MB (1673597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b84379e0a165db82cacd14dc4cc2ddc4a1928e7208e045021ea3115217b7553`  
		Last Modified: Sat, 18 Dec 2021 07:58:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
