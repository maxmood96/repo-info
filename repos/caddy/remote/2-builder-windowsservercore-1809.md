## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:d9056f7c8ccc04e12cf3daf31698cdcf5f083170891372f94d61c8da6db21187
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:5a908c8e961d324c5675ab4c2ab96d32fa02aa4f5989320b06753099bd224455
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2276876401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c05c04fbdab0842c80fc8d1fc925f4ffca4f1ca02e89371883ffc6d7ce887b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 21:51:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 21:51:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 21:51:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 21:51:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 21:52:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:52:47 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 21:53:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 21:53:20 GMT
ENV GOLANG_VERSION=1.21.10
# Wed, 15 May 2024 21:56:21 GMT
RUN $url = 'https://dl.google.com/go/go1.21.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '09170b66e7d7c4e2e7a30b8f3350778a8ba5c15951b7eb8ff7545cb86ea9bb71'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 21:56:23 GMT
WORKDIR C:\go
# Wed, 15 May 2024 22:53:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:53:36 GMT
ENV XCADDY_VERSION=v0.4.1
# Wed, 15 May 2024 22:53:37 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 15 May 2024 22:53:38 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 15 May 2024 22:55:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.1/xcaddy_0.4.1_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('b058280b1e15e0915c541bc8a3aefc2289155c38a9fbc2f8d6b05267f9d0469eae5be2a9312d52c5ba41c7dbcb18c0970efa5b1df628655cca81b55d5c51d9e1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 15 May 2024 22:55:09 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:896e983a0a4309b805accb8ae63327cc1f3b8f992e0d75b555a5c61d02fed986`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1c7744622a8e10412cfb393caef5a301667c3db556da9fd3857c72be60fcdc`  
		Last Modified: Wed, 15 May 2024 21:56:31 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b652aa3eb2aa15638a8e9f572497cfd1fb6884ebeeb6ecdc9074aad63f79a69`  
		Last Modified: Wed, 15 May 2024 21:56:30 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:148c74e800af547d1d14d91f5b9c167f17c75e65d02f875b5ae130c570d83299`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53bccf2db4b47631e2d74d6e6ad17ebb28e6387c6e6c884011fdde2bf29fac7e`  
		Last Modified: Wed, 15 May 2024 21:56:29 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f83d4419852279e679aaa47097723ddfa68affbce518a5f31fe47caabc8b251d`  
		Last Modified: Wed, 15 May 2024 21:56:32 GMT  
		Size: 25.6 MB (25575407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8509005ef5150522ee2b4ded57557935baf2a14c34cc5d25b2241d935a81284a`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1477c6f08b1aaca7cf172e0b0e9b08c945114f3cfca719b6d9479d28377627da`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 346.4 KB (346387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdd971ba008fee57e5da9f3e4bc2084142f53a330c099ed32492c660baebc4af`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3866e6ca6d2695e04b9a5fdb00612bf63b2a25f82548a42a0e9ea44defcc619`  
		Last Modified: Wed, 15 May 2024 21:56:38 GMT  
		Size: 69.4 MB (69400042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:063360e32b8a7b88e36a87b59c4cdb689ee9bce85fff56da69f8a0953db6a9c3`  
		Last Modified: Wed, 15 May 2024 21:56:27 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517e5d69bc86420b8e423d4fd9afd5e4138c87c06149927fb1ada38053147657`  
		Last Modified: Wed, 15 May 2024 22:55:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c1d817dc7c4f2d1ed65b8ebe3020056e330b2880f3ad70d0802de6684feb54`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf22c592153e6d7c1e0037379a2ec28694088ec9e283ef66024397d93249165c`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b46c8b9479856498dc80f87da766924b2bbb9fcd9f7ecaf9e84245241ac743a5`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46e3a07a3c56d5582fc71b9183eadde4dc83368be6d164ae5c95c4a9f4522234`  
		Last Modified: Wed, 15 May 2024 22:55:14 GMT  
		Size: 1.8 MB (1826095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677fb13fe6786ac8f8b9f709a8cfe6db6074ad603b3a45efe55fa8c478e22766`  
		Last Modified: Wed, 15 May 2024 22:55:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
