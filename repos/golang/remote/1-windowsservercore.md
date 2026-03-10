## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:e0cf0eb84e1a9a7305285c9965767ce089436f156bffba056b59c44b6c9d8d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull golang@sha256:1878b497e2b360e1d3549d5e36067763961c32dcadc070bd55f13077fa059c72
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2202591361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945dc1a9ac620b437f1753a84729b719ff457114acc07ec3b6cbd15a47279813`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 10 Mar 2026 21:57:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:05:00 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Mar 2026 22:05:00 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Mar 2026 22:05:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Mar 2026 22:05:01 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Mar 2026 22:05:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:05:15 GMT
ENV GOPATH=C:\go
# Tue, 10 Mar 2026 22:05:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Mar 2026 22:05:21 GMT
ENV GOLANG_VERSION=1.26.1
# Tue, 10 Mar 2026 22:06:46 GMT
RUN $url = 'https://dl.google.com/go/go1.26.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9b68112c913f45b7aebbf13c036721264bbba7e03a642f8f7490c561eebd1ecc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Mar 2026 22:06:47 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:158f9b4eb4f13cf841ba448566ccd79f22d7a8ca6bcd04fdb96cd2841e725493`  
		Last Modified: Tue, 10 Mar 2026 21:58:01 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537c58fb7d6a751d67b7371e24ce8226663f9217eacb731043dd2b73c112496`  
		Last Modified: Tue, 10 Mar 2026 22:07:00 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6bacc48570a713ce4f010416e60e52c8a550c9ee36efd079f8a6fe4d6f99da3`  
		Last Modified: Tue, 10 Mar 2026 22:06:59 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aaeeed7c63e20322a8d7311517fa65e57b1764b007458e759c5462b6f416df8`  
		Last Modified: Tue, 10 Mar 2026 22:06:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34aa9143f21f5416348d4437a34a725d5cd729524fa25522685e5b39bcfe18ea`  
		Last Modified: Tue, 10 Mar 2026 22:06:59 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2b4484cf7d31295b26e1ae322f9930bf2c7b6663b4c620012eba3119c3e9628`  
		Last Modified: Tue, 10 Mar 2026 22:07:05 GMT  
		Size: 51.2 MB (51220336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e06ed3ea7e9138b78745d00fd7f65e2c5a3c74c62b7e36f5fc72470616b6aa2`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af935961bb05c557aec8648fc00a747e08111ca5b6d6effc28e2db7223b4127a`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 343.5 KB (343519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a520c69ecc8202751ef255e3376b6c3e53cb8d57f3901ad6040cff68deb2d0f`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:beece69de6888783a8e4e26ac3c5a09f43ca50d4a3a09326cbc53d8b2c00983c`  
		Last Modified: Tue, 10 Mar 2026 22:07:09 GMT  
		Size: 69.8 MB (69820785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8369d2d0eb3f781b19f0e37e0f5f4d389a635dfe78b9f5b6b4329f2d3fcf8256`  
		Last Modified: Tue, 10 Mar 2026 22:06:57 GMT  
		Size: 1.5 KB (1464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
