## `caddy:2-builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:f88eb5bcf0578f255fce285d54b4941c4a3cd68b496dcbe239a1b02c6a09be4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `caddy:2-builder-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull caddy@sha256:87643957c20a3a87ccd5a56c00ef0f360eff0b9498e2fc15e0a93d8d5f513f86
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320513498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed61ae64a42b233780136a6dd4245dc4313a9d5a41e0b05ac7caf83ef6f39f02`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Wed, 12 Jun 2024 18:13:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:13:33 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Jun 2024 18:13:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Jun 2024 18:13:35 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Jun 2024 18:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:14:24 GMT
ENV GOPATH=C:\go
# Wed, 12 Jun 2024 18:14:41 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:14:42 GMT
ENV GOLANG_VERSION=1.22.4
# Wed, 12 Jun 2024 18:16:03 GMT
RUN $url = 'https://dl.google.com/go/go1.22.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '26321c4d945a0035d8a5bc4a1965b0df401ff8ceac66ce2daadabf9030419a98'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:16:05 GMT
WORKDIR C:\go
# Wed, 12 Jun 2024 19:06:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 19:07:00 GMT
ENV XCADDY_VERSION=v0.4.2
# Wed, 12 Jun 2024 19:07:01 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 12 Jun 2024 19:07:02 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 12 Jun 2024 19:07:41 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 12 Jun 2024 19:07:42 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae3c3ab4cd77fae9059354ee5b73b856f9ac9c22731d9dcf4e365268e08cd843`  
		Last Modified: Wed, 12 Jun 2024 18:16:10 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d86c37a0d0339c6b8b1c237b2c8250a774461350198b803d76982b65e45d102b`  
		Last Modified: Wed, 12 Jun 2024 18:16:09 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a3b2fa9fd4cc3f0df2f037d6653ea1cdb5b7f419bd99e0576a57dcdf4b1ace7`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:856fdc06eea972eccedb4e2c6d528d9d6b992c971c4a29f289a88eac23a5d5a9`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2096b09fa3f4c724fcb42fe19a8a5b0dc61277e2e802b4674b64a58de93238`  
		Last Modified: Wed, 12 Jun 2024 18:16:08 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69169629162eb6e94b664ddd335d3d02ae4c7a356ec11557b77d6780bfb3bb04`  
		Last Modified: Wed, 12 Jun 2024 18:16:11 GMT  
		Size: 25.6 MB (25576657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78abdc0679bbe9abc0864ab9497cfb6767ad50cc06c121d874dd8a022821b892`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6bc3316ec48d85e70aa2d8c21fa5ad4eb37113d651977b29d3b5495e034859`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 336.9 KB (336919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5222f75d358e9b8e60fd785f40a7b8245f0cf6d634f64488172b55910395e1a2`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e23068dc7ebfc095432cdb1e6af9726e3b10d959fb3635a24504c0e99a1a297`  
		Last Modified: Wed, 12 Jun 2024 18:16:18 GMT  
		Size: 72.0 MB (71984977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe4726c882b12bd6e005278f53050cd3de58b99ce5170e1d152a081dd3e8d6b`  
		Last Modified: Wed, 12 Jun 2024 18:16:07 GMT  
		Size: 1.5 KB (1501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a82c23888a8a0ba647456b84c7ea43d9006ae2be3d5696242de32eb8405ac31`  
		Last Modified: Wed, 12 Jun 2024 19:07:48 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46372b8f4856e120d8fb747141593fa94d9a23f57791830afde85df63afc9899`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af6f48c9a230e1a939a96d21e33a526d29db1f16f675d8a5a5d2980d525c55e7`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a77f93979cdc9572da29ca6339d8c5d86cab41b05c15587495a9eb7462e987f`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a650a02a30a4f0a3a25ceba7eb1f2a71ec607cc0ef9eadf34699b617fd5b0171`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.9 MB (1916297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e5d61909213f979bdf56f6332986a4a3e32291b9e092ecd1ee655b82e52b90`  
		Last Modified: Wed, 12 Jun 2024 19:07:46 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
