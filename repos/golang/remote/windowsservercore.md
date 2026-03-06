## `golang:windowsservercore`

```console
$ docker pull golang@sha256:b0b0ff8dedac797bf1cfab22bd82660ba7d5cb49881a215fa08fbcc2a7f46c60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `golang:windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull golang@sha256:e1ff8af5d9f470140fcb5c9276a883bf238cc9235d148c26d8a31a0dff979955
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2086110974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75698ce5bf03e96d3cddcb4b71aaace01762dacb7fdc2c36f3051df7e4bc537e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Fri, 06 Mar 2026 01:13:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Mar 2026 01:13:08 GMT
ENV GIT_VERSION=2.48.1
# Fri, 06 Mar 2026 01:13:09 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 06 Mar 2026 01:13:10 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 06 Mar 2026 01:13:11 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 06 Mar 2026 01:14:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 06 Mar 2026 01:14:31 GMT
ENV GOPATH=C:\go
# Fri, 06 Mar 2026 01:14:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Mar 2026 01:14:36 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:16:23 GMT
RUN $url = 'https://dl.google.com/go/go1.26.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9b68112c913f45b7aebbf13c036721264bbba7e03a642f8f7490c561eebd1ecc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Mar 2026 01:16:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a32a00ca815963ac26bbcb9242b203e183799b826f587474745bc4aa7071edf2`  
		Last Modified: Fri, 06 Mar 2026 01:16:32 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ca62db19f36b64c1650314e5ed60c37019bb06941f0d523716675f4e83c141`  
		Last Modified: Fri, 06 Mar 2026 01:16:32 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79aedf49f78a754746105ef07507427ec5f7cb65adadb27857b3d78ebff88f6`  
		Last Modified: Fri, 06 Mar 2026 01:16:30 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dee44783f3f9cb543c067aba9ba73393074be168c90920eb774319d644aa8d61`  
		Last Modified: Fri, 06 Mar 2026 01:16:30 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a71520d15f23042633ce0ba641c0edf3b3f7b5d875793ec7252fbac028f8cf`  
		Last Modified: Fri, 06 Mar 2026 01:16:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f9b75cbb672545331a7486b08fd23b683ebf1c5b5276fd08ba14bb8ddbb860`  
		Last Modified: Fri, 06 Mar 2026 01:16:36 GMT  
		Size: 51.2 MB (51230166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a588cdde5f01a865e1bc1797bb8731456fa48e73e875bd0b047a55d29424c29`  
		Last Modified: Fri, 06 Mar 2026 01:16:29 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2adcdd3a73c34937e25cac3ad9715891ba96ef6f06c01ad9a6ea386fa9344c3`  
		Last Modified: Fri, 06 Mar 2026 01:16:29 GMT  
		Size: 317.8 KB (317811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d3f677a1a37fe380eed07d818aabfead64feef0d60c39aa2ae914a05f887bff`  
		Last Modified: Fri, 06 Mar 2026 01:16:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1bda43970eb113a008ead3ed1d4f09e0e31327b5ed62db90f0dd80cdc3607d`  
		Last Modified: Fri, 06 Mar 2026 01:16:40 GMT  
		Size: 69.8 MB (69792471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddb021ff090a9ee2a30bf78e78db6feab175af4fa8b8f84b8b744bb6e46f443`  
		Last Modified: Fri, 06 Mar 2026 01:16:29 GMT  
		Size: 1.5 KB (1484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull golang@sha256:0412b4b1cc4ddfa3dde339d98178ee7b5e458db87df881607b192c68284ae178
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1984152171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffa605904eb1f82fa6fc338cd2243dfc6244885181fe30a8bb968460745b529`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Fri, 06 Mar 2026 01:13:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 06 Mar 2026 01:13:33 GMT
ENV GIT_VERSION=2.48.1
# Fri, 06 Mar 2026 01:13:34 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 06 Mar 2026 01:13:35 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 06 Mar 2026 01:13:37 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 06 Mar 2026 01:15:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 06 Mar 2026 01:15:16 GMT
ENV GOPATH=C:\go
# Fri, 06 Mar 2026 01:15:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 06 Mar 2026 01:15:24 GMT
ENV GOLANG_VERSION=1.26.1
# Fri, 06 Mar 2026 01:17:20 GMT
RUN $url = 'https://dl.google.com/go/go1.26.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '9b68112c913f45b7aebbf13c036721264bbba7e03a642f8f7490c561eebd1ecc'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 06 Mar 2026 01:17:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6b46e01147629aa5972652465a2087c5dca5ba201622b37bcb7acb14b6f29e`  
		Last Modified: Fri, 06 Mar 2026 01:17:33 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2e0a21400459a8fd7e32de51bdb91b6fda5fa99b841786ce276ca4f6c524bf`  
		Last Modified: Fri, 06 Mar 2026 01:17:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451a422ec8564b9a534c9d0f6dd28f5a456eb9b315f24c4d92cb99dae6d07a5d`  
		Last Modified: Fri, 06 Mar 2026 01:17:31 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551bc6b8c0e0e1b4700ad616a28835d2e9e27944ab3cdb1f07e157f80ad29b7a`  
		Last Modified: Fri, 06 Mar 2026 01:17:31 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc46c30adb7b92922a2c8d2c8f3e616328aada42ae3147b1632105227af25e72`  
		Last Modified: Fri, 06 Mar 2026 01:17:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8487ce3041e40c0ff4c6ab9378fef95f2467c86dfe04215d88b578be383968a6`  
		Last Modified: Fri, 06 Mar 2026 01:17:37 GMT  
		Size: 51.4 MB (51359478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d004a1351c0c3f02c5616e97d6473ddb3e549f56de737350bfee5d403415abf`  
		Last Modified: Fri, 06 Mar 2026 01:17:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31183330f77dc175fa1469ba705f41ee62cf75c4d0f37cb6f5a020aaa089c46d`  
		Last Modified: Fri, 06 Mar 2026 01:17:30 GMT  
		Size: 320.3 KB (320313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4723ecbf795d6b30ecab73814b55507b32f12f3d788fc0fb46c43043f85d6367`  
		Last Modified: Fri, 06 Mar 2026 01:17:29 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44150fa901c8610dfaf9403ade1a0e22d306d84b86d7e94600360bc4b81bb7f`  
		Last Modified: Fri, 06 Mar 2026 01:17:41 GMT  
		Size: 69.8 MB (69804591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b687202bd17ab76d8a3ac529dc7d94020173062a06dd2f89bfc40de7da7b070`  
		Last Modified: Fri, 06 Mar 2026 01:17:29 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
