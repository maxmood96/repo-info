## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:26ba7b10923c93ef220efb274033fbe7371e93aec53807f7bba2ab73c2944cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull caddy@sha256:e08615b53b204b2c9b3855605053827eb1468c7a96565fa0d66eb784458e3663
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3622655059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78acfea1090af90a93fbe2e3cb9fa36522df8facd00e01d6b79509719d36b7af`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:00 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Jul 2025 18:09:01 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Jul 2025 18:09:01 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Jul 2025 18:09:02 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Jul 2025 18:09:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:09:21 GMT
ENV GOPATH=C:\go
# Wed, 09 Jul 2025 18:09:33 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Jul 2025 18:09:36 GMT
ENV GOLANG_VERSION=1.23.11
# Wed, 09 Jul 2025 18:10:55 GMT
RUN $url = 'https://dl.google.com/go/go1.23.11.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '1dbcf0b4183066550964b22890fe119b0b867b51f12c1eea4445c71494d98cbb'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:10:56 GMT
WORKDIR C:\go
# Wed, 09 Jul 2025 19:17:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 19:17:52 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 09 Jul 2025 19:17:53 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 09 Jul 2025 19:17:54 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 09 Jul 2025 19:18:02 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 09 Jul 2025 19:18:03 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fcbd7b0a1f3608f39f45d38d77bd1d8bc99b8b80577690ae49f2495fc6d51ce`  
		Last Modified: Wed, 09 Jul 2025 19:08:51 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbefaf0dfdde287d90804b77898b45c5ef94d64a330ae064873881c761bf218`  
		Last Modified: Wed, 09 Jul 2025 19:08:51 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb68e41d9f4d1f374375d6645219cda0ddaa36113d1f6de7f661dcc381e3d3e`  
		Last Modified: Wed, 09 Jul 2025 19:08:52 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fe9c0ea90e66e5734a67ac053e1d758d6f475bedd4a0a4cf411cf5eab16032`  
		Last Modified: Wed, 09 Jul 2025 19:08:53 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ae92a24674185f8654a71266e67646d71a52721cdfe87cec0377846f4b97542`  
		Last Modified: Wed, 09 Jul 2025 19:08:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a073cef6dcac6c9a7d197c817a0ba7463a191042ef8cc3fd26924f06cfe4b7`  
		Last Modified: Wed, 09 Jul 2025 19:08:57 GMT  
		Size: 51.2 MB (51224393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a142b5a59ef9074cd98a328d00ff1b222b524c32b4976ea998157bea7cff68d4`  
		Last Modified: Wed, 09 Jul 2025 19:08:58 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b98273005a94fbcd558eb28bec9d8c9832e22ea984227d40a64e73a40f0244c`  
		Last Modified: Wed, 09 Jul 2025 19:08:58 GMT  
		Size: 349.3 KB (349345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e0d84361bfc8c1417975e73de1980d410cca0eb1163ac65642bcd63e513714`  
		Last Modified: Wed, 09 Jul 2025 19:08:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5755fedbe82004c3d756748e97eba3bdedea06701d4b28861ed527deb5c0e4be`  
		Last Modified: Wed, 09 Jul 2025 19:09:04 GMT  
		Size: 77.6 MB (77569178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b71e50361dc3c925a544f3540fa202962be34f46130c8b953b34fceb7deffe4`  
		Last Modified: Wed, 09 Jul 2025 19:09:04 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b69835399ef07b45b77c84283b3d1e37e690ffbdc9c0a712b3aad6f04649f896`  
		Last Modified: Wed, 09 Jul 2025 19:18:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fffe22c1e6fca6e3c2e2059f0a9b0d21045cf9adfe64be5991c4e5ab61315a6`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26a888014944bafdd9dc0a933c960732c80aac346d49270ee44d43afd8ca3db`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b9a901b33f24eee2332dd23dc56b016fb0a9c5daf4c6e018455e7843e981f9`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4640e7aaffe985e1a621940c94da4557766c00f2d076ca830ef0feea9612b33b`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 2.3 MB (2321607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ac0c444eb4fc566a4085085d1fdba33d255c8e8be137993e0e2ddc62fc3c17`  
		Last Modified: Wed, 09 Jul 2025 19:18:25 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
