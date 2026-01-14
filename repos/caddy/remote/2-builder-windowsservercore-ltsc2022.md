## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:3881070da9bf34baeb8e1bec802fcde355e652955af1e38bf94f116dda1b6649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull caddy@sha256:0fd3b216c9aaa93c5fe480ad8c6bac94bf487b80a4fe4c173554fdb3a260e350
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1952225777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a9432f7606a5e258ac8bd58f1c525a0276ae8a57c34b322fcc4b6168a3acef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 09 Jan 2026 00:11:24 GMT
RUN Install update 10.0.20348.4648
# Tue, 13 Jan 2026 22:53:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:05:43 GMT
ENV GIT_VERSION=2.48.1
# Tue, 13 Jan 2026 23:05:43 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 13 Jan 2026 23:05:44 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 13 Jan 2026 23:05:45 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 13 Jan 2026 23:06:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 23:06:05 GMT
ENV GOPATH=C:\go
# Tue, 13 Jan 2026 23:06:13 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Jan 2026 23:06:14 GMT
ENV GOLANG_VERSION=1.25.5
# Tue, 13 Jan 2026 23:07:54 GMT
RUN $url = 'https://dl.google.com/go/go1.25.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ae756cce1cb80c819b4fe01b0353807178f532211b47f72d7fa77949de054ebb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 13 Jan 2026 23:07:55 GMT
WORKDIR C:\go
# Tue, 13 Jan 2026 23:39:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Jan 2026 23:39:37 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 13 Jan 2026 23:39:38 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 13 Jan 2026 23:39:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 13 Jan 2026 23:39:59 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 13 Jan 2026 23:40:00 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8810874280ba2ea58e95647ea717ead1a5fb07fea1d9160047d580e653fe9cbd`  
		Last Modified: Tue, 13 Jan 2026 18:28:58 GMT  
		Size: 346.6 MB (346640075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f681901ae8b8270ef4ad40879b419cd45d092d5d347a675266218039d5b88a0`  
		Last Modified: Tue, 13 Jan 2026 23:01:20 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5e569184978b2c13767241543e1a184b8a6a6f3f59ba7fba3032a6a05912a6`  
		Last Modified: Tue, 13 Jan 2026 23:08:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f642f93c5eb552b61b88fa7f0395a9878957708678d7bc56ef4deb6ba618eb91`  
		Last Modified: Tue, 13 Jan 2026 23:08:23 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94aa54b3f3766b23fef0ffe775810d0c15c545c305edde7ae3dc8229e57c780`  
		Last Modified: Tue, 13 Jan 2026 23:08:23 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb3ad241c3ebeac775041ff53e7a7fd80f784efd4703ca690d8d3d5f6576b4d`  
		Last Modified: Tue, 13 Jan 2026 23:08:23 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febb97db327dd1c6dc79f7b9463eb535e1a141d82f6014efa85fab0790148f58`  
		Last Modified: Tue, 13 Jan 2026 23:08:28 GMT  
		Size: 51.3 MB (51349162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf0651e38a15f552ebb0ec7a2a10d24cbf2d4b3146015ef70fb75b249f9e628`  
		Last Modified: Tue, 13 Jan 2026 23:08:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a563008a47ab8d4d6a51d6b4a21d7c2b965cbe290f219c63f724ce0dc90b782f`  
		Last Modified: Tue, 13 Jan 2026 23:08:23 GMT  
		Size: 340.5 KB (340511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2debbef074ef36f2a41d4ebf0b2e121a9256a02d616e7b21616f54c75be673`  
		Last Modified: Tue, 13 Jan 2026 23:08:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bae741c06c7f5c3cc6a50e49b9c9c573ff473520afceb83a146dad0d98649f7b`  
		Last Modified: Tue, 13 Jan 2026 23:08:32 GMT  
		Size: 62.6 MB (62566951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77113cdbe8cb62f8def0ba7b006c0874c2a21fd7d91c6c3c79bc8da001d7fddb`  
		Last Modified: Tue, 13 Jan 2026 23:08:23 GMT  
		Size: 1.5 KB (1471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7ab4c6afc9fb825e9376b5c778c8275dbd978b2318ec43bcbb36dd527c7b85`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ca20e68dd8ec6da2dfa0afede875f274c0bb99a5c8c19edc77e5f1062e0934`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca8a89c57a54842de3404280026fdd6762c0fb2f2f16518021304d30621d03a2`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c17978e2dc6851fc0025d49100d72be8d8713ce67877e3a680a2d0c65a4cea80`  
		Last Modified: Tue, 13 Jan 2026 23:40:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd057a093bfaaac730c95beed2d10236a7498379d1f733ce6fc4baf3719316db`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 2.3 MB (2292797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3204edf7b9123a85dc33a893df5d038fb1c2d858562f824c3f5100f5f39cab`  
		Last Modified: Tue, 13 Jan 2026 23:40:14 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
