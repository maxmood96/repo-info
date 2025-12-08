## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:28f996eccb75df5a3e4499662791c076ed3653c26aa84cf72ba7ab964c981f2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull caddy@sha256:b059d64ed300816939b73ea17a062f4566f0b90184d4d1744914206dca9c8f2a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3351979296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ffe15640cdc274408d5b1573c595a9c61da08ea7da2567cab41cebf96acd61d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 17:47:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 17:47:47 GMT
ENV GIT_VERSION=2.48.1
# Tue, 02 Dec 2025 17:47:48 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 02 Dec 2025 17:47:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 02 Dec 2025 17:47:50 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 02 Dec 2025 17:48:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 17:48:28 GMT
ENV GOPATH=C:\go
# Tue, 02 Dec 2025 17:48:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Dec 2025 17:48:33 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 02 Dec 2025 17:51:00 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Dec 2025 17:51:02 GMT
WORKDIR C:\go
# Tue, 02 Dec 2025 18:12:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 18:12:58 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 02 Dec 2025 18:12:58 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 02 Dec 2025 18:12:59 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Dec 2025 18:13:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Dec 2025 18:13:06 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038179540c4b5bff54de1043c1801d521b53ebe92fd131623177c8ab3e5b6d87`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ac94f8017cb2897ec8c7b4a364d24e0de9b6ac03074907bedc69cddc08b35da`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f554ee569e72050d229b07d0ae457307eee760a7c8c947c44f4c392f33a5e9`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9856541e5702000461917f2b88924a9219eba9858435827133c1889a768779a8`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a3f1f2051dfeded04719c7da15c10f4446ed60a2bd37e1af4dbf690bc9d3529`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758542b365d1f7a0b7e649d055d124d6e79bce402223c28a0db8b57f362c3ca4`  
		Last Modified: Tue, 02 Dec 2025 18:00:15 GMT  
		Size: 51.2 MB (51240483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d8698f68d7d54c14ad9ac4657eacdda4a694c31726d4b17c82ed06aa3644cc5`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f08a1e7f7944207640262ae0124487391591ee14934148ccd95ff257223e071`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 364.9 KB (364909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8325f8a13aba0057ad7964f76545732ab485ea8a4db4231388fbc70ee772a4aa`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4129a1f5bd9a814437667d1fc8b72a89fd849469d76b6d7ee78c3eaf4d0d52c`  
		Last Modified: Tue, 02 Dec 2025 18:00:20 GMT  
		Size: 62.6 MB (62591300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7d867d536660e28f9277f6eaf18168efe5500e4880a872afd740e3b92da532`  
		Last Modified: Tue, 02 Dec 2025 18:00:09 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e00d2e18b31bd8c4b194a5d873718232d64f4148c2bd01b65a9c6cbf440cea`  
		Last Modified: Tue, 02 Dec 2025 18:13:21 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c76c004b285cc5cc835452e534795896226c81188da9ecec96c54bddf5c2c6f`  
		Last Modified: Tue, 02 Dec 2025 18:13:21 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11002b33dcb59b16a37e876556a759490ab4dfce571001333c2b5f5819f81aff`  
		Last Modified: Tue, 02 Dec 2025 18:13:21 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5f1a2a8781d98a563a0112227f039b886f30c7a4e701c020542243633e057e`  
		Last Modified: Tue, 02 Dec 2025 18:13:21 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56995eaccd938d2c7b6ad4790d194c02db31da04a65998abc36678322653c966`  
		Last Modified: Tue, 02 Dec 2025 18:13:22 GMT  
		Size: 2.3 MB (2309564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:270c9dc8b158773b15cace6bb6cc814ee6116bbe3d66776ee326405ec86b00ee`  
		Last Modified: Tue, 02 Dec 2025 18:13:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
