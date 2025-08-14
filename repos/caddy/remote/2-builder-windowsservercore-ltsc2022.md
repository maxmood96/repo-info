## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:98650c41b16ddc5cdf10cd25a093c890ed65791f69550795b93fe45b584dd99d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull caddy@sha256:59e32a2c62a2a8096734cd20064a3e705aa3bc1e02d6230b44baca9586ba0aa2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2413068133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48e38cc248c3ec7778c000be8a681be71ce66b4f8e0f419b4c023772380e3a8a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:32:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:32:48 GMT
ENV GIT_VERSION=2.48.1
# Tue, 12 Aug 2025 20:32:49 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 12 Aug 2025 20:32:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 12 Aug 2025 20:32:51 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 12 Aug 2025 20:33:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:33:15 GMT
ENV GOPATH=C:\go
# Tue, 12 Aug 2025 20:33:22 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 12 Aug 2025 20:33:23 GMT
ENV GOLANG_VERSION=1.23.12
# Tue, 12 Aug 2025 20:35:17 GMT
RUN $url = 'https://dl.google.com/go/go1.23.12.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '07c35866cdd864b81bb6f1cfbf25ac7f87ddc3a976ede1bf5112acbb12dfe6dc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 12 Aug 2025 20:35:19 GMT
WORKDIR C:\go
# Tue, 12 Aug 2025 20:50:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:50:13 GMT
ENV XCADDY_VERSION=v0.4.4
# Tue, 12 Aug 2025 20:50:14 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 12 Aug 2025 20:50:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 12 Aug 2025 20:50:23 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 12 Aug 2025 20:50:24 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f354c5b18541063a761d6dee95b9d0e361a7747e2c0a61fd7e412a70620324e`  
		Last Modified: Tue, 12 Aug 2025 20:37:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee4ce2fb7b62d7b1eaecc0577371e9a3e12e6b2750cc615a5f0b3e041d7b405`  
		Last Modified: Tue, 12 Aug 2025 20:37:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5649597aafc43db49d2358a893a5b8ab2d1cd664e737b5e2a0b2d1af8db651`  
		Last Modified: Tue, 12 Aug 2025 20:37:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f23a13d4b97640ab5032908c089cab51b08bea62bad0978ee446924a7d24c0`  
		Last Modified: Tue, 12 Aug 2025 20:37:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a355f756e8f31a07296b34dfcba39fcee4fb4e18f8d3cb971f954ac3152c486`  
		Last Modified: Tue, 12 Aug 2025 20:45:14 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:174410844527a91915e352aae834357c5d8bf1d05eba5e53759be40fae464a1a`  
		Last Modified: Tue, 12 Aug 2025 20:45:19 GMT  
		Size: 51.2 MB (51199562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3a0ebf296cff4fd0336eadffc44a7bc483884b4bf49c9897772671d55588e3`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5542734c0a5be96eff23b709552fd9a7d1ff2f665e6af0491d5f2d43a0721f`  
		Last Modified: Tue, 12 Aug 2025 20:45:15 GMT  
		Size: 335.9 KB (335914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3036c9889dc3924d3b4465b24eb4f517fb24905d6bb1ce7f8e24ca138c4820db`  
		Last Modified: Tue, 12 Aug 2025 20:45:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a341df05c369150ecc09f34589094000e03f1453652d6f6e85d9287e546db251`  
		Last Modified: Tue, 12 Aug 2025 20:45:23 GMT  
		Size: 77.5 MB (77518403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8653684d8a1edeb98d39bd10be23b50cff921bd94e7621188990796ea8cd6000`  
		Last Modified: Tue, 12 Aug 2025 20:45:20 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b158cb82013282bf643b8239c08506dd9b65054471a041b6c545402ad43544a`  
		Last Modified: Tue, 12 Aug 2025 20:51:05 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e292a29b348538a8383f9b575bf4706dc55071292937b77fb56120f93eeaefc`  
		Last Modified: Tue, 12 Aug 2025 20:51:06 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d9d0a667d4d82a9b99bc5f2a0357af6538dd6fda33855c351e86d3770ebe0e`  
		Last Modified: Tue, 12 Aug 2025 20:50:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3497940730cd75355cef34feeff5be3f2a8bdba45a64e1c486c383bd89b6794b`  
		Last Modified: Tue, 12 Aug 2025 20:50:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072688390e9c5534e6775a7f44cb169a681de7001effbfc242d343025e532b21`  
		Last Modified: Tue, 12 Aug 2025 20:50:54 GMT  
		Size: 2.3 MB (2305441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a9578652627834e5b023c05c3f79dce2ffe1938031befc94f1ded17f452308`  
		Last Modified: Tue, 12 Aug 2025 20:50:54 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
