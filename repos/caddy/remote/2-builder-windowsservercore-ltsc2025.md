## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:b629b28f5bd3a91e7704875f1141e8a6c1ea2c08f9c4b936eee2731f7a8b67b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull caddy@sha256:5dd7e11ecd46dc2a236f698d7542e0f19d020ae96d39e7b135c219f796083263
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3351893237 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d960da8a4d45ba99b8e16a6053d362300cb1494f4847367bd2db54630389a51f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 11 Nov 2025 19:13:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:23:01 GMT
ENV GIT_VERSION=2.48.1
# Tue, 11 Nov 2025 19:23:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 11 Nov 2025 19:23:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 11 Nov 2025 19:23:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 11 Nov 2025 19:23:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:23:15 GMT
ENV GOPATH=C:\go
# Tue, 11 Nov 2025 19:23:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 11 Nov 2025 19:23:20 GMT
ENV GOLANG_VERSION=1.25.4
# Tue, 11 Nov 2025 19:24:38 GMT
RUN $url = 'https://dl.google.com/go/go1.25.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6dad204d42719795f22067553b2b042c0e710b32c5a00f6c67892865167fdfd0'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 11 Nov 2025 19:24:39 GMT
WORKDIR C:\go
# Tue, 11 Nov 2025 20:16:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 20:16:27 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 11 Nov 2025 20:16:27 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 11 Nov 2025 20:16:28 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 11 Nov 2025 20:16:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 11 Nov 2025 20:16:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03b0dd942b2325bea867f58aeeb0af08752b535e7c2537bfab25eb44c3fdb8a0`  
		Last Modified: Tue, 11 Nov 2025 19:22:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1d9a7c57733598c262006db7cc864a6be8f74e4ad677025018444b66b84af55`  
		Last Modified: Tue, 11 Nov 2025 19:25:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d218b2e13e3d4cfe6cb49f852b6eb761b800684418d1037704bcbbf602e8343`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:286d99b5da106a868e2ce83dac0d213fb7a15c6507d832488c62a341b18d8a4c`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30a9624cd52cd3a3fd7ce42aeaca47ee244f771bcfe24bd1dbc48a163c4ec7aa`  
		Last Modified: Tue, 11 Nov 2025 19:25:00 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65e5d112ec160584d1a7494e606ec5ff969cb0bfc3f6325af5ed624d65c36956`  
		Last Modified: Tue, 11 Nov 2025 19:25:06 GMT  
		Size: 51.2 MB (51219091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e9681653760e2846782d64c03f4770cf19697d04f250a460fad237223a3890`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb4b1e7215f1022d263696481978d17bb18bfb9e5582f5afef1ba08b34bc4ee`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 345.8 KB (345769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9560800b103aa4813b55f7f3ef862c1aa8b8070d16547107a470dd77b62d66c`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a81600bf08117f42a9832ac12d7a83124dda09158f1ff798d15210632f10839`  
		Last Modified: Tue, 11 Nov 2025 19:25:13 GMT  
		Size: 62.6 MB (62565252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94e0407a4f61a29ea46f9188dd5ea02f1e0d017a9561bbae60be43a70e92ec5`  
		Last Modified: Tue, 11 Nov 2025 19:25:01 GMT  
		Size: 1.5 KB (1493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d4dcffc288b5dad20205182e17c873bbddb8272db79936f1604844a44ac2947`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff732c4a9d1d014a27ba034079eaae1f1c68587165d556eabf8b8e4b0f594676`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a48a167beac67e2c67b4c813599cf1683fe2dbcf8eb6426c40ddab10b57d03e`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e6dd144156a1c4a8abe786e810492daa8ce1fbf2ac551dd2d9a0e21cc7c80c`  
		Last Modified: Tue, 11 Nov 2025 20:16:49 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6cd15e2e6313c55dc1fbd2a160285023a74634e046b54f4ac26044c34e42a2`  
		Last Modified: Tue, 11 Nov 2025 20:16:50 GMT  
		Size: 2.3 MB (2290123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92dd04e7d1bc123010c3d24d3c47d8f830615685cae1dc5c9376bd0bbc9817ef`  
		Last Modified: Tue, 11 Nov 2025 20:16:50 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
