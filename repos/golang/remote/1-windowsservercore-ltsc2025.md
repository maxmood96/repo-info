## `golang:1-windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:76e7fcda2678d876a542a9dacf992a156d412143cc5e24fe20d768d2671b268b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6899; amd64

### `golang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.6899; amd64

```console
$ docker pull golang@sha256:2cc70ddf34ed2361d546e51c2cd1a667733b0158b92468f6b91759817502cdb9
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3334616550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a4325f9378dfd37ef819c354e1df7043dbf0a60840ec650c42b8aa6a22f7d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:52:04 GMT
ENV GIT_VERSION=2.48.1
# Tue, 14 Oct 2025 20:52:04 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Tue, 14 Oct 2025 20:52:05 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Tue, 14 Oct 2025 20:52:06 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Tue, 14 Oct 2025 20:52:21 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:52:22 GMT
ENV GOPATH=C:\go
# Tue, 14 Oct 2025 20:52:27 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 14 Oct 2025 20:52:27 GMT
ENV GOLANG_VERSION=1.25.3
# Tue, 14 Oct 2025 20:53:40 GMT
RUN $url = 'https://dl.google.com/go/go1.25.3.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'bc249a599c6fe9d0d4093c363856f6c6320dbbe05e5d5d8818b711fb4a14fc23'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 14 Oct 2025 20:53:41 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b31ef2acd9573fa311450133976eaea07e0ccfd74f3de24d672c7bf465eba24`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fdfe8df00e8f65fe05a8dcec1a9c9bcf157c585b485a2340afa46effb3085b`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac8a0f1afc6455ae3e0664ae53a39e9bd14cb6a5c24f30dac042aadaba2c68e`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:641c16ab7c76d00518e5cc280a143ac590175746d5286f778f18384e14808fd4`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccb7dc60695c767c62fcb8c95fe9f65ab74aa094069e1022f44b558d9087d1fe`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448bbef62076939cd63e6f8d49609b8fb2adc5beb02d651aba41b27b5702f96a`  
		Last Modified: Tue, 14 Oct 2025 20:54:12 GMT  
		Size: 51.2 MB (51215295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5381a3a340e7179938beb724daee446199efa60f6e2cfc31e2d0e932f20778d`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde940859bdd8f52eb029aaf1674f8befbf5a6e712052af1f487c267fe2cf267`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 343.8 KB (343824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ee53223a19ebc6db910b4cf71152ac4afb2dc0c40dec04a2a4ea6163d91e57`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d18c4ba82afefefaa36e2c54c74d9af40f5daffa1b867c5db38409718e2062`  
		Last Modified: Tue, 14 Oct 2025 20:54:13 GMT  
		Size: 62.6 MB (62566357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7d1daea032d064b1593edc0e230f0d136629eb5b98e4814a5cf121e139cb48d`  
		Last Modified: Tue, 14 Oct 2025 20:54:08 GMT  
		Size: 1.5 KB (1474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
