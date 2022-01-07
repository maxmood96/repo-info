## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:1d070358ceb1d64117a5a0c321c3da5fdb0df850abf3ca71dd242122d28eb661
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2366; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.2366; amd64

```console
$ docker pull caddy@sha256:4b726685d590d9d546d497c7633dcae1651f4391788eb510f39fcb3ffd610c78
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2881520451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709b60fca3717b0def57b71c5d01fabb8ce7c2a6ef1afed7e25cb25bf78ad298`
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
# Thu, 06 Jan 2022 22:19:38 GMT
ENV GOLANG_VERSION=1.17.6
# Thu, 06 Jan 2022 22:23:51 GMT
RUN $url = 'https://dl.google.com/go/go1.17.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '5bf8f87aec7edfc08e6bc845f1c30dba6de32b863f89ae46553ff4bbcc1d4954'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 06 Jan 2022 22:23:53 GMT
WORKDIR C:\go
# Thu, 06 Jan 2022 23:31:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 06 Jan 2022 23:31:58 GMT
ENV XCADDY_VERSION=v0.2.0
# Thu, 06 Jan 2022 23:31:59 GMT
ENV CADDY_VERSION=v2.4.6
# Thu, 06 Jan 2022 23:32:00 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 06 Jan 2022 23:33:13 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.2.0/xcaddy_0.2.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('233a57384b1f82e9420567da74b4fbd19e898112e43b8447dbdb8ddde15cb4d8a66aea58307ccdda74d37c5e525f0dc563f83d4670aee048842754eee9a3bc2b')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 06 Jan 2022 23:33:14 GMT
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
	-	`sha256:a052b1738ba5f522e9610fbae3f1972bca981ae691e049ed9b07b956068a8d65`  
		Last Modified: Thu, 06 Jan 2022 23:00:50 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941e7adb7f3a0e89b661cc51fc67d057922f4c81b14529e73cc99bdc617cdbd8`  
		Last Modified: Thu, 06 Jan 2022 23:03:24 GMT  
		Size: 145.4 MB (145423878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888baa7dedfe2a537005ea851c77a196974fc1e1dbcc7be7eb93a95fe7c7299e`  
		Last Modified: Thu, 06 Jan 2022 23:00:50 GMT  
		Size: 1.6 KB (1584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3224520fa3a4dc307aed3e6289c01352ed0f2a960c7dd6f004c63b4a15eb34`  
		Last Modified: Thu, 06 Jan 2022 23:35:36 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe87f489462e26b8ce1021337c09e14e290c46dd4318354244146793803ef9d1`  
		Last Modified: Thu, 06 Jan 2022 23:35:34 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b26c38706131743c78e64ac038d946272ff6ac9caa58b31e6af51bd942165f7`  
		Last Modified: Thu, 06 Jan 2022 23:35:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ec4000f4cf659608d744e0ca1c81c2887deac0b8d972f4c1b8f043d33f67a1`  
		Last Modified: Thu, 06 Jan 2022 23:35:34 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da522bb9811c2f1354aa415f843559e3d9d817c2a505f57b374e4c9c3b2c2c37`  
		Last Modified: Thu, 06 Jan 2022 23:35:34 GMT  
		Size: 1.7 MB (1670036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6a081271ee5c28037d879587556d3cd48ed770d67af72ca02eb6f5de69e2ad`  
		Last Modified: Thu, 06 Jan 2022 23:35:36 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
