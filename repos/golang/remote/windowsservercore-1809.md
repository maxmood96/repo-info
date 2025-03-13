## `golang:windowsservercore-1809`

```console
$ docker pull golang@sha256:b9e3ffc728c1fa5fc176d00edc64f2e0facbdc3ac93dbaf26e51f38855071e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `golang:windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull golang@sha256:2940aedd805dfb2c60a71de5cfd7494ee9f27ed2b9bfba6a0ffece0a30129ea9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2285425680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e8284e2aa9c65a7dd983155736b366f64fabe6ce46da64e85904641e9534dbf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Thu, 13 Mar 2025 17:54:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Mar 2025 17:54:58 GMT
ENV GIT_VERSION=2.48.1
# Thu, 13 Mar 2025 17:54:59 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 13 Mar 2025 17:55:00 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 13 Mar 2025 17:55:00 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 13 Mar 2025 17:55:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:55:28 GMT
ENV GOPATH=C:\go
# Thu, 13 Mar 2025 17:55:34 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Mar 2025 17:55:35 GMT
ENV GOLANG_VERSION=1.24.1
# Thu, 13 Mar 2025 17:56:48 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 13 Mar 2025 17:56:49 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81be870f634812fa1f6d6ef69c59c30cc849eb7596a61e1f3f6373a0a383d4ac`  
		Last Modified: Thu, 13 Mar 2025 17:56:57 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a8b22dbc93c5dd5761e377d70a307b01859c72506a434bc7980ec33dd3aa2e`  
		Last Modified: Thu, 13 Mar 2025 17:56:57 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b726286f3b4261c8b41eab22833c2eab62b8539b5d35de8da22ccc3be40d2d`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c64d4aaf2deb795cad856869013cbc6ea6c0ba2e8e476e4334e0acc8853062`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a721b86de1025ca9822807d4bd52272090272764f25dfb8ac69d0eb36d6bba`  
		Last Modified: Thu, 13 Mar 2025 17:56:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755ff4d29b2cfc97e0bd2e86cd87cd9db4f784be84bba2afad44d47e1d586839`  
		Last Modified: Thu, 13 Mar 2025 17:57:02 GMT  
		Size: 51.2 MB (51205680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31b7600c08bff7cb8b879392f339bf34ba620f20b441e46dfa3ab55239124304`  
		Last Modified: Thu, 13 Mar 2025 17:56:53 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d55a8591bfdbf361f4d5d6e9b6d827ba7fd30637673aefa88663f8833d6c1d`  
		Last Modified: Thu, 13 Mar 2025 17:56:54 GMT  
		Size: 345.5 KB (345509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:474e482464a247f4b87adba57ccbb331fc183aa2204a3cff45093cdc076ba360`  
		Last Modified: Thu, 13 Mar 2025 17:56:54 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7729385db686e034d720cf2a1617ed95ae204a798aa1d74e015319a4426eaaf3`  
		Last Modified: Thu, 13 Mar 2025 17:57:07 GMT  
		Size: 82.2 MB (82229348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5350fe0982ad03eb420de2fdf529fceca297915292bd006b4cb4e29d6d84b487`  
		Last Modified: Thu, 13 Mar 2025 17:56:53 GMT  
		Size: 1.4 KB (1443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
