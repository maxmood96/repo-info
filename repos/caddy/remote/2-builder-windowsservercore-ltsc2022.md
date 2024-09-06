## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:0cf25c234c09a997c070ea4e8427487d9fc73f9f2e3381becce470c00a04220f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull caddy@sha256:dc96edbd3174325b1cd6a2745e108067b244c1ee1e170ce873c434133954f23e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2241170820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7630bd99f6a7f8681c9f339d88185f06bc10ce2f26c882e53e20e9eeb1f203`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Thu, 05 Sep 2024 22:02:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Sep 2024 22:02:59 GMT
ENV GIT_VERSION=2.23.0
# Thu, 05 Sep 2024 22:03:00 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 05 Sep 2024 22:03:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 05 Sep 2024 22:03:01 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 05 Sep 2024 22:04:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:04:30 GMT
ENV GOPATH=C:\go
# Thu, 05 Sep 2024 22:04:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Sep 2024 22:04:36 GMT
ENV GOLANG_VERSION=1.22.7
# Thu, 05 Sep 2024 22:07:23 GMT
RUN $url = 'https://dl.google.com/go/go1.22.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'efbc30520601f4d91d9f3f46af03aafb2e1428388c5ff6a40eb88489f7212e85'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 05 Sep 2024 22:07:24 GMT
WORKDIR C:\go
# Thu, 05 Sep 2024 23:06:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Sep 2024 23:06:56 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 05 Sep 2024 23:06:56 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 05 Sep 2024 23:06:57 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 05 Sep 2024 23:07:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 05 Sep 2024 23:07:53 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2310108d765b1d8aa5b099e9e0502536ec684eda2008d54f8129a83d6dbe4b29`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa02a13b26572c52f802607cca775b0f8ee0068f252e2b4cb1816d88cc907f39`  
		Last Modified: Thu, 05 Sep 2024 22:07:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acead8088ce2ff4f0fae1020e0ddd3806fc735303e8df2ee5d1c9f6a7be16670`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b52b5aadc2895d747455a66450717a1875ebb07a1fd4fb92676826910aac30`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d77ecf1e40f03b56cc5b25aa1d5b1e0b9cd5ef68a557c16ac3ef0b27d790d602`  
		Last Modified: Thu, 05 Sep 2024 22:07:28 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb015ec251e478a27ad07d43923577b1feff098b157e74453ade13361f7783fe`  
		Last Modified: Thu, 05 Sep 2024 22:07:30 GMT  
		Size: 25.4 MB (25443893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2713f48db96da3c8c9919e7c181eacb3377b798862926a7b4fdecd74e8eab8a1`  
		Last Modified: Thu, 05 Sep 2024 22:07:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f9cd281b25493d5e3d108e9567f35abcc52b405c76a2dc19001436d743d8d6`  
		Last Modified: Thu, 05 Sep 2024 22:07:27 GMT  
		Size: 302.9 KB (302923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a01de8b033405f882e2d975e5bbf7c794ab351049d9abe1cfc64842e3edb6e00`  
		Last Modified: Thu, 05 Sep 2024 22:07:27 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad71b51eed4d878a10ad7923d8b81b47f9554f5cc73af9c3c14c8d9e94f62dd`  
		Last Modified: Thu, 05 Sep 2024 22:07:37 GMT  
		Size: 71.7 MB (71721934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f23dfb320d7f0765e2db317d4d2bb185836ff847fdf92de15d1a598845e8ca5`  
		Last Modified: Thu, 05 Sep 2024 22:07:27 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8411e870884633b188d0eff7a195c15090d2a2c2f1379a2482e24f4e6488ea2b`  
		Last Modified: Thu, 05 Sep 2024 23:07:57 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ceaf3d6e1fdacec9184ea2445a717b30b3396aade8cf5f74494f1a72e14882`  
		Last Modified: Thu, 05 Sep 2024 23:07:56 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9244b4278ef644409184a9383626117e14c80fb4bf50cc21820dd8ceeec67895`  
		Last Modified: Thu, 05 Sep 2024 23:07:56 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35e496f8cac53176903c182cf9626b604df0580f660d1392b63e0e3aa4ab5363`  
		Last Modified: Thu, 05 Sep 2024 23:07:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54b00500ea6d685f8a35b94b5abf9a046be110ce1fe4c024439c38ec872ac5aa`  
		Last Modified: Thu, 05 Sep 2024 23:07:56 GMT  
		Size: 1.9 MB (1920268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61b9dca8a85e3816a1a4da200ae9c6a9e4cc954244d69d1a4e702e0398b6e29`  
		Last Modified: Thu, 05 Sep 2024 23:07:56 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
