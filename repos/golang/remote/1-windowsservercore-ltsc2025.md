## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:80ec515eaec24c2cc794163f8df3b9550eac1a5e48b9ce40c053cae3694f43c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull golang@sha256:dee839a1a1e6c9a47680d0e46a13ad18b16e15018dec24566bd0041f99952b1d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3625281663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e04c78912e4ba1f54139a9f5951e06588f3ab796f37ab31fbd700d871e144f7c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:41 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:08:43 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Jul 2025 18:08:44 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Jul 2025 18:08:45 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Jul 2025 18:08:47 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Jul 2025 18:09:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:09:04 GMT
ENV GOPATH=C:\go
# Wed, 09 Jul 2025 18:09:12 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Jul 2025 18:09:14 GMT
ENV GOLANG_VERSION=1.24.5
# Wed, 09 Jul 2025 18:10:37 GMT
RUN $url = 'https://dl.google.com/go/go1.24.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '658f432689106d4e0a401a2ebb522b1213f497bc8357142fe8def18d79f02957'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:10:39 GMT
WORKDIR C:\go
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
	-	`sha256:e75f8d61ebd59362890e94a9b2e3fa1b81ef8298b39bf71bcf6fc437a5037b2d`  
		Last Modified: Wed, 09 Jul 2025 19:09:05 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc15897e255a9af4a4e8a0bbfc6ea45c33fab9ee2ac9e4ff83c6b511ad670bc`  
		Last Modified: Wed, 09 Jul 2025 19:09:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4386c72eedaf95845221cf6bb36b10667cf292a3840cdcd77c29f63337917edb`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ccd1618edfd26b77def2ff540c8afcf66aa08047fd143559bf3ecf79bbe731`  
		Last Modified: Wed, 09 Jul 2025 19:09:09 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32215a8739418644745070f8c7b4041cc9b4ab4df1a9cb9c7bd078f2c2e434c`  
		Last Modified: Wed, 09 Jul 2025 19:09:11 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3524787662d917bad4397fd9f78167e0ae69619673bc0b9d67d49818d395fcc0`  
		Last Modified: Wed, 09 Jul 2025 19:09:20 GMT  
		Size: 51.2 MB (51233502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b0c8cba70d18324d47901652b3fcc81ab457a991a9305a580ca68315198d7c`  
		Last Modified: Wed, 09 Jul 2025 19:09:21 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63468999507b6adaecfe067308f2e9ff64f39b3790e467b30731b70df8547b52`  
		Last Modified: Wed, 09 Jul 2025 19:09:22 GMT  
		Size: 357.2 KB (357208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fa6a3f4563abf9456d95489dcade7d8d7328fb8772e338888ac4fb534d5861d`  
		Last Modified: Wed, 09 Jul 2025 19:09:24 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ad21c977fa5eb622ff290dbadb4f74946023fefad715ed6ca71048b8f0fd6`  
		Last Modified: Wed, 09 Jul 2025 19:09:52 GMT  
		Size: 82.5 MB (82507005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016ff88bfd85d0eeff1db72e0fb21cbd1c7832042ae4d6631b606717c81ad213`  
		Last Modified: Wed, 09 Jul 2025 19:09:31 GMT  
		Size: 1.4 KB (1449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
