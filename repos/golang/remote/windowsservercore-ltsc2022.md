## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:d2f2b8e87fde7cd3e887898de2e3e72ef9653c1d789cebffa4ecafc3dd1619a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull golang@sha256:c35d1b65d8eea34fcd2601b5ed906be080fead7f24d4f4773aca1c2942b3ef36
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2191784264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2fb1cd58f561660970b03156aa8756c6b766b9eeca2610e54e2766028ad5766`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Thu, 07 May 2026 17:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 May 2026 17:53:33 GMT
ENV GIT_VERSION=2.48.1
# Thu, 07 May 2026 17:53:35 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 07 May 2026 17:53:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 07 May 2026 17:53:37 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 07 May 2026 17:55:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 07 May 2026 17:55:04 GMT
ENV GOPATH=C:\go
# Thu, 07 May 2026 17:55:11 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 07 May 2026 17:55:11 GMT
ENV GOLANG_VERSION=1.26.3
# Thu, 07 May 2026 17:56:46 GMT
RUN $url = 'https://dl.google.com/go/go1.26.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '20d2ceafb4ed41b96b879010927b28bc92a5be57a7c1801ce365a9ca51d3224a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 07 May 2026 17:56:48 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2378ac9adb80e88244d0b5376587d59531940ecea248b460e25d88983b06154a`  
		Last Modified: Thu, 07 May 2026 17:57:03 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3836af80f0a6f14eceac02dc7214c140edd78ac022c39a98154f7942c645a505`  
		Last Modified: Thu, 07 May 2026 17:57:03 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:388b8fc0ffd2d9cadfdbfd7ac4987f1d43d05bf89f7ec594ed81263a101a579a`  
		Last Modified: Thu, 07 May 2026 17:57:02 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a021932d840f83f2512640d1b3f502ca15d08dc8de6e2c42ef57bc7973de4`  
		Last Modified: Thu, 07 May 2026 17:57:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d9b4e71af7f2fd74687abbbd345232b9ad7430dd81907054261de5a356f3cb`  
		Last Modified: Thu, 07 May 2026 17:57:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792ce439b0df5bff1154dd515d172f39f8d536627284a695bd2e6d517d2c4b81`  
		Last Modified: Thu, 07 May 2026 17:57:07 GMT  
		Size: 51.4 MB (51357878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5b53dec1bc9c71c9392dd83947562ce8e3e9e51f05a0a64162e4ee79aec27c`  
		Last Modified: Thu, 07 May 2026 17:57:00 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30dec76380380523d77ce48b17139f1142556f986ea6a624e382ab7058c5c5d`  
		Last Modified: Thu, 07 May 2026 17:57:00 GMT  
		Size: 318.6 KB (318618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236cab43865dc091848f408bf1b4cbfb832fa072070376fd4907fb7d73c712ee`  
		Last Modified: Thu, 07 May 2026 17:57:00 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517b292d46a1f72cf248f6bf550085d6c4da10d780becb44704ed5e46050090b`  
		Last Modified: Thu, 07 May 2026 17:57:11 GMT  
		Size: 69.9 MB (69885854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bd579428553633c42bc79b7e91125c840796d95b73a374a4ddd50c780715f8`  
		Last Modified: Thu, 07 May 2026 17:57:00 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
