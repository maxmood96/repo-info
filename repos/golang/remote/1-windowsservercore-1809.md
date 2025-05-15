## `golang:1-windowsservercore-1809`

```console
$ docker pull golang@sha256:75b0b08702fd309620edb1f369b9c97f2fc9296520217948d39f0725e2c1ad83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `golang:1-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull golang@sha256:68b622deabed02180f6c985925143b02076942a3d5390e7bae36c037d646eee2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2317822209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79845e1e6db4ba224b3bea4f6a57e4754585372cca319fb3da1a55df8f25f18a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:03:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:03:38 GMT
ENV GIT_VERSION=2.48.1
# Wed, 14 May 2025 21:03:39 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 14 May 2025 21:03:40 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 14 May 2025 21:03:40 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 14 May 2025 21:04:54 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:04:54 GMT
ENV GOPATH=C:\go
# Wed, 14 May 2025 21:05:01 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 May 2025 21:05:02 GMT
ENV GOLANG_VERSION=1.24.3
# Wed, 14 May 2025 21:06:22 GMT
RUN $url = 'https://dl.google.com/go/go1.24.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'be9787cb08998b1860fe3513e48a5fe5b96302d358a321b58e651184fa9638b3'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 14 May 2025 21:06:24 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aae1d10c52ba30ae0aaff0842bd5ac1db29ff2a509262e6a69099ffef2e2eaab`  
		Last Modified: Wed, 14 May 2025 21:06:29 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b906e19596d76f1f62cb29bb4f9a64ea59543b8497da1370d2c120c4099efa`  
		Last Modified: Wed, 14 May 2025 21:06:29 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febee24bc823ff9c3d19fd79b83189fb17947498a9d91be3faa429ffc1a91450`  
		Last Modified: Wed, 14 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa1fa357b5ea0b14d584bf6b59b5a21273c979e15dabf02257450022ffe375f`  
		Last Modified: Wed, 14 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9a8d872e379038e66325ab145e0d0b8227d94799ab335f571f7e494cf673ee`  
		Last Modified: Wed, 14 May 2025 21:06:28 GMT  
		Size: 1.3 KB (1345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90524c93e0925b2e0549b02dc6ce0bcd1ccb51aab2267e4df18429a0129b4559`  
		Last Modified: Wed, 14 May 2025 21:06:34 GMT  
		Size: 51.2 MB (51217705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cb6a608bcad4829dbc30abd0dbbd9e5fba4ad42f70c4ce02a0768dd4392f478`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db51d9d62e3f9acfb7a57782ba95e0059ba66f86370b10b0e0e7c9b97c82bd20`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 337.1 KB (337105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69dd31260ac1011cb4c0dcfa0b3b682f52aaf100fee15c10ce3a8080bca2694`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e08660d7bc8fd0f271002cd3ca8eb1a69546359e3cdbf275c93240f61e5887d`  
		Last Modified: Wed, 14 May 2025 21:06:40 GMT  
		Size: 82.5 MB (82539039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3bc891f58f07d15e00c45bd15fe49ef30f48f716bab1aaf722548d3fb2c07a5`  
		Last Modified: Wed, 14 May 2025 21:06:27 GMT  
		Size: 1.5 KB (1499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
