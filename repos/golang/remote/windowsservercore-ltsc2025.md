## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:e59639664ed890d3425c167fad03c1ee05ae018191e07decd69661ddb8f1801e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull golang@sha256:45e5adf90ef8bee8e13270d1f87509629272694de62cc5cb1b9ae066a4fe4731
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3334473725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe08f944b97ae9ef521700a47c34713f37d21a8d9009f647ac6be4bf2f1cbc08`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:13:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:23:23 GMT
ENV GIT_VERSION=2.48.1
# Fri, 24 Oct 2025 18:23:23 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Fri, 24 Oct 2025 18:23:24 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Fri, 24 Oct 2025 18:23:24 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Fri, 24 Oct 2025 18:23:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:23:41 GMT
ENV GOPATH=C:\go
# Fri, 24 Oct 2025 18:23:46 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:23:47 GMT
ENV GOLANG_VERSION=1.25.3
# Fri, 24 Oct 2025 18:25:13 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:25:14 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:538fa5a72d17bbf02682b93a31bb1c51e26fa76d63e779418172290659f96331`  
		Last Modified: Fri, 24 Oct 2025 18:23:16 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdeb1426db55d5915d70c5dc425b17c2844bbfaee9578bc5221f81be140cb45d`  
		Last Modified: Fri, 24 Oct 2025 18:25:42 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41143ff24779c8c52aa4fbbf888de370e000c7b8d4625dda216b8c14f5c130c6`  
		Last Modified: Fri, 24 Oct 2025 18:25:42 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c3e1a3aead6bdd142767ffbfc0c6b546535f5e76a67519b92f6b13628d2f2f`  
		Last Modified: Fri, 24 Oct 2025 18:25:42 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fc15994dcb915dc5df1b8e7da50c5dd22ae02c9f12a25a5e03045c2ba15e77`  
		Last Modified: Fri, 24 Oct 2025 18:25:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cba27f26dc064789cb3c388d000fa6ec653793a62e2d8a104b3e84e5931c781`  
		Last Modified: Fri, 24 Oct 2025 18:25:47 GMT  
		Size: 51.2 MB (51217266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb2ee786aa82c15bbfae177aa8cbd1714a5274f3109b36916e164daef4e668a7`  
		Last Modified: Fri, 24 Oct 2025 18:25:42 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1eb074a82e87136177ab084a04219fee348c95cbcf258cd5949157c45007695`  
		Last Modified: Fri, 24 Oct 2025 18:25:42 GMT  
		Size: 338.5 KB (338530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fda5fb3fa918e76fa8f0fa9cea9d8de3b0ea3857c2ee743a034637cb5b1a5ded`  
		Last Modified: Fri, 24 Oct 2025 18:25:43 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a5e1cd742d321fbd01430b6f51dbd2835aaec9d36dce7b304e6558195ed14c`  
		Last Modified: Fri, 24 Oct 2025 18:25:51 GMT  
		Size: 62.6 MB (62560279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0373394fdd6c1d9cbdbcff21186fc8e49222a1414a38916cda5cdb2c518c898b`  
		Last Modified: Fri, 24 Oct 2025 18:25:42 GMT  
		Size: 1.5 KB (1467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
