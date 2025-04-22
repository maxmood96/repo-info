## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:232c3fb379ab59b5815d9960222a90500214ba9177a4a884b2e95d3e4fad9e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull caddy@sha256:a7ea1ef1309f1b533604f9e47fd8f46e9273b672a5b9143519518acb12aa4d62
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296732556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bdf67b4ebde66b6747e9843e7fe550b06f0fe3c24c1c4254757b566d9ad6a2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:17:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:17:07 GMT
ENV GIT_VERSION=2.48.1
# Fri, 18 Apr 2025 03:17:08 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 18 Apr 2025 03:17:09 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 18 Apr 2025 03:17:09 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 18 Apr 2025 03:18:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:18:03 GMT
ENV GOPATH=C:\go
# Fri, 18 Apr 2025 03:18:09 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:18:10 GMT
ENV GOLANG_VERSION=1.23.8
# Fri, 18 Apr 2025 03:19:19 GMT
RUN $url = 'https://dl.google.com/go/go1.23.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'e0ad643f94875403830e84198dc9df6149647c924bfa91521f6eb29f4c013dc7'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:19:21 GMT
WORKDIR C:\go
# Mon, 21 Apr 2025 22:44:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 21 Apr 2025 22:44:13 GMT
ENV XCADDY_VERSION=v0.4.4
# Mon, 21 Apr 2025 22:44:14 GMT
ENV CADDY_VERSION=v2.10.0
# Mon, 21 Apr 2025 22:44:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Mon, 21 Apr 2025 22:45:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Mon, 21 Apr 2025 22:45:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc58abf569d39be3c925dc5f3f86dc1a988b54666b1ef1e12e53e7a71ceee179`  
		Last Modified: Fri, 18 Apr 2025 03:19:25 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:830f09db3a63bcefe67c5e4c9edf039dd6ae6d2659ad1a8c73e98ad7cba6f5f6`  
		Last Modified: Fri, 18 Apr 2025 03:19:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:714665fd638a59d67ec9f069d157ce0dce974ed7c9285c968cddc8627580f434`  
		Last Modified: Fri, 18 Apr 2025 03:19:24 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad74e1639eca81ea7f6918389decfcbd99eff8cc06d3b45df134905fe3ee644`  
		Last Modified: Fri, 18 Apr 2025 03:19:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4aa0dd71bcec799d3139dbf32c3b593be611239852195e362549d5ef53b12f`  
		Last Modified: Fri, 18 Apr 2025 03:19:24 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b03fb9f9ed271b4b8ba462e9599108f4f231edd3e9e31882613bf832581c5da`  
		Last Modified: Fri, 18 Apr 2025 03:19:30 GMT  
		Size: 51.2 MB (51198821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3807dff106c6843be9a5701c1480f12b6adc9107b47aa9ea3ebb5d581578496d`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b8fa9bc2097fbe08d4713ba5b159b9111273e3cd51f3277f14ae56ed5dd74f`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 332.8 KB (332775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61592680fbb790793d61381979f3bfe77e4832b89285cb3f7574a7f00dca59d1`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88a6a4c6fe241e1cb17c9b14ce9eaaab1556394d408c7d194990d713b0b6584`  
		Last Modified: Fri, 18 Apr 2025 03:19:36 GMT  
		Size: 77.4 MB (77368125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac59c8176cabc693d38bb28cba053ca9b77e720f96eaa27ee36b62afedcbf233`  
		Last Modified: Fri, 18 Apr 2025 03:19:23 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233522a12b15b4ae3cc5ca6ed917af92ea0cdc99907df28370189264a45118ad`  
		Last Modified: Mon, 21 Apr 2025 22:45:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5210a01ed7decd576dbc999955e6a08f084c4ab3d9286c47c391cb32f4bfde28`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f018eddc2a100b41a8ee2c91defbcea643392feacc69e79c3be0ed377eac3b01`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b3f012693f4b9779457c37af2b07e24dbe97d1fa6d8f47a55d17c93eca2cca`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d43af34798a541997ea8b16ad84b185ae0f3f847ba4abff7dc62c1efd86dcd5`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 2.3 MB (2289949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27535f88ba33f080f88664920c0b5216b85d8acccfa68614c8430d654d4ead02`  
		Last Modified: Mon, 21 Apr 2025 22:45:06 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
