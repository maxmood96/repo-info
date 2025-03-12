## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:bae7f0717a7d69a1ae6dc5f927bfd1877b8c1f483c3b24ced6762a5cd23feedc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3328; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3328; amd64

```console
$ docker pull golang@sha256:c847736731967ee8e051a7bc2cf3d8b13fdd23eed1c70b586bbabc824cd81db0
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2377983311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45d4afbff0ffc05f61fbe75d1c97791412ccd2e2bdefb8a13db5fdc3c1320b65`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 18:58:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:58:21 GMT
ENV GIT_VERSION=2.23.0
# Wed, 12 Mar 2025 18:58:22 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Wed, 12 Mar 2025 18:58:23 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Wed, 12 Mar 2025 18:58:24 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Wed, 12 Mar 2025 18:58:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 18:58:44 GMT
ENV GOPATH=C:\go
# Wed, 12 Mar 2025 18:58:50 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Mar 2025 18:58:51 GMT
ENV GOLANG_VERSION=1.24.1
# Wed, 12 Mar 2025 19:00:06 GMT
RUN $url = 'https://dl.google.com/go/go1.24.1.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '95666b551453209a2b8869d29d177285ff9573af10f085d961d7ae5440f645ce'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 12 Mar 2025 19:00:07 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a0222c54466eba1f4e3d496e36783256236bd0ba955a32c276a73a4bae55f12`  
		Last Modified: Wed, 12 Mar 2025 19:00:12 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f738ddcdcec11675cc605e97e290d6ed3979b24bd1fb9352dde6d0a38cbb3ca2`  
		Last Modified: Wed, 12 Mar 2025 19:00:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b30289162cc502f3b8350922e87e11a1b7fcdd790322944e5102c95863647e6`  
		Last Modified: Wed, 12 Mar 2025 19:00:12 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3983bb13f5c55fad4162065c0cccc3bf0f820833f733a227c0c48c7afd6047ed`  
		Last Modified: Wed, 12 Mar 2025 19:00:11 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0568ff5e141ced7a0538999dfac7e41b9c6d2a3fcb56d830b2acd80029b5f0df`  
		Last Modified: Wed, 12 Mar 2025 19:00:11 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d657a01997f502c936716f3f4ad383ccacb0eda654e8a8bd10faa92258b6fd37`  
		Last Modified: Wed, 12 Mar 2025 19:00:14 GMT  
		Size: 25.4 MB (25448241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a75c5e2b6be49b9ef8839eca90fd8569834e623c7ded2547fc602d8d383969a`  
		Last Modified: Wed, 12 Mar 2025 19:00:10 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf801a35bf93956ec6fa41e89e585b65797e6693c9dccf11bf8f98743ea1b7c`  
		Last Modified: Wed, 12 Mar 2025 19:00:10 GMT  
		Size: 350.1 KB (350129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e975a5587c4c87fd6cf37487321fa93f4227629a7997f69b26a901f7d3d1ee3a`  
		Last Modified: Wed, 12 Mar 2025 19:00:10 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df605bb6f8373f309bd1a93ae23fa7ad4f2dbc0891110aeb0b4d854feddbbe77`  
		Last Modified: Wed, 12 Mar 2025 19:00:24 GMT  
		Size: 82.2 MB (82233294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6baff3acb60214f13ddd7676a278ee8992e5c6e82adc5b38e6172526b18b05f`  
		Last Modified: Wed, 12 Mar 2025 19:00:10 GMT  
		Size: 1.5 KB (1459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
