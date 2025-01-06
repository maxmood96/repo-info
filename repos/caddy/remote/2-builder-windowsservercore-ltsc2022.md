## `caddy:2-builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c0a26b140e3171d9a599edf74879018e64c91a8ef7e8117d895399a56be526dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `caddy:2-builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull caddy@sha256:060ca64a20787cdeae9e6a7f72736838887c5b82a69f0fa9515044aff1729658
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2359322612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:425c207f173a0b70ac4e5757357b4b5f71f4de0aea6cf03fffe21a832196a14b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:29 GMT
ENV GIT_VERSION=2.23.0
# Wed, 11 Dec 2024 20:41:30 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 11 Dec 2024 20:41:31 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 11 Dec 2024 20:41:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:41:51 GMT
ENV GOPATH=C:\go
# Wed, 11 Dec 2024 20:41:57 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 11 Dec 2024 20:41:57 GMT
ENV GOLANG_VERSION=1.23.4
# Wed, 11 Dec 2024 20:43:05 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 11 Dec 2024 20:43:07 GMT
WORKDIR C:\go
# Wed, 11 Dec 2024 21:45:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 21:45:59 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 11 Dec 2024 21:46:00 GMT
ENV CADDY_VERSION=v2.8.4
# Wed, 11 Dec 2024 21:46:01 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 11 Dec 2024 21:46:09 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 11 Dec 2024 21:46:10 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f2203f205368ce649ffd4367d83cb7d0e0f349edd4a73d17bf72e1d1fd45547`  
		Last Modified: Wed, 11 Dec 2024 20:43:12 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a929050203563fde4afe1d48374621524ea8726dc8ca55d3c22d0ac7a798594`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1be8f168e721557e602e0b7a3a7cb7e068d12e159af7b67cbd570277d67b6d3`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a047a2e43f164719e30219f432eae6c44e556b5a49ad8de5c356eef5ceb9f2`  
		Last Modified: Wed, 11 Dec 2024 20:43:11 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b538affaf25305d64f324539f173d0eb2d2dd465cb1762b082450ad4c797f27c`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b23c69a8ef4d7541c4f17aa73bdd2bc059fbf9e06bb80dba0c6780214385b946`  
		Last Modified: Wed, 11 Dec 2024 20:43:13 GMT  
		Size: 25.4 MB (25433638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec8adf8499c2eb9b67d228fba4c9e69a29a2d7060f8b7c5592eacc3be4421710`  
		Last Modified: Wed, 11 Dec 2024 20:43:09 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb262fe2ef81142570e16f48f8f03d4031993f7f4bdd1e8ddc6130f5ac401023`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 339.0 KB (338961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b81c31620602735496201938ab0373d338f5d0422cdb2fe31bf91e703561180`  
		Last Modified: Wed, 11 Dec 2024 20:43:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027a3cd836a09077c7888a8a16d4e7bdf054357c81b2dfc19d8a0d373c88f51d`  
		Last Modified: Wed, 11 Dec 2024 20:43:22 GMT  
		Size: 77.3 MB (77349783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6072f4215eedb6bd6a3744f556ae0cd5807bf437d9168f5f06a714a4935e11ad`  
		Size: 1.5 KB (1475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb0a4fe644b4fc0b92ce2fe2d5b6e9f4a44c4c93ac976329f56267a6b594385`  
		Last Modified: Wed, 11 Dec 2024 21:46:16 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2864d84752e650e6559d2323e6969b50efb62edbeeae473b99493337769662a`  
		Last Modified: Wed, 11 Dec 2024 21:46:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b4e5b88d32c4b3cb3a998a93447da5f221d454eb496d6c377639150d682cffe`  
		Last Modified: Wed, 11 Dec 2024 21:46:14 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4642e919865ce7eedd45587cb7c22fc721babb388b7005d42a51874b3921feec`  
		Last Modified: Wed, 11 Dec 2024 21:46:14 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b5ac225017fd64995c1a32d3cc63d71f2d1363fe562e285ca864b196b85ab8`  
		Last Modified: Wed, 11 Dec 2024 21:46:14 GMT  
		Size: 2.3 MB (2309742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08607fd13dbe050e2ef92fb52cff03e287cc4444a996f742a3d00b9040332f32`  
		Last Modified: Wed, 11 Dec 2024 21:46:14 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
