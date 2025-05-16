## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:a0fce0bfcf2634e898415ce0ecd5b75ddd480917fe53406823dfc02821130648
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull caddy@sha256:6d7b02ba210ee90c738c9c27d3985d484cfc57ee6974fdcfb6ee0243a4f8df31
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404849429 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0892e85f8ffd386f0300eb4746d89eee36c5d32d384e7bfd12783e1e2ef6cc72`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 20:58:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:59 GMT
ENV GIT_VERSION=2.48.1
# Wed, 14 May 2025 20:58:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 14 May 2025 20:59:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 14 May 2025 20:59:01 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 14 May 2025 20:59:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 20:59:20 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 20:59:25 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 May 2025 20:59:26 GMT
ENV GOLANG_VERSION=1.23.9
# Wed, 14 May 2025 21:00:35 GMT
RUN $url = 'https://dl.google.com/go/go1.23.9.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16409aa244b672de037389e9e39115cbf82633e5fa0d4db6ec1a9191ca00a1e1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:00:36 GMT
WORKDIR C:\go
# Wed, 14 May 2025 21:16:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:16:21 GMT
ENV XCADDY_VERSION=v0.4.4
# Wed, 14 May 2025 21:16:22 GMT
ENV CADDY_VERSION=v2.10.0
# Wed, 14 May 2025 21:16:22 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Wed, 14 May 2025 21:16:34 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Wed, 14 May 2025 21:16:35 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7851e376914407ee44b63283f59444316a659b2495eb72b046adf9c0f0cdfb`  
		Last Modified: Thu, 15 May 2025 20:06:42 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62b1d0d25fa005ea190c43328cad3bdc7cd9cc2badf7295acfe710ce469df640`  
		Last Modified: Thu, 15 May 2025 20:06:42 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e8c9abc90534c50799f85d9d34c87ca357cb1958d72a1e3f48ac20190b4c9f1`  
		Last Modified: Thu, 15 May 2025 20:06:42 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a189048c383ded714ac76135ae5679d809d8f177078e99bd6e15b9224d207d95`  
		Last Modified: Thu, 15 May 2025 20:06:42 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03047ba58131093de5c276d438ec5d13ac1ea43b6a4cd8aa0d4eb115ba37a932`  
		Last Modified: Thu, 15 May 2025 20:06:43 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cc7ad0e5bfd3223f380b62113bbf1c1cd263358e1453d8119e75650809d29ea`  
		Last Modified: Thu, 15 May 2025 20:06:57 GMT  
		Size: 51.2 MB (51193109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e825425710a46fad26e66fc36ade4049046a593719d652bcbf2f24c57b7651a5`  
		Last Modified: Thu, 15 May 2025 20:06:43 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ff6dc97f8f0c2f19b5852611f113de7342481c12956850511e9251fd12a8137`  
		Last Modified: Thu, 15 May 2025 20:06:43 GMT  
		Size: 335.3 KB (335301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:882982efdecb446d3e3504e65eab58f03bed158e58f6a54ec2bb4e58b4814ae8`  
		Last Modified: Thu, 15 May 2025 20:06:43 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f51e03191c3b665fad2b78b24275caeadf41fcef79dafd7053517561ba4691`  
		Last Modified: Thu, 15 May 2025 20:06:51 GMT  
		Size: 77.4 MB (77370762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed72f2005cd738e72950eeaf7d1f9b3d5229a74fc3d88c4e05871f49a3f13c1`  
		Last Modified: Thu, 15 May 2025 20:06:44 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd34b450308b8f43d45f48b6536e70ac79bea43923dd59174f45178146da0876`  
		Last Modified: Fri, 16 May 2025 16:16:54 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c988bfce29c80e434fa2955797774a4467da9c24199ba21c932b0914b5a522e6`  
		Last Modified: Fri, 16 May 2025 16:16:54 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2b7d75369321e9e5ef4ff8b794109692ca1c10406abfc6be77606a2e83bbab`  
		Last Modified: Fri, 16 May 2025 16:16:54 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dbaaa8823edd92e5c61b44e1217c3810113526e25a9bc5932a0ebea1e38082b`  
		Last Modified: Fri, 16 May 2025 16:16:54 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:676b8e595d575273114b230b80515ee722eec0dac2cd5a3b3f1ef1fed99666e8`  
		Last Modified: Wed, 14 May 2025 21:16:39 GMT  
		Size: 2.3 MB (2305327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd65fe9967d5bbb64c54caecb4c927e3367abb5f14da03339931c9a837544cc5`  
		Last Modified: Fri, 16 May 2025 16:16:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
