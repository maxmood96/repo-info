## `golang:windowsservercore`

```console
$ docker pull golang@sha256:621b40e8c18c9b100d65f7d17d4e3245fb256bfc95a3f7dafd9c5a60784700de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `golang:windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull golang@sha256:93c19e2c5aaa0ed2d17a1ac45bdfe26ac1181cb6016710f76a12cd3c1c9c515f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2215720565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7c4b970e3840ac10b658acac4071cc5c93bc474e8ecd00c998aa3dc2d28bb02`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Tue, 02 Jul 2024 22:06:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 22:06:20 GMT
ENV GIT_VERSION=2.23.0
# Tue, 02 Jul 2024 22:06:20 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 02 Jul 2024 22:06:21 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 02 Jul 2024 22:06:22 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 02 Jul 2024 22:07:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 22:07:19 GMT
ENV GOPATH=C:\go
# Tue, 02 Jul 2024 22:07:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jul 2024 22:07:26 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 22:09:19 GMT
RUN $url = 'https://dl.google.com/go/go1.22.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '59968438b8d90f108fd240d4d2f95b037e59716995f7409e0a322dcb996e9f42'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 22:09:21 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f873b4f46384f1cd0aadb3a9cd33bd1403dd1dbd9626a24820bf9b15b08092a`  
		Last Modified: Tue, 02 Jul 2024 22:09:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b54a9c02aa9f6bd3d31b7ac94856f87a460bdbdb829c81d619d94430fea1360`  
		Last Modified: Tue, 02 Jul 2024 22:09:28 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c1368d1e6e61ae6d5dbeef83ea7cff04b138461fc5123a5a918062c35d5491`  
		Last Modified: Tue, 02 Jul 2024 22:09:27 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac85260a68a5159fd4f096dd016325fbe47368e2942bb696148e14a676cfcc5`  
		Last Modified: Tue, 02 Jul 2024 22:09:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26c4b5c590e6cced662fd6dfeecb683367d81aad6c4eab59defbe14f0b678ed`  
		Last Modified: Tue, 02 Jul 2024 22:09:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bad10521e953465503e5baee9533519887c77c40508f3b319811dd11bccb154`  
		Last Modified: Tue, 02 Jul 2024 22:09:29 GMT  
		Size: 25.5 MB (25456672 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fae142fe755c0b71663d37734e00abf856d3ebd51b128dd8181b76c312a9d3d`  
		Last Modified: Tue, 02 Jul 2024 22:09:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72ec2298cee8798116b94370768cc0079d9b8201aef587d802079858ce16f0e`  
		Last Modified: Tue, 02 Jul 2024 22:09:25 GMT  
		Size: 322.3 KB (322258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802d117ad71d9fb0954efd0c80c4d120df23a562b1adf4c4c7367fc38b2ef4ca`  
		Last Modified: Tue, 02 Jul 2024 22:09:25 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1fbac41a0b11f9b7d2672d821068f3e22d4864f69ce45ca8dcdb6dc791b3210`  
		Last Modified: Tue, 02 Jul 2024 22:09:35 GMT  
		Size: 71.7 MB (71740973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9c90f24ac0d328dd58342ba0aec720b29301276e28ba58bcd35803d79981b0`  
		Last Modified: Tue, 02 Jul 2024 22:09:25 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `golang:windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull golang@sha256:3ce39f6a99b3e9ea8da72e607fc7ab46287c45d6612f4823547d202cf03ee521
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2318446470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e267ad186af406689d831de306b6f664b2ef5d901452b36f5e928494efd74050`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Tue, 02 Jul 2024 22:06:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 22:06:09 GMT
ENV GIT_VERSION=2.23.0
# Tue, 02 Jul 2024 22:06:09 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 02 Jul 2024 22:06:10 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 02 Jul 2024 22:06:11 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 02 Jul 2024 22:07:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 22:07:43 GMT
ENV GOPATH=C:\go
# Tue, 02 Jul 2024 22:08:06 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 02 Jul 2024 22:08:07 GMT
ENV GOLANG_VERSION=1.22.5
# Tue, 02 Jul 2024 22:10:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '59968438b8d90f108fd240d4d2f95b037e59716995f7409e0a322dcb996e9f42'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 02 Jul 2024 22:10:58 GMT
WORKDIR C:\go
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
	-	`sha256:d0634ecefeb73103367a149571ca87b29ce173ce2ddb56ad9d3daf95ef1ae413`  
		Last Modified: Tue, 02 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f22ee6e58359f08f771329b2e79f555fe616dd84e03a802c17f68885738a08`  
		Last Modified: Tue, 02 Jul 2024 22:11:06 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bb0f98cbf39d2bf0c78f97a7551a0b0fd2e2d3a682debc2c6eb6661213f46b`  
		Last Modified: Tue, 02 Jul 2024 22:11:04 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37297a0ed6022f23eb3bdc610e59f71ae723e2d7de240eb390416ff3271ffb72`  
		Last Modified: Tue, 02 Jul 2024 22:11:04 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac1df863730967ccf74d3e803a0ee35eaa4e6fd757d9f194fdeefce01b0c60f`  
		Last Modified: Tue, 02 Jul 2024 22:11:04 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db32394d77f4812f60903c2e571bfb10051f699127817cf1b885b45355c564f`  
		Last Modified: Tue, 02 Jul 2024 22:11:06 GMT  
		Size: 25.6 MB (25597704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86f86050974677ffce63b023cc1153595b011f1ef6dc3fdac74db46b35180a9d`  
		Last Modified: Tue, 02 Jul 2024 22:11:02 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa999c7fcaf95ec9b123669351a92a3cb079d8a5d06dfa670e554785853c2a`  
		Last Modified: Tue, 02 Jul 2024 22:11:02 GMT  
		Size: 366.7 KB (366725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b3a307eca3fc695f1344b28cd13b9922d113bf7b658605cecf802545eef4e29`  
		Last Modified: Tue, 02 Jul 2024 22:11:02 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e5a8acfb8172e73d5ff7247838af36ef2c14ddd953bc72fc49cbd83d9ae139`  
		Last Modified: Tue, 02 Jul 2024 22:11:13 GMT  
		Size: 71.8 MB (71790362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9846de757ac32852acd928ab8fc1c91e2da1581b98100af1d187fe2736651071`  
		Last Modified: Tue, 02 Jul 2024 22:11:02 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
