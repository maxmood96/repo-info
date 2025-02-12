## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:b3aa8f4380ce49390ff7ba67bb03f1b7a0bea097c2be91dc7aa644ed706af4eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.2894; amd64

```console
$ docker pull golang@sha256:9b13fad98bdb330ed6a393381195d2508bdc7e3c581604603fe04b958399c20a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2608495221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01c980941e94851a3ad70baa4f09c6387a87c61d785413666501e9fbb88cbd6a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Wed, 12 Feb 2025 17:33:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Feb 2025 17:33:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Feb 2025 17:33:48 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Feb 2025 17:33:49 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Feb 2025 17:33:50 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Feb 2025 17:34:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 17:34:04 GMT
ENV GOPATH=C:\go
# Wed, 12 Feb 2025 17:34:10 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Feb 2025 17:34:11 GMT
ENV GOLANG_VERSION=1.24.0
# Wed, 12 Feb 2025 17:35:19 GMT
RUN $url = 'https://dl.google.com/go/go1.24.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '96b7280979205813759ee6947be7e3bb497da85c482711116c00522e3bb41ff1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 17:35:20 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfb1470dfdfd11de59044d9bee0634879aad1f4240bc8d813c1b97b55d568535`  
		Last Modified: Wed, 12 Feb 2025 17:35:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d476048629d426197c0828198c4657b7ce1e7a4b93e9900070fcb6c41e573dd3`  
		Last Modified: Wed, 12 Feb 2025 17:35:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bb4fbb5e3a24c2a4927e575016b9ce1ce228802412b5909f8f1a61f21c8bb72`  
		Last Modified: Wed, 12 Feb 2025 17:35:27 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c708aff48e1f17039c91c557d3b34ceff25aaf0595c1ffdf2057609a8c60a5be`  
		Last Modified: Wed, 12 Feb 2025 17:35:27 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf57c8e965011b15d0f5db6f4a19a70e4598650f8ac9c1d4a2634b8a97c9b213`  
		Last Modified: Wed, 12 Feb 2025 17:35:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db2ba832687114abea83a580499f0ab718f4ea8ae5f6638a2f0244e42a36bb`  
		Last Modified: Wed, 12 Feb 2025 17:35:30 GMT  
		Size: 25.5 MB (25493505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b9a5e26a68bf8ea014295242660cfc78ea870ee75f18e236d1439c13fbb3f1d`  
		Last Modified: Wed, 12 Feb 2025 17:35:25 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35f5b3f7b25294755cc185f0c2e7d14aca8ac96e7ab901363bb27531aa13fc10`  
		Last Modified: Wed, 12 Feb 2025 17:35:25 GMT  
		Size: 383.5 KB (383524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61616895ef1f532e408262cada7693cdbf2617d7610f0740c6ca79285c224659`  
		Last Modified: Wed, 12 Feb 2025 17:35:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c10b45f5021bb06f95785e8e27f2c4d9cb49bb65f5726d6a18e4e66623fe57`  
		Last Modified: Wed, 12 Feb 2025 17:35:38 GMT  
		Size: 82.3 MB (82330155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50f16e67c92cd6d6f75558a6ec6c942a08279ac52cb534ecdab603cab8739a7`  
		Last Modified: Wed, 12 Feb 2025 17:35:25 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull golang@sha256:97ecf78cad583001ecf4a43a4102fb0c3add088a857129b182436d71828c6a38
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2370220258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08d2c5b54b9d20306f85f086f72466f438cf9220a6a85b9901a7e5d617ab0ef3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 12 Feb 2025 17:29:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Feb 2025 17:29:35 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Feb 2025 17:29:36 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Feb 2025 17:29:37 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Feb 2025 17:29:37 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Feb 2025 17:31:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 17:31:08 GMT
ENV GOPATH=C:\go
# Wed, 12 Feb 2025 17:31:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Feb 2025 17:31:20 GMT
ENV GOLANG_VERSION=1.24.0
# Wed, 12 Feb 2025 17:34:41 GMT
RUN $url = 'https://dl.google.com/go/go1.24.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '96b7280979205813759ee6947be7e3bb497da85c482711116c00522e3bb41ff1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 17:34:42 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c4f37c567822c6e48890efb4320b6afe801bf406915a215e295ec7a008d8ab`  
		Last Modified: Wed, 12 Feb 2025 17:34:47 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5e859f50cd1d0d99701f378a7241585df432bc8322aed153dc1581408d3b79b`  
		Last Modified: Wed, 12 Feb 2025 17:34:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ca4d2166a84990f8b3bacdc3ec052aa9a1602522d595ad43c8a37b3650bb13`  
		Last Modified: Wed, 12 Feb 2025 17:34:45 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e2d335147197596124d44af6926a8b2de4f4bc4770e691da6961341292095ed`  
		Last Modified: Wed, 12 Feb 2025 17:34:45 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d62572c8b6b9e617ac354028d02614d8a399d743449fcb4887cdb4886d21a4`  
		Last Modified: Wed, 12 Feb 2025 17:34:45 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23a43ea27317a47d5dc20647a055809ced5b660c9b25f5a071e405af514228c`  
		Last Modified: Wed, 12 Feb 2025 17:34:48 GMT  
		Size: 25.4 MB (25447314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50396204a3d3a6abb10ebcc73c8dd25ba33cac8348077c3d9814976868c81f77`  
		Last Modified: Wed, 12 Feb 2025 17:34:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fba4ce9bbe6d4bb405fb35f11f63330e95e40bba8012a2cf4df6b32b32966d`  
		Last Modified: Wed, 12 Feb 2025 17:34:44 GMT  
		Size: 307.8 KB (307836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b5c0da68b3b84f20762fed8c819d938d3673b5a3a614452aaa4132b12cfb4b4`  
		Last Modified: Wed, 12 Feb 2025 17:34:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:289272b9422a429386861b2f2dc9a784f8fea7940451b571245e0a849496166a`  
		Last Modified: Wed, 12 Feb 2025 17:34:56 GMT  
		Size: 82.1 MB (82069311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d45b3e2084969963bf090549a26e240c93ec056ca28746a2c25690b10223421a`  
		Last Modified: Wed, 12 Feb 2025 17:34:44 GMT  
		Size: 1.5 KB (1462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull golang@sha256:885357132dbfa35b76c43bdd126472de9a0a9c6dc4daae6c906187f5c62428a2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230118172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab9c29d5068e72d5ae25403d383533f2b2eef41509cb92e820b08ed406b9b47`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Wed, 12 Feb 2025 17:29:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Feb 2025 17:29:50 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Feb 2025 17:29:51 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Feb 2025 17:29:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Feb 2025 17:29:52 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Feb 2025 17:31:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 17:31:17 GMT
ENV GOPATH=C:\go
# Wed, 12 Feb 2025 17:31:27 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Feb 2025 17:31:27 GMT
ENV GOLANG_VERSION=1.24.0
# Wed, 12 Feb 2025 17:33:21 GMT
RUN $url = 'https://dl.google.com/go/go1.24.0.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '96b7280979205813759ee6947be7e3bb497da85c482711116c00522e3bb41ff1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Feb 2025 17:33:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243e8d0bcc483f534dba402c136587c958958f1e7bdf7aabc14107dca74a9200`  
		Last Modified: Wed, 12 Feb 2025 17:33:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd55b18b5487a58ed777dc5d90bd49df3e77fdd6cb7d84ff9c3d87c2c19cabd6`  
		Last Modified: Wed, 12 Feb 2025 17:33:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a315a8f305936f5793eae96f00ef69d50508c5c64b8b25c305cb7717aa0fee4a`  
		Last Modified: Wed, 12 Feb 2025 17:33:28 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913374ca976e1f7da74d1da95823225a3c4e1fa61d7a7ea813fc0fa1ee4b9578`  
		Last Modified: Wed, 12 Feb 2025 17:33:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba6e181a0dae1ec08485e3751c6544d94a94274306e4fb0adb1cef885e17633`  
		Last Modified: Wed, 12 Feb 2025 17:33:28 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc9a97f905b176dedaae5b5c9de608ce532cd16bc5b16cadbbd9e1a9510b007`  
		Last Modified: Wed, 12 Feb 2025 17:33:31 GMT  
		Size: 25.4 MB (25446016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b0f67ef6e4b043f239773b6cd0fd52f33b415a2ee3a9b867f58a6636c04fe3`  
		Last Modified: Wed, 12 Feb 2025 17:33:26 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d2b7d90444547ed56d4acc4052508a42a400020f484fb90fdc17779c185058`  
		Last Modified: Wed, 12 Feb 2025 17:33:26 GMT  
		Size: 351.0 KB (350994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0da78860fa65d723151d65bee4f2a4b25d034ae70150e4ed44367bb7d06afa5`  
		Last Modified: Wed, 12 Feb 2025 17:33:26 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060a97562ff43c0685ea1f986a08df433b1e15ae867bf07f1765a103e31324c`  
		Last Modified: Wed, 12 Feb 2025 17:33:38 GMT  
		Size: 82.1 MB (82098465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5b3f1413d093d5608820c28ac77e06389146c89ad85b3ba22e4372d1d4d06`  
		Last Modified: Wed, 12 Feb 2025 17:33:26 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
