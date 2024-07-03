## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:5d81e18b0979190ec73dbbcc2cbeba316db2cd685c8d4c5e105c2e40da256986
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5936; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5936; amd64

```console
$ docker pull caddy@sha256:3ac26ce9060cdc3f296a525600e123ee3a55adf4510e52be07e4b60d0daa2f86
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2320403777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74a6a1011f379bb5360888890bc8bd0b2118c52faecdd2d4b1a10298516f71e9`
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
# Tue, 02 Jul 2024 22:59:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jul 2024 22:59:37 GMT
ENV XCADDY_VERSION=v0.4.2
# Tue, 02 Jul 2024 22:59:38 GMT
ENV CADDY_VERSION=v2.8.4
# Tue, 02 Jul 2024 22:59:39 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 02 Jul 2024 23:00:08 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 02 Jul 2024 23:00:09 GMT
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
	-	`sha256:9bd684ba67d4ce776716bd2970bc91f10918e48569f72587bdcf210c0e74a041`  
		Last Modified: Tue, 02 Jul 2024 23:00:15 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61076e1cc3ef1d17b21f6816ab0c08ec68e187cb30966fe833d2f49301e340e2`  
		Last Modified: Tue, 02 Jul 2024 23:00:13 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b2786a731bde7ebde65a41495932ec021f4a2ca844208ccafffb81a0b2bef7f`  
		Last Modified: Tue, 02 Jul 2024 23:00:13 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b27f52cc7b4833402ddddd75105df51b0ef044ba49f2cf27123940fb34250650`  
		Last Modified: Tue, 02 Jul 2024 23:00:13 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc3638e8af757912c4870e8c5c5473040ea0a02c00f2305117a582f169d203f8`  
		Last Modified: Tue, 02 Jul 2024 23:00:14 GMT  
		Size: 2.0 MB (1950819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33e4a900b2be841331544e9225fa911db370baa0c9046a9d25320883f82b48e`  
		Last Modified: Tue, 02 Jul 2024 23:00:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
