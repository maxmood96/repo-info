## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:2cf1c1823c1b46d38e0f87e67f1507c0065dc1a5165579648df87cde9558666a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

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
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 20:54:32 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:243e8d0bcc483f534dba402c136587c958958f1e7bdf7aabc14107dca74a9200`  
		Last Modified: Wed, 12 Feb 2025 17:33:52 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd55b18b5487a58ed777dc5d90bd49df3e77fdd6cb7d84ff9c3d87c2c19cabd6`  
		Last Modified: Wed, 12 Feb 2025 20:18:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a315a8f305936f5793eae96f00ef69d50508c5c64b8b25c305cb7717aa0fee4a`  
		Last Modified: Wed, 12 Feb 2025 17:33:53 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913374ca976e1f7da74d1da95823225a3c4e1fa61d7a7ea813fc0fa1ee4b9578`  
		Last Modified: Wed, 12 Feb 2025 17:33:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bba6e181a0dae1ec08485e3751c6544d94a94274306e4fb0adb1cef885e17633`  
		Last Modified: Wed, 12 Feb 2025 17:33:54 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bc9a97f905b176dedaae5b5c9de608ce532cd16bc5b16cadbbd9e1a9510b007`  
		Last Modified: Wed, 12 Feb 2025 20:18:02 GMT  
		Size: 25.4 MB (25446016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b0f67ef6e4b043f239773b6cd0fd52f33b415a2ee3a9b867f58a6636c04fe3`  
		Last Modified: Wed, 12 Feb 2025 17:33:54 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d2b7d90444547ed56d4acc4052508a42a400020f484fb90fdc17779c185058`  
		Last Modified: Wed, 12 Feb 2025 19:34:24 GMT  
		Size: 351.0 KB (350994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0da78860fa65d723151d65bee4f2a4b25d034ae70150e4ed44367bb7d06afa5`  
		Last Modified: Wed, 12 Feb 2025 19:34:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9060a97562ff43c0685ea1f986a08df433b1e15ae867bf07f1765a103e31324c`  
		Last Modified: Wed, 12 Feb 2025 19:34:27 GMT  
		Size: 82.1 MB (82098465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ef5b3f1413d093d5608820c28ac77e06389146c89ad85b3ba22e4372d1d4d06`  
		Last Modified: Wed, 12 Feb 2025 17:33:55 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
