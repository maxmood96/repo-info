## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:fdc87426491af0ab8da96f4e485fd6b8a38b1ff085e43b1bc1b5f080637d450f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull caddy@sha256:a5ba2d4e805309376c3cad234053797a2e07f61ca3cfa4ccb77779ce62cba351
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2257240189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0518d644b30a6e22a09c21bdbf4d953202c27bd80bf2813eae7129db52da98a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 01:22:55 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 May 2023 01:22:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 May 2023 01:22:56 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 May 2023 01:22:57 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 May 2023 01:24:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 01:24:15 GMT
ENV GOPATH=C:\go
# Wed, 10 May 2023 01:25:19 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 May 2023 01:36:16 GMT
ENV GOLANG_VERSION=1.19.9
# Wed, 10 May 2023 01:39:26 GMT
RUN $url = 'https://dl.google.com/go/go1.19.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3b0ca22aedf5fd85e84c944dd96ab3044213bf224cc3e9850ad86f1f71e1be93'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 10 May 2023 01:39:28 GMT
WORKDIR C:\go
# Wed, 10 May 2023 03:08:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 May 2023 23:20:18 GMT
ENV XCADDY_VERSION=v0.3.4
# Wed, 17 May 2023 23:20:18 GMT
ENV CADDY_VERSION=v2.6.4
# Wed, 17 May 2023 23:20:19 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 17 May 2023 23:21:25 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.4/xcaddy_0.3.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('542b4c083852d41081186c79757b66ff3c26248f72ed461dbc038b51687d0a8a8ce8eee69e3b5a1d43360c48b3405b611b940fa378debe98aaa0b3c5aebfa218')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 17 May 2023 23:21:26 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69c8e1c8adec95ce194194fafcfc6a1e07f15344588a0b08f7f625c5a547434`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47736757cd8e844fa5669cb79caf4053a95eb6b57e09dd4ab01823f071f92f24`  
		Last Modified: Wed, 10 May 2023 01:46:45 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd4aa96423c060d9cbb5c55c535627e8c1e46ba89f752a3d601450afe81b5b8`  
		Last Modified: Wed, 10 May 2023 01:46:44 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077f8de560673af047f7136635e2e62927f8f69d11a928140de06383e86fb295`  
		Last Modified: Wed, 10 May 2023 01:46:44 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed8138b5cc05a953f350e06a0713c2c031257b514bb362629f520d00db71fd7`  
		Last Modified: Wed, 10 May 2023 01:46:49 GMT  
		Size: 25.5 MB (25530178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814a31d39859b5f50d901390aa5410b00f1637dce1a5839d12e69722fab50294`  
		Last Modified: Wed, 10 May 2023 01:46:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e05276aaa698fd9d43e2a1961637e16578fa84a5128237d7c2bdfe57c54fa89`  
		Last Modified: Wed, 10 May 2023 01:46:42 GMT  
		Size: 262.2 KB (262162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4aecdb7abe61438b7c484538d9abcbf9f221e8250bbc14ff0340952477872ca8`  
		Last Modified: Wed, 10 May 2023 01:49:56 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8a8051e6917bcca154f994e561aaca88eec8542d26c4215449c493cc20677a9`  
		Last Modified: Wed, 10 May 2023 01:50:27 GMT  
		Size: 157.7 MB (157699831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:819570cca8314d2c43127f47e580ccca379d28ee2b2a710a0cf56ac3dc22e5a9`  
		Last Modified: Wed, 10 May 2023 01:49:56 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fb1cac98386c21a9acf42c96ef5775a0f72c5d8aa5b0d4702c8878a59324521`  
		Last Modified: Wed, 10 May 2023 03:12:06 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f97e1faf8713a6549f36062626000386e3c37d2fd82f3d0dcbcc487d5ca1175`  
		Last Modified: Wed, 17 May 2023 23:29:05 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aafc3d9e3a6f382dc5558e92883a875c5ce4355a34224b86366356fef530e586`  
		Last Modified: Wed, 17 May 2023 23:29:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aadb8b0ea8e2cd1384ed29133fbe94138bccc7f0d1c6403d556f042a085c4f44`  
		Last Modified: Wed, 17 May 2023 23:29:05 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce0dd52f687ee9c599c4f3d794a62543140d278e91f5ef9e78e57608b0f584d`  
		Last Modified: Wed, 17 May 2023 23:29:06 GMT  
		Size: 1.7 MB (1695142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c44cb5a253a6e1590f4c503c254bf7801f02a6b834ed3b6207145e47e79fe`  
		Last Modified: Wed, 17 May 2023 23:29:05 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
