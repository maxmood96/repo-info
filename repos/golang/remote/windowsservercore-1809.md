## `golang:windowsservercore-1809`

```console
$ docker pull golang@sha256:e54bf64477c59d6daa916246913ec9e726d66924e9236fee93d19f9f9a3b18d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `golang:windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull golang@sha256:1fe4ed239c2ce94d4fd1eaaa7cddc8953c8ade5bf1bba79648d6ba18b532d520
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336123924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90ff9174fec453960d29f8723fa322bfeacdd3cf4b19ffc579e958ffdcc952da`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Tue, 06 Aug 2024 22:56:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Aug 2024 22:56:01 GMT
ENV GIT_VERSION=2.23.0
# Tue, 06 Aug 2024 22:56:02 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 06 Aug 2024 22:56:02 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 06 Aug 2024 22:56:03 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 06 Aug 2024 22:56:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:56:46 GMT
ENV GOPATH=C:\go
# Tue, 06 Aug 2024 22:57:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Aug 2024 22:57:06 GMT
ENV GOLANG_VERSION=1.22.6
# Tue, 06 Aug 2024 22:58:59 GMT
RUN $url = 'https://dl.google.com/go/go1.22.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '6023083a6e4d3199b44c37e9ba7b25d9674da20fd846a35ee5f9589d81c21a6a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Aug 2024 22:59:00 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09177a2d8100731d191cc1f7268068fe9838aeb2c4082ff06b328709fd7ebf65`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f430bf25eee4267b1d84ea64815fb55a7d7cf85c8fa78ddd8485a195fb00cc`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b0976710052c049e2f19bcbec09e706ab0805f3007984ffa21d58be92599740`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8186263fc237d42bb6e9f2bdf27e324ce393fc351732137e2a6f0bf6af1a256`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2b3aada17941bcb5f4d65c437730c3eb6330eafac2adfc5be0cfcb842b12d3`  
		Last Modified: Tue, 06 Aug 2024 22:59:07 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb29c5f1c6b570e746a18be662c5fed69c91c6f9cd49817ddd368ec3d00945b`  
		Last Modified: Tue, 06 Aug 2024 22:59:09 GMT  
		Size: 25.6 MB (25580557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0a9fe7afd5b5f0e04a762ae3584205d38d916b2a97b79b270145c6c999e92ac`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f752cb947fcbfa05ceaf706a0e7d09de2c5f6fb064c02e3ba8c08605e18e9a`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 342.4 KB (342379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b5038a529a813e24653c828b04cedfb004652d03694ddf4285d057586181e3f`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a4a42e8184621546ae9b99673a7b5f26572753cb40d4f37e5786941b715f63`  
		Last Modified: Tue, 06 Aug 2024 22:59:15 GMT  
		Size: 71.8 MB (71761086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d71452634c4b504306599ea0b3fa0e112063e9436c281ba1b78b961368864b1`  
		Last Modified: Tue, 06 Aug 2024 22:59:05 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
