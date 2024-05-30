## `caddy:builder-windowsservercore-1809`

```console
$ docker pull caddy@sha256:4c00208a7869c08a9cb6ef821d15eafeac675e507194f54957fc91cbaf787e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `caddy:builder-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull caddy@sha256:31ea6cb75b5ad08fb08500916a0a249d3cd3fac67e2062428129f1255fd747a6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2279344819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72d816cca71514d888c55882cedda59c9e63b2873912ab19d832e8f0c192cfa6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 15 May 2024 22:51:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 May 2024 22:51:52 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 May 2024 22:51:53 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 May 2024 22:51:54 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 May 2024 22:54:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:54:20 GMT
ENV GOPATH=C:\go
# Wed, 15 May 2024 22:54:45 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 May 2024 22:54:45 GMT
ENV GOLANG_VERSION=1.22.3
# Wed, 15 May 2024 22:58:57 GMT
RUN $url = 'https://dl.google.com/go/go1.22.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'cab2af6951a6e2115824263f6df13ff069c47270f5788714fa1d776f7f60cb39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 May 2024 22:58:59 GMT
WORKDIR C:\go
# Thu, 30 May 2024 19:58:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 30 May 2024 19:58:09 GMT
ENV XCADDY_VERSION=v0.4.2
# Thu, 30 May 2024 19:58:10 GMT
ENV CADDY_VERSION=v2.8.1
# Thu, 30 May 2024 19:58:10 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 30 May 2024 20:00:16 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.2/xcaddy_0.4.2_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('8ef75d6141029a1f2a2b5aefdee44f0704366302c7416e2136341a3c5910d7809e713cf3d965512f1440473b99c177a0d19789e20601628462747a2d6bc71d27')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 30 May 2024 20:00:16 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936b721870b6ca4ac86a4dd17a9efa72d3bbbc3e2f4db24604ab3e5529ac9483`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231059aab43e3c4c95c41ffa0eaaf0a505c5a3e17b120dfc894682b1930a3968`  
		Last Modified: Wed, 15 May 2024 22:59:06 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83508e294490f2fa915d9cd65227cc8e8661207b15aa2cfdaf074ff8ae7bb4d4`  
		Last Modified: Wed, 15 May 2024 22:59:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d676bfa2282c568dda9fa4af2f2e6d235ebca82a6c367717bf083bad7dd8b3a`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f3161f170f396d7c78bb77ee80c5b634beca05d901f05396abeab4e06be7f5`  
		Last Modified: Wed, 15 May 2024 22:59:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c76d7a1b3a9e63480abdc848b1fd30a006301a1e471568b571a209702755daa`  
		Last Modified: Wed, 15 May 2024 22:59:07 GMT  
		Size: 25.6 MB (25574881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3b1dcf82dafd8633a79265dca42870493640409651674a91b43f2adf04c165a`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29dac5092add95bf42e98f932737023e0c6ef6ca428f58802291c2cc4c9559b7`  
		Last Modified: Wed, 15 May 2024 22:59:03 GMT  
		Size: 345.9 KB (345903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7992418d5500de5ceeac2fa4f57b54353f18a13b476f19add206e269ef1e6fc`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40ad77f522384c92c66907f62599064a34ebdd67556de4d2570970de37d46d8`  
		Last Modified: Wed, 15 May 2024 22:59:13 GMT  
		Size: 71.7 MB (71743817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a716ef2ea189a02632506ad12bdad7990790c5792d611ac5831fdfa2896ac298`  
		Last Modified: Wed, 15 May 2024 22:59:02 GMT  
		Size: 1.4 KB (1448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fbedff9109d9c95af2643ac63a5cacb1b2bc7f05ffacb6f738c7bd71a8eccec`  
		Last Modified: Thu, 30 May 2024 20:00:20 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca153f0633c0d2c02ede7da833835063735438dffc496ac2f6e096fd2ffba56`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4e8add55d5a48aeb589d70b12c70950ab9d36ea1844e46a0c3243431fc5d023`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c23241851e0ece31bec24fbcc64f6a45ad49e757b6d83fd867de1db46ef1750`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1af3c5163dc4db242d8d318f53106e3edab0cbfcdee3719d51d1eb44031b1f`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 2.0 MB (1951704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fab58945a98d4f4ef5a6f69ce2d9c53b14cdfdb6bbf677de534c9df7f2a5d11`  
		Last Modified: Thu, 30 May 2024 20:00:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
