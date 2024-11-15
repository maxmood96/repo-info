## `caddy:builder-windowsservercore-ltsc2022`

```console
$ docker pull caddy@sha256:c84ef1d2ad3dcd571c045dc52f483ffb222e75117345d6cb578302cbcc94fa33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `caddy:builder-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull caddy@sha256:dcf4e6df20334d36b86c5ebc212c3ae8bde7ad21418e2b037b3008756070d951
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2357995924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831d6ae584122a0cd9475b5d19cc6c81e2094d77b57f5e453f2894d85a5e3a5a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:21:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:21:05 GMT
ENV GIT_VERSION=2.23.0
# Thu, 14 Nov 2024 20:21:06 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Thu, 14 Nov 2024 20:21:07 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Thu, 14 Nov 2024 20:21:07 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Thu, 14 Nov 2024 20:21:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:21:27 GMT
ENV GOPATH=C:\go
# Thu, 14 Nov 2024 20:21:32 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Nov 2024 20:21:33 GMT
ENV GOLANG_VERSION=1.23.3
# Thu, 14 Nov 2024 20:22:39 GMT
RUN $url = 'https://dl.google.com/go/go1.23.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '81968b563642096b8a7521171e2be6e77ff6f44032f7493b7bdec9d33f44f31d'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:22:40 GMT
WORKDIR C:\go
# Thu, 14 Nov 2024 21:14:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 21:14:11 GMT
ENV XCADDY_VERSION=v0.4.4
# Thu, 14 Nov 2024 21:14:12 GMT
ENV CADDY_VERSION=v2.8.4
# Thu, 14 Nov 2024 21:14:13 GMT
ENV XCADDY_SKIP_CLEANUP=1
# Thu, 14 Nov 2024 21:14:22 GMT
RUN Invoke-WebRequest         -Uri "https://github.com/caddyserver/xcaddy/releases/download/v0.4.4/xcaddy_0.4.4_windows_amd64.zip"         -OutFile "/xcaddy.zip";     if (!(Get-FileHash -Path /xcaddy.zip -Algorithm SHA512).Hash.ToLower().Equals('cbc63529fd591742d67d68ca21c4cdb70a288cb91b20f2d9c711c34b4674d7beccd3aa774e5a6a4b7ea2c8fa92434911288c872b67fe56b8979eedd19130c041')) { exit 1; };     Expand-Archive -Path "/xcaddy.zip" -DestinationPath "/" -Force;     Remove-Item "/xcaddy.zip" -Force
# Thu, 14 Nov 2024 21:14:23 GMT
WORKDIR C:\
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9823cf794cdc6b131959ef3fd911eb792cde7fe57ba485246abcd2a87e11211`  
		Last Modified: Thu, 14 Nov 2024 20:22:47 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe89cc0c4b3209642d17eb9cdfcf090b77b9f0669ccba2f7a1cdb6408911d75c`  
		Last Modified: Thu, 14 Nov 2024 20:22:47 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a9bb1c79295d487a50e4192ad8894145f48abb94d04782589921bb3d673683`  
		Last Modified: Thu, 14 Nov 2024 20:22:46 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5e20a61ba5f492fc164b2acd288cc48615b99c92886060724f77e33e394c1d`  
		Last Modified: Thu, 14 Nov 2024 20:22:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacdad877274f45130856029a878c17a45d442a65b8f4ab110a89cc8dcab10ff`  
		Last Modified: Thu, 14 Nov 2024 20:22:45 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2abc01af7c3927b2ae518885ee8fb5d621ad3872b89e146a2ab15caad465a04a`  
		Last Modified: Thu, 14 Nov 2024 20:22:48 GMT  
		Size: 25.5 MB (25453632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7a014da4f6e2c462c5f10cdf9391bb8d4e1b3b75fafcda6cb26e3fb153d0eab`  
		Last Modified: Thu, 14 Nov 2024 20:22:44 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e91379f96289a57a1e4022a208139f35cf898f57c96fb5bc10df3e20f6ee897`  
		Last Modified: Thu, 14 Nov 2024 20:22:44 GMT  
		Size: 357.5 KB (357497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49edf46a848cfbd52d30501ace77bbaf6d8a3059313ab6d7f6208ce0dfa67427`  
		Last Modified: Thu, 14 Nov 2024 20:22:43 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f673b5e160116a001ff227b14f723d017b162b809b61081301ceb1a35a8fcdd`  
		Last Modified: Thu, 14 Nov 2024 20:22:57 GMT  
		Size: 77.4 MB (77353827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519c672468c81d41cf97550250f6e947bd8695c9ca49911d6ca2842794bd6a52`  
		Last Modified: Thu, 14 Nov 2024 20:22:43 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:867fc23cc0e0fee5768e07b262748139173b69d6ca5ec7685ec4b6dd872c9640`  
		Last Modified: Thu, 14 Nov 2024 21:14:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83de58693881d51fa43756af07f1af3047de414425e9ea17109d2a0cdab8961b`  
		Last Modified: Thu, 14 Nov 2024 21:14:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2532448d5b5c56bd84ae89dc52101d63cc50530e65e31d6630b36b83c8d9f570`  
		Last Modified: Thu, 14 Nov 2024 21:14:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1893a89e197f2b3f08c497ec8d4d9a74b2bb1bb980f162a026757de620a2b1d8`  
		Last Modified: Thu, 14 Nov 2024 21:14:27 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1537023c61f507b1ec2fd5d7f2d4977fba18b8fb1a9cdded71cafb5f4a883486`  
		Last Modified: Thu, 14 Nov 2024 21:14:27 GMT  
		Size: 2.3 MB (2329844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75f0545028e82779f07f73bc1a953771eb877208dfd36335827d5d72cdb52e24`  
		Last Modified: Thu, 14 Nov 2024 21:14:27 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
