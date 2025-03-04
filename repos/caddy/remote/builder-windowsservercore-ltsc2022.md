## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:1ea22c1485abdb53d40fff92fd5718d2c3b729dd40375dd43fc87f76dccec932
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull caddy@sha256:59bf96e076ab97eac4c799db3525af4e2558776630aebedae8e127b39984f98f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2369273250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b49e8458337a722977e06e8e4c5f65706b7309bf06f973f857f20c52ae07426`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 07 Feb 2025 21:10:03 GMT
RUN Install update 10.0.20348.3207
# Tue, 04 Mar 2025 21:16:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 21:16:57 GMT
ENV GIT_VERSION=2.23.0
# Tue, 04 Mar 2025 21:16:58 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 04 Mar 2025 21:16:58 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 04 Mar 2025 21:16:59 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 04 Mar 2025 21:18:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 21:18:12 GMT
ENV GOPATH=C:\go
# Tue, 04 Mar 2025 21:18:23 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 04 Mar 2025 21:18:24 GMT
ENV GOLANG_VERSION=1.23.7
# Tue, 04 Mar 2025 21:20:32 GMT
RUN $url = 'https://dl.google.com/go/go1.23.7.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'eba0477381037868738b47b0198d120a535eb9a8a17b2babb9ab0d5e912a2171'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 04 Mar 2025 21:20:33 GMT
WORKDIR C:\go
# Tue, 04 Mar 2025 21:57:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 04 Mar 2025 21:57:39 GMT
ENV XCADDY_VERSION=v0.4.4
# Tue, 04 Mar 2025 21:57:39 GMT
ENV CADDY_VERSION=v2.9.1
# Tue, 04 Mar 2025 21:57:40 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Tue, 04 Mar 2025 21:58:52 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Tue, 04 Mar 2025 21:58:53 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bc4873980ff6a1dec3c10adb1f289ccf73e4c47c8694420e8ff929f1476ada`  
		Last Modified: Tue, 11 Feb 2025 18:38:32 GMT  
		Size: 801.7 MB (801665588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a7ab61e70e629d49431781c6a50bde10e9c987a1346773139b2b6c182426c71`  
		Last Modified: Tue, 04 Mar 2025 21:20:38 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7a00cf7db1dd9a9acbd5f30fcb2eb8ee4db56ca36b8652ad6d7419e13af49e1`  
		Last Modified: Tue, 04 Mar 2025 21:20:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cf3a79c464b334a38afa99d48f27c81195969537e4c6aaad41d126abb6061e0`  
		Last Modified: Tue, 04 Mar 2025 21:20:38 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a775b3f795f8650d6041670e97556c687f564acf5eacf4851543d39b40bce43`  
		Last Modified: Tue, 04 Mar 2025 21:20:38 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daef7f0287cf64d836892f4b8955ccc82bea9b3001934bc2deb324e84340cb61`  
		Last Modified: Tue, 04 Mar 2025 21:20:37 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013092b2bb81df17f38f78d9cd306fe0db318698e98868d2f52746ec250fd0b0`  
		Last Modified: Tue, 04 Mar 2025 21:20:40 GMT  
		Size: 25.5 MB (25451857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90dbc0c1e6c29f07ac0c6eba937c1739f6247b393b625c627777a961e438af92`  
		Last Modified: Tue, 04 Mar 2025 21:20:36 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082340644d0af82151cfac0fe7d39f487b3a7f5ce0644205414217c34cc10472`  
		Last Modified: Tue, 04 Mar 2025 21:20:36 GMT  
		Size: 313.4 KB (313380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f81c4f240161589af59d98ade7afa43a9014e901b7c507787d0224806a4979`  
		Last Modified: Tue, 04 Mar 2025 21:20:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abb8dd629329aa1927e01c08f7676dee13a74c7196b68c6fd92dcda550c7d79f`  
		Last Modified: Tue, 04 Mar 2025 21:20:48 GMT  
		Size: 77.3 MB (77345240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae85459bdac4570fe180b4e354826d2d93702189fd102aa08d3583bcd68b7667`  
		Last Modified: Tue, 04 Mar 2025 21:20:36 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dee54201de00999d9098f0722cdf31d6d0b755b4ad5def4851f7744282c7b6`  
		Last Modified: Tue, 04 Mar 2025 21:58:56 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0001ca44da3cf66d87b428c434fe8adfc280970d7a597c0addf8d238b7e1505e`  
		Last Modified: Tue, 04 Mar 2025 21:58:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed420f2da0a3400d9d72a13f58537a99f6ea944bc796dbd5c9e9286b28a59c53`  
		Last Modified: Tue, 04 Mar 2025 21:58:55 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd7fd7d165a2fd8631345716d0a752f73e382ff914ce3991cf28efd83946a53`  
		Last Modified: Tue, 04 Mar 2025 21:58:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60ea00a40ac9288944ebaa6fa41a1f4bc488f43c317d7c46aff6ce8591710b2c`  
		Last Modified: Tue, 04 Mar 2025 21:58:55 GMT  
		Size: 2.3 MB (2287906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f899f0227f213a6c47c0436291e38a9b3e480e5567dac6464825dd9d51bc4e7`  
		Last Modified: Tue, 04 Mar 2025 21:58:55 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
