## `caddy:2-builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:490d6428ca3071208ea0869c77f4b8b020e011b1189a8a4ee94475d9f2e375fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `caddy:2-builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull caddy@sha256:266f66153e5728a118fe06baba2f612f6c7430fce8e8ef10f94a7f961eb96dec
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1612413343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e79f97d12cf027e03a6ed1d1457c0f8c3201872bbcae25d5c40ee465b77ac67`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 06:35:44 GMT
RUN Apply image 10.0.26100.32230
# Wed, 04 Feb 2026 17:09:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 17:10:00 GMT
ENV GIT_VERSION=2.48.1
# Wed, 04 Feb 2026 17:10:01 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 04 Feb 2026 17:10:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 04 Feb 2026 17:10:03 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 04 Feb 2026 17:10:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 04 Feb 2026 17:11:00 GMT
ENV GOPATH=C:\go
# Wed, 04 Feb 2026 17:11:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 04 Feb 2026 17:11:06 GMT
ENV GOLANG_VERSION=1.25.7
# Wed, 04 Feb 2026 17:12:27 GMT
RUN $url = 'https://dl.google.com/go/go1.25.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c75e5f4ff62d085cc0017be3ad19d5536f46825fa05db06ec468941f847e3228'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 04 Feb 2026 17:12:28 GMT
WORKDIR C:\go
# Wed, 04 Feb 2026 17:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Feb 2026 17:51:55 GMT
ENV XCADDY_VERSION=v0.4.5
# Wed, 04 Feb 2026 17:51:56 GMT
ENV CADDY_VERSION=v2.10.2
# Wed, 04 Feb 2026 17:51:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 04 Feb 2026 17:52:19 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 04 Feb 2026 17:52:20 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:e8e286c160e014cebd84213d5cfa83952f5927713def450860146ee76600ee3f`  
		Last Modified: Tue, 13 Jan 2026 18:49:06 GMT  
		Size: 1.5 GB (1495760247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0ca9c86a705f58dbc5b545175e27e5e37766e10b3f12eeabd44caff11efa5`  
		Last Modified: Wed, 04 Feb 2026 17:12:42 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e499bb41ea2ee6826b550d07a26576199995701378f04f8fd311f860e5498a3`  
		Last Modified: Wed, 04 Feb 2026 17:12:42 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a005dfb58609e4e8ce8de3ec9360a81b51137963a749610ff1d46ef75477dd`  
		Last Modified: Wed, 04 Feb 2026 17:12:41 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6fbc05539f831c9c45349c2aaaadc887e6e799f00bf4a4b4c44562981fdc71`  
		Last Modified: Wed, 04 Feb 2026 17:12:41 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fdb8f997f4f44fba880e29c37d9be8680c350303cca74d9c43ae1888ecbc11`  
		Last Modified: Wed, 04 Feb 2026 17:12:41 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ac274f4427ab6980702746b2a49be6cb4cdce3ea353f39a3688506c894822ba`  
		Last Modified: Wed, 04 Feb 2026 17:12:47 GMT  
		Size: 51.3 MB (51264713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62d138ab20880bb60281796d095bc8dbb43708f79541f985fc2585ab770d07c`  
		Last Modified: Wed, 04 Feb 2026 17:12:39 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105fe71e25097160afa6c6bbf04b00f7cfcc4e2a479439568b4a715e7d577635`  
		Last Modified: Wed, 04 Feb 2026 17:12:40 GMT  
		Size: 403.4 KB (403359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:889648476a657c9de440693f6a7b89c70891c85866b6ebbafd132d4a92def4ef`  
		Last Modified: Wed, 04 Feb 2026 17:12:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef413425c91b6d357d827848da0c9b3c67209ecc40091e76b1e0c53470329ec2`  
		Last Modified: Wed, 04 Feb 2026 17:12:51 GMT  
		Size: 62.6 MB (62625752 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a37e896ee43b80530a21a6597c19f5fece282718295ebb59a1ac191ffc4efc`  
		Last Modified: Wed, 04 Feb 2026 17:12:39 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e08c8bf079de54471a746cb47b003bf4c21311a6cc2709b7727dfcec6fb7ffb`  
		Last Modified: Wed, 04 Feb 2026 17:52:29 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ed74d151c3b058471d4f9a4347a0a0f3bced5c1262c7d2d9cecea2a104bd92`  
		Last Modified: Wed, 04 Feb 2026 17:52:27 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11c43db62f9ccfae38740ae5a831d16ae5cae60f92ec94ef7422ca23939f4696`  
		Last Modified: Wed, 04 Feb 2026 17:52:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4966aa2b4be340e134d20f8ea77170b8fab9f8701ed648ed40b14a21061a993e`  
		Last Modified: Wed, 04 Feb 2026 17:52:27 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2787b8b338024cbf2c1f0dcede528666ee35e0ac2e1e5f4f11e485200e5ecfe2`  
		Last Modified: Wed, 04 Feb 2026 17:52:28 GMT  
		Size: 2.3 MB (2342000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b258bb9e3ccd042b26c37c97310a6e10efd9049469f1b71424bc8baa9f434926`  
		Last Modified: Wed, 04 Feb 2026 17:52:27 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
