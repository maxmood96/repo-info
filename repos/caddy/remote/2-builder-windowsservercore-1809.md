## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:519892ed48355c6127534cc7069ac38b64bb944fbfe1ed213cccf982533a2e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull caddy@sha256:8a0ebbad06b9122718baf1979bbb5f22f4884fad3015ccb5f2063fadce18bbea
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2261446143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a50b09728da69a74e81194284fbf40f618d6bb6efe38d28e2387bed3de2c8e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:38:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 01:10:34 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Apr 2024 01:10:35 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Apr 2024 01:10:36 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Apr 2024 01:10:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Apr 2024 01:12:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 01:12:15 GMT
ENV GOPATH=C:\go
# Wed, 10 Apr 2024 01:13:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 07 May 2024 18:30:02 GMT
ENV GOLANG_VERSION=1.21.10
# Tue, 07 May 2024 18:33:41 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 07 May 2024 18:33:42 GMT
WORKDIR C:\go
# Tue, 07 May 2024 19:51:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 07 May 2024 19:51:09 GMT
ENV XCADDY_VERSION=v0.4.0
# Tue, 07 May 2024 19:51:09 GMT
ENV CADDY_VERSION=v2.7.6
# Tue, 07 May 2024 19:51:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 07 May 2024 19:52:58 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.0/xcaddy_0.4.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('4798dd7a73be99b4c035816af6f59d807014828bbe45e673a6b79182d3a9ecded48dd453691f02d178481c62787f53b3703e5a4e1d69b2b78cb9644f2e56dcf7')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 07 May 2024 19:52:58 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31d438ec04c376f7ffff3d4a16e8eb5f805f6f7cd5441a903c7b428c670212f4`  
		Last Modified: Wed, 10 Apr 2024 00:46:06 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:843b97b1625fa02e123dfc05bebcf9f05077e6dbdd1f5253c3c6d07b95f0f55f`  
		Last Modified: Wed, 10 Apr 2024 01:35:25 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6532f7333203cbc41355f91a4431427f575a24ad3dc3dd393b4292b4c2660d76`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c34d692c7e9d5e97e4674c9fefa41e1c78447d2e9c8db3a3f94f325b6188af`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cead4e65b4492e37b01dc6043de135f9dfad18c9f01232c605eb59e7da4a98`  
		Last Modified: Wed, 10 Apr 2024 01:35:23 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7638380d4eb3933d8241dfe83deaffc516e8bed7b2ab01f96b42864a0d722760`  
		Last Modified: Wed, 10 Apr 2024 01:35:27 GMT  
		Size: 25.5 MB (25535896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159dd7a1de12391b28b5260b6132a515d19e87a7e18b64d7bc843df2c26fb615`  
		Last Modified: Wed, 10 Apr 2024 01:35:20 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004df08705794a49d57aabf8c97ae8dfe750cedd45eb476bd574ce29807e152`  
		Last Modified: Wed, 10 Apr 2024 01:35:21 GMT  
		Size: 263.3 KB (263307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5155135be95d0425a26e9a6756eab6fcb7ce32b3da3ec6a9db1485c2c78eff3`  
		Last Modified: Tue, 07 May 2024 18:42:15 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daf38e9da6691cf80389507abf857bcfb706187c2b18c4e2a3ab8e4b3063646a`  
		Last Modified: Tue, 07 May 2024 18:42:35 GMT  
		Size: 69.4 MB (69375247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:509dc5d2c9595878a2be9c59477fa20f85a091b8487b851002790ce02d2f9ca0`  
		Last Modified: Tue, 07 May 2024 18:42:15 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7838970dbdeef02f21288d6db681e306dfdc01c4dc1ae6cfc9ef622e756b519`  
		Last Modified: Tue, 07 May 2024 19:53:02 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df46a1918824e05097fd94f1b524036902e160317d38fefe99a5b844f615e945`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09235c54ab4d87e6ab2118af9a30d5302e8b6c1c41ec21034cb9fbbcc4e6ac5c`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28654f43884cdcfaa7d06ef6abb025001024fc4de7e69e20fc9f86d8bc5ebac0`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6adfa503ae8bdae9fe79a0376d70a98d4b88de51af55749647bec695ebbb71ce`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.8 MB (1826193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d965ef39a682845e20ce13e9931be75037023f073f2a54a86bec23a1d034ca`  
		Last Modified: Tue, 07 May 2024 19:53:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
