## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:f2563939451852ca0d92ea2ab065973832cf7d2d5ea39831c636dceed775d387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull golang@sha256:840ca8a1efca24b3c86c1464b65d75f05ec1556d6ffd83bed219c5fd7a87de85
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2008165040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:781e7113724a169282747ce4706b75eafee83ae231786927f9e41fa7ed86262b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 19:36:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:27:24 GMT
ENV GIT_VERSION=2.23.0
# Wed, 14 Feb 2024 20:27:25 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 14 Feb 2024 20:27:26 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 14 Feb 2024 20:27:27 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 14 Feb 2024 20:28:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:28:04 GMT
ENV GOPATH=C:\go
# Wed, 14 Feb 2024 20:28:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 05 Mar 2024 19:15:18 GMT
ENV GOLANG_VERSION=1.22.1
# Tue, 05 Mar 2024 19:17:48 GMT
RUN $url = 'https://dl.google.com/go/go1.22.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cf9c66a208a106402a527f5b956269ca506cfe535fc388e828d249ea88ed28ba'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 05 Mar 2024 19:17:50 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63d42cabf5bedf06720e416234beca9b72544bcc7ae0f30533edad0043aa3f12`  
		Last Modified: Wed, 14 Feb 2024 20:55:47 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ac8de2d709384a84400f6f072b2d3d4c4d454ee27f8ec716db4964eabac3f8`  
		Last Modified: Wed, 14 Feb 2024 20:55:46 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70115ee0ce6c09f30645181ec6f80fe9ece4e9b51628fdbaa85ebd4e0ae979e1`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab323644de57af1911793c0a10501a7b21640f8e58484665dc2258f482cb943`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae53fd363daebfb127c2ba7e51543cf93130802d95e194fc71db09c52b9fe10c`  
		Last Modified: Wed, 14 Feb 2024 20:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:665a9a35030c2076331610dfe4c22866525c2b0ac219981d900f1b6178af5241`  
		Last Modified: Wed, 14 Feb 2024 20:55:50 GMT  
		Size: 25.5 MB (25534020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a21ab59c20a7391d04f68a3dc2b9d6eb4cfd1e7af0ddd33e30d2cd19f13535c0`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a35884f3b4e6aa2080cc34668faeabacc75000ef04e2fe4ec3e76f166d992e4`  
		Last Modified: Wed, 14 Feb 2024 20:55:43 GMT  
		Size: 266.0 KB (265989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e52e8a2f3a375432a1ce562b53600ed5e0a5666d76806b793f7489242b2965`  
		Last Modified: Tue, 05 Mar 2024 19:39:32 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99c51d55c989a52fb3ba15c22b4057aff1833264da8e868257c667f7f7c58d69`  
		Last Modified: Tue, 05 Mar 2024 19:39:51 GMT  
		Size: 71.7 MB (71699445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb35ddc33ae5875433de6a805922e3aaa04852cad858efb4ee2a01c1858abd0`  
		Last Modified: Tue, 05 Mar 2024 19:39:32 GMT  
		Size: 1.6 KB (1564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
