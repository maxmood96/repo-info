## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:db4489d0bf7891aa5c5159006d3a15caa5b0208dc892eb4227185bb99dff34e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull caddy@sha256:ce832d201acce034f73a7ad2cbad0880d458590d4b5ca98ed6d40eac1e6c8fc7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2007430843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff50f71fafc8b4c437882f7b8677c389e29861b9f22c42f77eebabccb492f89`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Thu, 07 Nov 2024 02:58:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 Nov 2024 02:58:54 GMT
ENV GIT_VERSION=2.23.0
# Thu, 07 Nov 2024 02:58:55 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 07 Nov 2024 02:58:55 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 07 Nov 2024 02:58:56 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 07 Nov 2024 03:00:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 07 Nov 2024 03:00:19 GMT
ENV GOPATH=C:\go
# Thu, 07 Nov 2024 03:00:27 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 07 Nov 2024 03:00:28 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 07 Nov 2024 03:02:21 GMT
RUN $url = 'https://dl.google.com/go/go1.23.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '81968b563642096b8a7521171e2be6e77ff6f44032f7493b7bdec9d33f44f31d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 07 Nov 2024 03:02:22 GMT
WORKDIR C:\go
# Thu, 07 Nov 2024 03:48:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 07 Nov 2024 03:48:37 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 07 Nov 2024 03:48:38 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 07 Nov 2024 03:48:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 07 Nov 2024 03:49:05 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 07 Nov 2024 03:49:06 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79479da7f7f1735d60cfc8070cf1b84dafacb2b3b3a98d9b1e934fbf97c9d9d4`  
		Last Modified: Thu, 07 Nov 2024 03:02:29 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e2590be1c3a65810977148270d41363883d20129d18f0ac0a1bbc321a37ed2`  
		Last Modified: Thu, 07 Nov 2024 03:02:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f5fe598872a38f4e7557ee214d9d84db27fa9ab46458a9389d4bb9811959c6e`  
		Last Modified: Thu, 07 Nov 2024 03:02:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c9fc16abe34ef1c4af9f860e5a4d3614fe43a9c6d38af8ac2935ae63558565`  
		Last Modified: Thu, 07 Nov 2024 03:02:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551592e795ab2ca258e604f27ab5800321f70c90e25997624c283c7f05f47d21`  
		Last Modified: Thu, 07 Nov 2024 03:02:28 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae937cb9fb3f265d1d53fb7e61448a93a401d3edbe26a43af6b01974fb66f57a`  
		Last Modified: Thu, 07 Nov 2024 03:02:30 GMT  
		Size: 25.6 MB (25595147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a8b73da8fdfe2bf9f94fe8c8149a86339e362a4789438b69aa3035dff6a12be`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c88ad30f34542f7c26f450f093601c118e4d1ecc49c780dc507a5f76a77014e8`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 347.9 KB (347897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23f40948b9cc828d3e0779fe95176880d3f4240573c131940b69a72d4721d09`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c30d5b336ac154c42be9b040555efaaca0efbd9b6a4a6863f61a89d4632bc587`  
		Last Modified: Thu, 07 Nov 2024 03:02:37 GMT  
		Size: 77.3 MB (77339950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4510b45d687fbea6bf5de1579cd007c0e6579622858859701f0d5b45d56f6cf0`  
		Last Modified: Thu, 07 Nov 2024 03:02:26 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230da8fd44360a588d2b4dd0418d2ea5811e71ed9dffa90eae21e07b642f1bbf`  
		Last Modified: Thu, 07 Nov 2024 03:49:12 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:574ca39f523c5b6a42a862a16ffad399162d9a12ea1e8a0cc08e5393ff3350f4`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:103d0f7006bd524f556e7b29ead5081649b16a747d4eacfb5b5a62790e5686da`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501d2af8af1faa11338e7d54975b3cd73a0b0e62b592fe2cb1d161ffe2fe7a3d`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7789106df25539d98743b3b4397858ec3ed250f36e0759b7b52281910a2612aa`  
		Last Modified: Thu, 07 Nov 2024 03:49:11 GMT  
		Size: 2.3 MB (2305578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e51d55d7bb91ee81ee86523c249db0fc3f769d25f64eff1d8f10e006e34e346a`  
		Last Modified: Thu, 07 Nov 2024 03:49:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
