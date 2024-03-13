## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:88480ae6cc843e1f4d7891d869f95182848a5414c6545cc2662d466a7c8dfdd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5576; amd64

```console
$ docker pull caddy@sha256:53d965e8f604060a1c65cdf2a722300b8ff2f7a36494b6c0ba0c315fc7ffd2c2
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2221957582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0daee73c43fffad7bf7cfb8399d58db63aaa5f6727affb62b8d370b9760df81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:38:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 01:49:48 GMT
ENV GIT_VERSION=2.23.0
# Wed, 13 Mar 2024 01:49:49 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 13 Mar 2024 01:49:50 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 13 Mar 2024 01:49:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 13 Mar 2024 01:51:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 01:51:29 GMT
ENV GOPATH=C:\go
# Wed, 13 Mar 2024 01:52:49 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 02:04:28 GMT
ENV GOLANG_VERSION=1.21.8
# Wed, 13 Mar 2024 02:07:38 GMT
RUN $url = 'https://dl.google.com/go/go1.21.8.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'ab396b44a5c6fadd6494c54b527a13cafefcc669ade01e817bad5740ef175a3b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 02:07:39 GMT
WORKDIR C:\go
# Wed, 13 Mar 2024 02:38:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 02:38:30 GMT
ENV XCADDY_VERSION=v0.3.5
# Wed, 13 Mar 2024 02:38:31 GMT
ENV CADDY_VERSION=v2.7.6
# Wed, 13 Mar 2024 02:38:32 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 13 Mar 2024 02:39:53 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.5/xcaddy_0.3.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('e7a7b91439669b96bd3dbe347d9fcc84767c02c68ed451b7b80c8d3063c9e4ae2531d4bba0ee51d7d78be29371d36bac56412e39144b92e781e253f265a3883c')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 13 Mar 2024 02:39:54 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958f7c360fd7d6281bb6b494ebac22f9165235afc440fb43948425a566792f6`  
		Last Modified: Wed, 13 Mar 2024 01:29:39 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cc39f00be83bc8d2b0e0f2123fce0278f495e47f8a969bf03ec57df5f98cbda`  
		Last Modified: Wed, 13 Mar 2024 02:14:08 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f8b9e441646ef17118a0d394fa50244ef70c9e053c5b7d33e648796c8df90e`  
		Last Modified: Wed, 13 Mar 2024 02:14:07 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8759cd20778bf436a14e59cb31806b28212fcd510d8de32d44e49a9f39656f3d`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09d99a22ebabf5f80d07ad166a24eace1c2fa31cef2566a179bfec0d6407513e`  
		Last Modified: Wed, 13 Mar 2024 02:14:06 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cfdb963b4125b258828e1fbac783c993a6845ad94973fad173f5dd25be3c34b`  
		Last Modified: Wed, 13 Mar 2024 02:14:12 GMT  
		Size: 25.5 MB (25540238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae89960ac90d33a751006d43faf1cbd1309b448658a447bb19dddabdbee17a9`  
		Last Modified: Wed, 13 Mar 2024 02:14:04 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fff0bdcb61a7230b8b00d6e08d739c64fc0342dc675ed99fe6d35885cf1aa369`  
		Last Modified: Wed, 13 Mar 2024 02:14:05 GMT  
		Size: 272.6 KB (272572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c052d4b938689fbc1637386d1e61efa391787bd8128ee6d093464bad09b0231`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e82772a8bffddc9f4a46c65cfa48f47938d84feb3730231762158c98014e47a`  
		Last Modified: Wed, 13 Mar 2024 02:16:31 GMT  
		Size: 69.4 MB (69350702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbffcc4012ecf27a404cc40eb63c43a880ad5104a82ee619fd0669acb2b5a710`  
		Last Modified: Wed, 13 Mar 2024 02:16:12 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fcd0eeed9adb7d9bf391df7f194150cb8ee56a63bc679cf147a14185381c3b`  
		Last Modified: Wed, 13 Mar 2024 02:42:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d74d351932d9ba6c92c9398e69d6736df75938a6ba3b7f1055206a1ed80b48`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51f1e77d8641618afadb6f8c1ad073c4f72bb79099a00b0cabcbc8f5579248`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43620705f408ca0a7894137080f7947cc45d10badb0c7668ae1d46464494001b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdaa0771d9c8b704195f821c3a9c23a5d9ff5e7e9b29335b835ce237f9d4dd50`  
		Last Modified: Wed, 13 Mar 2024 02:42:03 GMT  
		Size: 1.7 MB (1676257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010496734b493d0bc1b1a73566306e98777144ff64c5c886cf84de3af4fd971b`  
		Last Modified: Wed, 13 Mar 2024 02:42:02 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
