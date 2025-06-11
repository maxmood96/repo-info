## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:8357927473cc0bccd107dc1daa2f660204d87788e3437ae4c4a0adfff0d5335d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3807; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.3807; amd64

```console
$ docker pull caddy@sha256:87997a8e375374f12c2e01498281f2944e142ed937be4626eeb73594af8f2718
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2411473585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f28983d3f6a0f7a4f63475d3b3cc72592e1e1ee45c99c230b647c31a062820`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Jun 2025 01:01:39 GMT
RUN Install update 10.0.20348.3807
# Tue, 10 Jun 2025 21:27:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 21:27:25 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Jun 2025 21:27:26 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Jun 2025 21:27:27 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Jun 2025 21:27:28 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Jun 2025 21:27:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:27:45 GMT
ENV GOPATH=C:\go
# Tue, 10 Jun 2025 21:27:52 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Jun 2025 21:27:52 GMT
ENV GOLANG_VERSION=1.23.10
# Tue, 10 Jun 2025 21:29:01 GMT
RUN $url = 'https://dl.google.com/go/go1.23.10.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '3b533bbe63e73732bf19b8facc9160417e97d13eb174dfe58a213c6d0dee0010'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Jun 2025 21:29:02 GMT
WORKDIR C:\go
# Tue, 10 Jun 2025 22:19:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Jun 2025 22:19:50 GMT
ENV XCADDY_VERSION=v0.4.4
# Tue, 10 Jun 2025 22:19:51 GMT
ENV CADDY_VERSION=v2.10.0
# Tue, 10 Jun 2025 22:19:51 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Jun 2025 22:20:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 10 Jun 2025 22:20:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db5652627be066fd088860f3ebfcc61d4cb76922ffa16c5496b4158c7e4e7151`  
		Last Modified: Tue, 10 Jun 2025 19:16:01 GMT  
		Size: 818.1 MB (818059164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:327396a80b633d65f669cafb34887c185226a3a441281387159b461b3d925bd3`  
		Last Modified: Tue, 10 Jun 2025 21:30:46 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4d043dce7c812267f57e2b22f36e0307f07c792c5cc5106a8cf07835bc0bbe1`  
		Last Modified: Tue, 10 Jun 2025 21:30:46 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf153b82bd72b2bcb74e5e7bb4c09922d78fc827e02047e038acbb68cca8b7c`  
		Last Modified: Tue, 10 Jun 2025 21:30:46 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b5e276f4472d67ecfec0e6d9e47e747710996136cb2f84fcc1117373a657a1`  
		Last Modified: Tue, 10 Jun 2025 21:30:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4caccb8df9f1051ea8b645289a48b0159b2031399341cbbae1d6426dd87c9a9`  
		Last Modified: Tue, 10 Jun 2025 21:30:47 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f41e9929f04ce2552f318dfbed2569ce53c757a9cf822db2e54e9c9e3726f`  
		Last Modified: Tue, 10 Jun 2025 21:30:51 GMT  
		Size: 51.2 MB (51192353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc356e2a3499959bbaffd23acc4f96218ba6b829cfafe5fd6962fe723006e5a6`  
		Last Modified: Tue, 10 Jun 2025 21:30:48 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9626631ba06b2061705762f5378c00c2483fb69494af70775929f39f77545591`  
		Last Modified: Tue, 10 Jun 2025 21:30:48 GMT  
		Size: 336.4 KB (336447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56f33015c1687a9e724c980894b4a60e0c97b5ba6b35b898547f24849c9d676`  
		Last Modified: Tue, 10 Jun 2025 22:09:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a311c69e665838e79c5c88584084e42e3187d36ceaaee814b2bb91bb1f02e90`  
		Last Modified: Tue, 10 Jun 2025 22:09:16 GMT  
		Size: 77.4 MB (77371400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06c9df51424449bfcd6bc3518589643239acec485ff3244257785a7258c9a95c`  
		Last Modified: Tue, 10 Jun 2025 22:09:09 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d865afd6de661a23e287227cbdba069b8880acbc139de21689f1a931508a16`  
		Last Modified: Tue, 10 Jun 2025 22:20:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65938a8f12d6b2a1d377e9d3890aaf2d22faf85517a849d096cbf1ed2d43cb0`  
		Last Modified: Tue, 10 Jun 2025 22:20:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717b7eb86def2757f7d64723462fad570a7cbf361800c38ec9d43e05a3e49051`  
		Last Modified: Tue, 10 Jun 2025 22:20:27 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fb6b09f503745c803ebd5d6362a5edd443a46e76664a69f75aac86dd902cc8a`  
		Last Modified: Tue, 10 Jun 2025 22:20:27 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c7c09263bf2b6e74ba7bff386b540d92f31eb0bb2103a16d6f2bf2366e661e6`  
		Last Modified: Tue, 10 Jun 2025 22:20:27 GMT  
		Size: 2.3 MB (2304964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b9c4f14ce60070f0174f5b42958f62707b74f831d64fb1a7d6dcb92fbe8d63`  
		Last Modified: Tue, 10 Jun 2025 22:20:27 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
