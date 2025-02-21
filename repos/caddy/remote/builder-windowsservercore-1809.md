## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:17d3631b303c93cd94c310bd737b00cbff2e05a7db81a70c63da9852b12493d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull caddy@sha256:3e8705d53c87a9edc2e45a93a782f5b1190c1ceee53f51c118ff1325b47ae4e8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2242329732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d59d81a36d95186bd70accdee1671a70fdf7ff30f4fc49cbaa8b7baf4aa8cef`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:30:46 GMT
ENV GIT_VERSION=2.23.0
# Thu, 13 Feb 2025 00:30:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 13 Feb 2025 00:30:47 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 13 Feb 2025 00:30:48 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 13 Feb 2025 00:31:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:31:13 GMT
ENV GOPATH=C:\go
# Thu, 13 Feb 2025 00:31:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:31:20 GMT
ENV GOLANG_VERSION=1.23.6
# Thu, 13 Feb 2025 00:32:32 GMT
RUN $url = 'https://dl.google.com/go/go1.23.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '53fec1586850b2cf5ad6438341ff7adc5f6700dd3ec1cfa3f5e8b141df190243'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:32:34 GMT
WORKDIR C:\go
# Thu, 13 Feb 2025 01:18:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 01:18:10 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 13 Feb 2025 01:18:11 GMT
ENV CADDY_VERSION=v2.9.1
# Thu, 13 Feb 2025 01:18:12 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 13 Feb 2025 01:19:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 13 Feb 2025 01:19:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 18:49:50 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d136fde42e6e2bc91f5956d1e8ac33fc4084914e9982e16f2ddaa1a241fdfafe`  
		Last Modified: Thu, 13 Feb 2025 00:32:42 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af2a1616935cf9566cec5a3c62a7dc245e7c5af888145e48ea7ce3fbca2aa52`  
		Last Modified: Thu, 13 Feb 2025 00:32:42 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d857ea95e03ce72ba0cb753a4ac08d710617d9747b4146f005f4a4b2ecf7da`  
		Last Modified: Thu, 13 Feb 2025 00:32:40 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9efeacb0745fe69e3fc393b6abd1b8685a3e6d4b442f3418888b88c570adef40`  
		Last Modified: Thu, 13 Feb 2025 00:32:40 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1944d354e141d0e6fab9973beb428631e15a12c7cf102d9164712bfc5ec2774e`  
		Last Modified: Thu, 13 Feb 2025 00:32:40 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10a76bdabf7b0e00c0c95acbd81a11afb3c9e98e719a1e05fd131f224f1b6f5e`  
		Last Modified: Thu, 13 Feb 2025 00:32:43 GMT  
		Size: 25.4 MB (25429808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f858d3ced918bc0d0c407242159a57e218ee53b65f3f1969c90bb33dbb289d37`  
		Last Modified: Thu, 13 Feb 2025 00:32:38 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b24259778625afcce89689eef634fd77a27e7d5bf6abdd9d17baa857abd515`  
		Last Modified: Thu, 13 Feb 2025 00:32:38 GMT  
		Size: 333.0 KB (332954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376aee295847eb57d8099b4a71488b21729dc5500e739f4d7a50ed8b99b48736`  
		Last Modified: Thu, 13 Feb 2025 00:32:38 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472f935a883cd53a550d97a611da1241b94339b34c6c9df9658cb698b8209d5a`  
		Last Modified: Thu, 13 Feb 2025 00:32:50 GMT  
		Size: 77.3 MB (77348156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ada68cd6c4090eea38d86ac6a8ca00d468b62ca4954c03e16a04d3985a57a0d`  
		Last Modified: Thu, 13 Feb 2025 00:32:38 GMT  
		Size: 1.5 KB (1453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ece25bc91fc0a7327a8f64cafb4cd0237ade2cfff8b55578f024ab9da6f91f`  
		Last Modified: Thu, 13 Feb 2025 01:19:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87b5ce8692b8608aaac9d4b9bb62fa76c3c32ed01043d0652c9825d915045748`  
		Last Modified: Thu, 13 Feb 2025 01:19:05 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c85a00f6d0a73986ac0efc0998a656c23ad2bb894ef1adaf894836a5af69a707`  
		Last Modified: Thu, 13 Feb 2025 01:19:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:793ef1769ceadaed34f7a4fa52de949adce1b874dd8f84acf364d74ffa85d844`  
		Last Modified: Thu, 13 Feb 2025 01:19:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80b4f2d615714064f24ef30715eba1159833340bf464fbb1df4726bebec90d3c`  
		Last Modified: Thu, 13 Feb 2025 01:19:06 GMT  
		Size: 2.3 MB (2292786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bdd7fac213579eb6578cb8f231fbd80bf84b007ddea648ad35c5be58e7bb65e`  
		Last Modified: Thu, 13 Feb 2025 01:19:05 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
