## `golang:1-windowsservercore`

```console
$ docker pull golang@sha256:1fdce68db23b73f1744fe2734d8f3b9174a1ea5a7ac448a37bb79d51e364741c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `golang:1-windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull golang@sha256:1370d194bdf407d478409b6f4bc0698a24744804aa33ae0a48743822a00a342a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3529297169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7731d4c98507593c042bceb78fa957acb2bdcf115089ede2e737dfd948b911d2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Tue, 06 May 2025 19:30:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 May 2025 19:30:32 GMT
ENV GIT_VERSION=2.48.1
# Tue, 06 May 2025 19:30:33 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 06 May 2025 19:30:34 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 06 May 2025 19:30:35 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 06 May 2025 19:30:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:30:50 GMT
ENV GOPATH=C:\go
# Tue, 06 May 2025 19:30:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 May 2025 19:30:58 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 19:32:20 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:32:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de87335d1c9a449bcce9131efbe6f91bde0e373c2f076246e5ccd5c7e5bb215a`  
		Last Modified: Thu, 08 May 2025 18:02:38 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b75278b6e95576d6066761a4e192750f91c104615ed6937847f9a811db1ab71`  
		Last Modified: Thu, 08 May 2025 18:02:39 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db7f1ce236be07ada3a9a5354c3a1f62ca3189f3df77d1f1324df48d1703179`  
		Last Modified: Thu, 08 May 2025 18:02:38 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5507297606e034bb52351826a1095851298680c3b51a60c21c2fdfd3d961fb48`  
		Last Modified: Thu, 08 May 2025 18:02:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50c25645198c06516589af3d4db644f15e49b4ad642a3c740dd03e9e325c1df`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bc41e9c720b3f2d46b532f242a566390be3646f1d14d3ddfe5f4577b010170`  
		Last Modified: Thu, 08 May 2025 18:02:43 GMT  
		Size: 51.3 MB (51250477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b19841838c60786023a6ce0262f8f90f7b41b799ec27092b3a82a078d49663d3`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891beee3fbd5e453e88885c8f30fd4b90e519589bed3808012a38ed659e1d574`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 372.0 KB (371980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4329263bf322251e90ac57d450b8d9fb423a2149ded5b772da24c71bbb0829c`  
		Last Modified: Thu, 08 May 2025 18:02:40 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:457386aeb8f541a599579e6fc5673bd9021a21cdb88f53ed9a89693f05af447d`  
		Last Modified: Thu, 08 May 2025 18:02:44 GMT  
		Size: 82.5 MB (82502679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16ecbf12d5173fe8ec9862838f33aac4550ec2c72f42288ed4fd32bfe9a1956`  
		Last Modified: Thu, 08 May 2025 18:02:41 GMT  
		Size: 1.5 KB (1466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull golang@sha256:3915f12448cd0eeb5904605d5f8f72970708eff5eec4a540a6d0233899b8a0f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407389088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eff297937d38a806b6e722fb905457d85d7013e378adcc42bad322886799284`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Tue, 06 May 2025 19:25:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 May 2025 19:25:11 GMT
ENV GIT_VERSION=2.48.1
# Tue, 06 May 2025 19:25:12 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 06 May 2025 19:25:12 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 06 May 2025 19:25:13 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 06 May 2025 19:26:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:26:28 GMT
ENV GOPATH=C:\go
# Tue, 06 May 2025 19:26:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 May 2025 19:26:36 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 19:29:11 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:29:12 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c98d92f22ab0d5c6c5ea3f06ad91355c59e318a738fe9a058cf6fd0da506ee81`  
		Last Modified: Thu, 08 May 2025 17:22:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb78dd05f81f129b030ea299588a235605b4b9801832ad5bb55307421220dec`  
		Last Modified: Thu, 08 May 2025 17:22:22 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caee6e09da45816722ae4119e6b23b4a94f6dcee98212b92d53766faa0b05d3b`  
		Last Modified: Thu, 08 May 2025 17:22:22 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:380a4d5f00e122cb5c72104331a6ce92abdcb724c738b7866f7f30b278732770`  
		Last Modified: Thu, 08 May 2025 17:22:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e487273d43722bcdbb731db8d220c06f6b424df8c9a8962b050ddd00e5e96c30`  
		Last Modified: Thu, 08 May 2025 17:22:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4072413ce3a00860917addef04cd728dbb113dc489fb8d61e0cf151c4332c6ee`  
		Last Modified: Thu, 08 May 2025 17:22:32 GMT  
		Size: 51.2 MB (51210564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f119da440b47772ac2bc4b137513245e424af28de85eb880ed398e0d7d5138`  
		Last Modified: Thu, 08 May 2025 17:22:26 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7609a3365fbbfe8598bd85d9ff49ca733041b13747a76c618c5ed38c6de4c7ee`  
		Last Modified: Thu, 08 May 2025 17:22:27 GMT  
		Size: 314.6 KB (314611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65952ef9921c0868bb6a5035d8db0d15d71b6956f5836a4dacdf34fd63cb4aa0`  
		Last Modified: Thu, 08 May 2025 17:22:29 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a2ab2fb53c0e7db78829d23691aec4105c117d07fa842fa889012c652eba1a`  
		Last Modified: Thu, 08 May 2025 17:22:42 GMT  
		Size: 82.3 MB (82270922 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c53bae34a3be3d2830ea7605006ae635b27040e56aa0d56f441a446f630978`  
		Last Modified: Thu, 08 May 2025 17:22:32 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:1-windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull golang@sha256:0c164c2158d96aeaf0741a2141825d7ab550435781e0166d1b75c5572105b06d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2299418491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e5d3f06ff48c1a7815bc376a7c046498fb55cfe9c6274cb4a8d76099b72ead`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Tue, 06 May 2025 19:25:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 May 2025 19:25:02 GMT
ENV GIT_VERSION=2.48.1
# Tue, 06 May 2025 19:25:03 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 06 May 2025 19:25:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 06 May 2025 19:25:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 06 May 2025 19:26:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:26:12 GMT
ENV GOPATH=C:\go
# Tue, 06 May 2025 19:26:20 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 May 2025 19:26:20 GMT
ENV GOLANG_VERSION=1.24.3
# Tue, 06 May 2025 19:27:59 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 May 2025 19:28:01 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f16e060e22dafd6121928bd065c83b232311afee2b80e769abc2fb02a2ae54`  
		Last Modified: Thu, 08 May 2025 18:02:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:315302ea6280bf623ff7abf9a3a4f9977770df18a5a739ebbfa4348d0911374b`  
		Last Modified: Thu, 08 May 2025 18:02:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ddf5b410ed529f9d31e96be1e35447e4553b0eaa108709ac4846c52afacdc2b`  
		Last Modified: Thu, 08 May 2025 18:02:42 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a55cb71485ce10175e38aa8fefcbc9993c7b2d0a32a052f7307181d57aeea8e`  
		Last Modified: Thu, 08 May 2025 18:02:42 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f15d28ea246f8587e6b26f38f837a70060db4a7b5d280f5a07e1685312802a7`  
		Last Modified: Thu, 08 May 2025 18:02:43 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:984fb95f5ccec8206e4f4b16668cd527a036b9d08af8c37a14601c4267ba5009`  
		Last Modified: Thu, 08 May 2025 18:02:46 GMT  
		Size: 51.2 MB (51221682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565b8e66b070e6345bdbbaa0d4bfcb0ea9542b3d220256bc2fdf01afb60bcb56`  
		Last Modified: Thu, 08 May 2025 18:02:43 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fcd74320a25667a20867d5b1c833b29698ab8fd089a8e9151a16283ceac8411`  
		Last Modified: Thu, 08 May 2025 18:02:43 GMT  
		Size: 353.3 KB (353297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9da0e0cd6cbb93e413c7bd667fcba35f51c902dab22773b482152e47733134`  
		Last Modified: Thu, 08 May 2025 18:02:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea653b59badf9cb2d72c67598913dc0f4862b5075668788e43208a4d3ba9aa95`  
		Last Modified: Thu, 08 May 2025 18:02:48 GMT  
		Size: 82.3 MB (82307168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45178303a357983920b83090c5e10a8a7f8378647123a996d7be1c999d62ae4c`  
		Last Modified: Thu, 08 May 2025 18:02:45 GMT  
		Size: 1.5 KB (1480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
