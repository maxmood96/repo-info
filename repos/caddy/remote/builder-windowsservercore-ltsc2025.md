## `caddy:builder-windowsservercore-ltsc2025`

```console
$ docker pull caddy@sha256:f341412eb8281a755dfce103b5fb92a81fce179031427c18fab7a025b5f9af4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `caddy:builder-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull caddy@sha256:dc422505a2158b1e6ef10ea33a742c88b11ba76afccc3533a9b651d571ec878b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2081273737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80d2cbf914c68ba53933eb85c388939c884eb000e07e00039b2cad06c91fa5d3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:52:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:57:18 GMT
ENV GIT_VERSION=2.48.1
# Tue, 10 Feb 2026 22:57:19 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 10 Feb 2026 22:57:19 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 10 Feb 2026 22:57:20 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 10 Feb 2026 22:57:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:57:33 GMT
ENV GOPATH=C:\go
# Tue, 10 Feb 2026 22:57:38 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 10 Feb 2026 22:57:38 GMT
ENV GOLANG_VERSION=1.25.7
# Tue, 10 Feb 2026 22:58:53 GMT
RUN $url = 'https://dl.google.com/go/go1.25.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'c75e5f4ff62d085cc0017be3ad19d5536f46825fa05db06ec468941f847e3228'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 10 Feb 2026 22:58:55 GMT
WORKDIR C:\go
# Tue, 10 Feb 2026 23:39:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:39:10 GMT
ENV XCADDY_VERSION=v0.4.5
# Tue, 10 Feb 2026 23:39:11 GMT
ENV CADDY_VERSION=v2.10.2
# Tue, 10 Feb 2026 23:39:11 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 10 Feb 2026 23:39:21 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.5/xcaddy_0.4.5_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('652857d019f3e1772b154b33f2479d8f17f4b10818802363737d35601c4cd51dc9a9ba0b3c64cdada9fe6bdcebb4395d0561b2ca302ae1219b288758c01911c1')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 10 Feb 2026 23:39:21 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c98dbe9f1f0558e249573b12845ab1eecd63a28b82c4d7dd0c89342195382d`  
		Last Modified: Tue, 10 Feb 2026 22:53:53 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:251c3d72ec6a1d7676d8fa7e6af9fcf34bf0ecb07a1ef1805d6b843e0632d4d7`  
		Last Modified: Tue, 10 Feb 2026 22:59:02 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a78b4505ca74331a9760e657c5468a5c8544a63ca677628ea8029bbb13ba8fa`  
		Last Modified: Tue, 10 Feb 2026 22:59:00 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309d35d4699da17df5046f80277300d105ab415162ee7a6ecb8552c4cfd247b1`  
		Last Modified: Tue, 10 Feb 2026 22:59:00 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86e68594acdba1ce1abfba05743da4d1c0f21a8d83ab65efe4e2e3395188ef9a`  
		Last Modified: Tue, 10 Feb 2026 22:59:00 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f7df85cfb2b210e8b90c6d0c9d4cbb71328ddb8eff48f7428a79486204346b`  
		Last Modified: Tue, 10 Feb 2026 22:59:06 GMT  
		Size: 51.2 MB (51225626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2a54d8b384c442bf6b91fcecc7b0ce8525c0cd3d86bfcfd6e98084116c589e5`  
		Last Modified: Tue, 10 Feb 2026 22:58:58 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e0f7c88184089406c87f817ff8795bd5152837545a7f8ece28a00e44b05de62`  
		Last Modified: Tue, 10 Feb 2026 22:58:59 GMT  
		Size: 357.1 KB (357115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c4c84621f1581972a92a4a59b600bde5898723349ce42ab50ec427d4098c798`  
		Last Modified: Tue, 10 Feb 2026 22:58:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07fea59d2775697bded3d77cb2164a7b828ac0a28b3f1c693d3a9d041a26c48`  
		Last Modified: Tue, 10 Feb 2026 22:59:09 GMT  
		Size: 62.6 MB (62574154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4050fb7d4bb34edf3762602a3d1abfd67f61cb3e54822384b9f5b99ad501a8bb`  
		Last Modified: Tue, 10 Feb 2026 22:58:58 GMT  
		Size: 1.5 KB (1452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85aade87d9d0b2de2c57b3032a7c39359898074ccc3d8089af433c223b0f007a`  
		Last Modified: Tue, 10 Feb 2026 23:39:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f1fe9824aa02c06cc027f2ac38772455622615ac7460314704a3512ea8559d`  
		Last Modified: Tue, 10 Feb 2026 23:39:25 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f139f229bc81448c3864dae1786b054bf2f431c450d6c58e7bfac6a9fea7578`  
		Last Modified: Tue, 10 Feb 2026 23:39:25 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13dbf3dfa24e065ed733fba2f2223b2304adf9f82424f7a78da70a4ff9c163d1`  
		Last Modified: Tue, 10 Feb 2026 23:39:26 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f185c2d652253d42ca337ead716cd4bbcd1f883d2eabb3ce088bd0b829c9d2`  
		Last Modified: Tue, 10 Feb 2026 23:39:26 GMT  
		Size: 2.3 MB (2339632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d74a105cbbebfbfce72718387812a180bd188d7a3eeabe97b0410294b6ff0c9`  
		Last Modified: Tue, 10 Feb 2026 23:39:25 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
