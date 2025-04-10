## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:21203647bfb26d910918c71ead1d02d9b29255fd98fcf31c4198ca81a9527371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull golang@sha256:e29fa934998590e81186bb08c40a15164560e42544d807437c6f89eb5bc9fae2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3528792761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816853d92bdc97451867ed14d5a594511d44b99ac051a03661c3f2e86f17150b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:44:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:44:04 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:44:05 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:44:06 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:44:07 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 00:44:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:44:21 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 00:44:28 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:44:28 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 00:46:03 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:46:04 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7672cf33de477ad825cbaa16a956e9d5d339db68a30efa7b3ff24ea6fbd02846`  
		Last Modified: Wed, 09 Apr 2025 00:46:09 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89fc7c6dd17b7d72b3a1b65f71da98a86a10e9a2f62f51700a42682ce4268914`  
		Last Modified: Wed, 09 Apr 2025 00:46:09 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e132aab1dd805923e52f664ee264e6f42963c7e99a6037ab371c2d54ca76b32`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62eb12eeebab81f5162a35e2db0fc603735dbf320dfdbdc094656656cda055da`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e27a60939c03ad6bcc785a1bf280189f4e112281d56c5356ca4876e4c7acd78`  
		Last Modified: Wed, 09 Apr 2025 00:46:08 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a77c9a310a4f142c5098362986c6c9975ca2b1243431d56e12055fef19d49ea`  
		Last Modified: Wed, 09 Apr 2025 00:46:14 GMT  
		Size: 51.3 MB (51253178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0312c7451731be32488e49beb94106a26ff17993a360c0b06498474fa488521c`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8727a8f7c608ffd128685607cf14b845cd5148598a30250657b78a7727fce963`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 378.0 KB (378041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c156426602a359ef6dae2b64d5ce0a2145b84588c901063d41fd0f1713dd5eca`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7906439a638b42ec85dcdd3b2205effee08115f7f42d2dcf9f1a5f2103a07f40`  
		Last Modified: Wed, 09 Apr 2025 00:46:23 GMT  
		Size: 82.5 MB (82471510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e79a665256513d99d621933d5f1489cdfb9bab3495509e0ec43766fe85ced9`  
		Last Modified: Wed, 09 Apr 2025 00:46:07 GMT  
		Size: 1.5 KB (1473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull golang@sha256:f50a62a024e851fe1d9684010d18b6dd3db48288cfeeab250726d1e7423e66ad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404810921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89491f6a50d6ba7c3221a93691258c9181e343d5d9ef694d4f372a183832f4fe`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:59:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:59:51 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:59:51 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:59:52 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:59:53 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 01:00:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:00:11 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 01:00:17 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 01:00:18 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 01:01:28 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 01:01:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4345c6a4265223fc889b761aac9cfe0402e9e7ba36ff92c9041a7e01af827238`  
		Last Modified: Wed, 09 Apr 2025 01:01:38 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9c0bc025e49b96a98e158aa3628492681560a9b66371cafa674a13baffb2a0`  
		Last Modified: Wed, 09 Apr 2025 01:01:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b147f042085899dbe15fbcbc97b157dadc056218a793c091f8da26fc35b080`  
		Last Modified: Wed, 09 Apr 2025 01:01:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88330bb9180b967b8f1ddf3ebb374d770def047428f52d4735e71e7a99e5c150`  
		Last Modified: Wed, 09 Apr 2025 01:01:36 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414252e9ec98fb3ee28bc6c024d35e323011170f9662b4e95d501f8494e2cb7`  
		Last Modified: Wed, 09 Apr 2025 01:01:36 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ad7c06935374ce4f49b6691c8491cb0a04fbe87314498c7a0eb0fc56be2052`  
		Last Modified: Wed, 09 Apr 2025 01:01:42 GMT  
		Size: 51.2 MB (51209846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2bce03b9acb963d134c3f4e69e3472732ebccc067518a62e69db5353b82f613`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181b8f7ca8d16a5332510aa93def630fd3ea6b003489ed120843ba48a1c9bbf`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 344.1 KB (344106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57de3a3af62347b91455ddc9ebaad5b04aa71cb5c9a01aba9f633e99f023e0cc`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:242c423f37cbf4329c08684df4d886ef6f2fe1db3fb69c651eff20ee85a345d8`  
		Last Modified: Wed, 09 Apr 2025 01:01:47 GMT  
		Size: 82.3 MB (82250859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d64572c273c292cc9d00c8b1835d833c74c4589a70b2fd6536b3220a1c960`  
		Last Modified: Wed, 09 Apr 2025 01:01:34 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull golang@sha256:c110fb0a7415f00e732b5f9860b22ebbd55f43922f9c757dccef79ac84670c1f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296500885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e256c32d2bf069c4f461bce58676a4e23a841fd285d364090db8b212699bc788`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:54:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:54:21 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Apr 2025 00:54:21 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Apr 2025 00:54:22 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Apr 2025 00:54:23 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Apr 2025 00:55:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:55:14 GMT
ENV GOPATH=C:\go
# Wed, 09 Apr 2025 00:55:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:55:21 GMT
ENV GOLANG_VERSION=1.24.2
# Wed, 09 Apr 2025 00:56:35 GMT
RUN $url = 'https://dl.google.com/go/go1.24.2.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '29c553aabee0743e2ffa3e9fa0cda00ef3b3cc4ff0bc92007f31f80fd69892e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:56:37 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02d2e4cd82e1486d8c37ceea51a0f0efaaf886c079dcbf2934f7ece112c6b90`  
		Last Modified: Wed, 09 Apr 2025 00:56:41 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15093f0690bdd7424b0b96331ecc38bdd6301e6a63b3d5e70cf90d7c1ee4b1e0`  
		Last Modified: Wed, 09 Apr 2025 00:56:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c7926e8a15a554949994c42bdfc849f5c59edd204b8b2169a45044a654e0f`  
		Last Modified: Wed, 09 Apr 2025 00:56:41 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22a8386bdc4d78f1288691ecd130bba3666993f6b7e16591cf4bfef191dd364`  
		Last Modified: Wed, 09 Apr 2025 00:56:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aea277ef6f3962d14e126a8a4f1af0f399e4677c41003870ca28e2cae932650`  
		Last Modified: Wed, 09 Apr 2025 00:56:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518df7556a6bcb9c71a812f8da756e173d093dfb12ce99ee09c73be6414566e9`  
		Last Modified: Wed, 09 Apr 2025 00:56:47 GMT  
		Size: 51.2 MB (51191557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d56ac7b4debc4416f3b91cc7339b2bdb9236407799a9a27006ab2aee4cf22a8`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1acd1526edff837e8891600f66513cd21b9a141f65a8fe4c3a8bf56bfe42a464`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 329.1 KB (329093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63eaaf2a7e9e9c994c6d8055c6e7cdb2137522d943e88b73d1d17a05109bd2d`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90f146ef39e2e97f834ec6bbf7dc1d2464835e2f956850e1ae6104f11a84b59`  
		Last Modified: Wed, 09 Apr 2025 00:56:53 GMT  
		Size: 82.2 MB (82243898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0354bf1be150753bb6c24a3032c72b0fd25d4c9c81468650807adcb6fc9f2a1a`  
		Last Modified: Wed, 09 Apr 2025 00:56:39 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
