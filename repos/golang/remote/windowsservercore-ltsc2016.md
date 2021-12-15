## `golang:windowsservercore-ltsc2016`

```console
$ docker pull golang@sha256:39afa9a1dbbc2e4f995df9df93823cdf51a06786e9e79b304ce7feca35473f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4825; amd64

### `golang:windowsservercore-ltsc2016` - windows version 10.0.14393.4825; amd64

```console
$ docker pull golang@sha256:ef241ee21778edcf2279509fbf43d492938f471ba8ae7b03548688badb2500bf
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6450360107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:310cc40b76dc3bb98696749abd725149a54ad822446937efc277ddf1e4469a4a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 08 Dec 2021 08:38:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 15 Dec 2021 00:54:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Dec 2021 00:54:10 GMT
ENV GIT_VERSION=2.23.0
# Wed, 15 Dec 2021 00:54:11 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 15 Dec 2021 00:54:12 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 15 Dec 2021 00:54:13 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 15 Dec 2021 00:56:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 00:56:06 GMT
ENV GOPATH=C:\go
# Wed, 15 Dec 2021 00:57:05 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 15 Dec 2021 01:16:47 GMT
ENV GOLANG_VERSION=1.17.5
# Wed, 15 Dec 2021 01:21:14 GMT
RUN $url = 'https://dl.google.com/go/go1.17.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '671faf99cd5d81cd7e40936c0a94363c64d654faa0148d2af4bbc262555620b9'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 15 Dec 2021 01:21:16 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2d026d646213ccf73d9f0584941d108253d62e73df2a74e070776884b7b0242b`  
		Size: 2.2 GB (2204728802 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e473536e08c92a08f92b05dcf009604fd3f0425171a596a8efeeeb5f69746a24`  
		Last Modified: Wed, 15 Dec 2021 01:54:48 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28a097f1c6da1d1d6045b118791cf5076a7360b91373bae76209dbfa4609e661`  
		Last Modified: Wed, 15 Dec 2021 01:54:48 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32ba63b1b2e53158cc5902f8107d4421a8a12f929e4c67242ce3fa2cbc0553a`  
		Last Modified: Wed, 15 Dec 2021 01:54:46 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80515b90b11c42a574f7c31fcadd4d31668f93066540f17e3b0905fe12eacb59`  
		Last Modified: Wed, 15 Dec 2021 01:54:45 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002818a5b378a085c7e0c0f95258fb97a557afe6e00e35912ce0902965cd52d8`  
		Last Modified: Wed, 15 Dec 2021 01:54:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6826b991d808a789450cae893bca8fe52c185ba68567aa7c9ec3246d8b657b0`  
		Last Modified: Wed, 15 Dec 2021 01:54:51 GMT  
		Size: 25.4 MB (25419377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd193319409f137bee128603a046e69ee6159b35485612b9e65f81b4ecf814e6`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915b9557c339e8e1394558abd44be62c971aa5b7a6294be429b85d48fdf24bfe`  
		Last Modified: Wed, 15 Dec 2021 01:54:42 GMT  
		Size: 327.7 KB (327679 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d59d0085a49b20c89b965a3123994487d2e7783745047826b6d634ec132a3b`  
		Last Modified: Wed, 15 Dec 2021 01:58:48 GMT  
		Size: 1.4 KB (1444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e325c3f626db4247c9a89671cc5c32e99fe3ddb747cef2ff9412048b364ea9ef`  
		Last Modified: Wed, 15 Dec 2021 01:59:22 GMT  
		Size: 149.9 MB (149887140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82982f6520d1d8a9a9c8dd886a740c4aca31cb91ff724690626f63744c02042d`  
		Last Modified: Wed, 15 Dec 2021 01:58:48 GMT  
		Size: 1.5 KB (1537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
