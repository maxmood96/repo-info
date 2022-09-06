## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:fe0d29bba97b1d3dc69101d71a946a9c287ae54e09bf74ceda0862cbcc9c8c01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.887; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.887; amd64

```console
$ docker pull caddy@sha256:74e5c262569cc62e28d6a0c26d55b346fe44a6e237885f79cd046dc67e8feee9
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2495017603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cdfe05622c54c44a1ea1396c550b4a927c74c0d24e8e2ac3bb5438ab3a7dfb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Sat, 06 Aug 2022 02:59:35 GMT
RUN Install update 10.0.20348.887
# Wed, 10 Aug 2022 12:11:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 12:49:45 GMT
ENV GIT_VERSION=2.23.0
# Wed, 10 Aug 2022 12:49:46 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 10 Aug 2022 12:49:47 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 10 Aug 2022 12:49:48 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 10 Aug 2022 12:50:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 10 Aug 2022 12:50:19 GMT
ENV GOPATH=C:\go
# Wed, 10 Aug 2022 12:50:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 06 Sep 2022 19:32:19 GMT
ENV GOLANG_VERSION=1.18.6
# Tue, 06 Sep 2022 19:35:26 GMT
RUN $url = 'https://dl.google.com/go/go1.18.6.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '480b7212ab1d152d5e3fc382ac34d3dd26bf637ae4537c35b4b554ede8a36b47'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 06 Sep 2022 19:35:28 GMT
WORKDIR C:\go
# Tue, 06 Sep 2022 20:12:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 06 Sep 2022 20:12:12 GMT
ENV XCADDY_VERSION=v0.3.0
# Tue, 06 Sep 2022 20:12:13 GMT
ENV CADDY_VERSION=v2.5.2
# Tue, 06 Sep 2022 20:12:15 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 06 Sep 2022 20:12:45 GMT
RUN [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.3.0/xcaddy_0.3.0_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('63d60531a924a0618a15907a276a67745186a1f92077a48aff2fb68b549b7b80a92238f8a8dca6af82e1840dcdac479e32672b7d62f118c77363be6fae5281a6')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 06 Sep 2022 20:12:46 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:97b25a378238b615dc51216c4d87ce17fd3cc3dca9db458e8705d1a4c17e3bb7`  
		Size: 880.0 MB (880025531 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a5e3787c778295a5877e0381020b02273a985f7db2dd483ddff586869546e4c`  
		Last Modified: Wed, 10 Aug 2022 12:42:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89a6a7fe48246bae14c787b3f68ad97b9d649ad0f0ebc9d654eefa90a681bc4`  
		Last Modified: Wed, 10 Aug 2022 13:24:02 GMT  
		Size: 1.4 KB (1394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:700d78f1a37edaf812b6b377963b4ad46402a067ea09535d282788b017da5ce1`  
		Last Modified: Wed, 10 Aug 2022 13:24:00 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97de872a1f90401514b1fd4224785cb2d6301b849142a6612abe22f91f6bef42`  
		Last Modified: Wed, 10 Aug 2022 13:23:58 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89af222c4e6bc5d4bc31acd2d1cf98a0258bcacf3d9a8ecd43f1705eac313351`  
		Last Modified: Wed, 10 Aug 2022 13:23:57 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84a406a2386e04b60cf969f8eb5872e6749e87b083a11e09bf35dc23634c489`  
		Last Modified: Wed, 10 Aug 2022 13:24:05 GMT  
		Size: 25.7 MB (25713776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3810a29e3add75397336456fd6d35a417140bcfa4ba740025ae5377ffd17b83b`  
		Last Modified: Wed, 10 Aug 2022 13:23:55 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d8ff3f35e00b20d78e9808298cedaf198a5e5733be3735faa63d2784a0c5848`  
		Last Modified: Wed, 10 Aug 2022 13:23:56 GMT  
		Size: 558.2 KB (558170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd2ee5093a5c822d5f44ddd45359e9f4b4c3e6dd9c34972e632d74841f81fc9`  
		Last Modified: Tue, 06 Sep 2022 19:52:05 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e52a0db1305c48db78b1417cb67ba2e8677a7b3493f4c01143a731fa9712fc9`  
		Last Modified: Tue, 06 Sep 2022 19:52:41 GMT  
		Size: 149.9 MB (149895643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a59c3c05e4fcec3faa1d65ef013bc97e2f831d0570db26f58c5fda66b5a8f7e`  
		Last Modified: Tue, 06 Sep 2022 19:52:05 GMT  
		Size: 1.5 KB (1537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa9d0b92e053d3cce8a090a1a383b44271c07dece64e96dc9cf467758cc8c56c`  
		Last Modified: Tue, 06 Sep 2022 20:13:30 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23ef9a1c5ef13d9a22457d28aa395948c469819ce88e990a637cb238e15a2cde`  
		Last Modified: Tue, 06 Sep 2022 20:13:28 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b86a6269add1abbcb1b0ff1103618d72a08f925461b528a6128245c35d381e67`  
		Last Modified: Tue, 06 Sep 2022 20:13:27 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5025b5955b1830e84916b28695049d3d61f3e05492fbaf8a471fdcd4977ad070`  
		Last Modified: Tue, 06 Sep 2022 20:13:28 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2c2aab23d834f4bd6cb85ee8b93d72ad562d73fd7b0b23504f9d32fcbf9efa`  
		Last Modified: Tue, 06 Sep 2022 20:13:28 GMT  
		Size: 1.9 MB (1942308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75c13f66dfde8ff4709dbc032e5cdb6cc3bb71b154b513674890d92118b449b`  
		Last Modified: Tue, 06 Sep 2022 20:13:28 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
