## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:f0a48481ecd899de08fee5d6666ea4f66cafe0f0c9202ffecd46ac59fe094436
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull golang@sha256:3824ddc96d961ebd52d5f6d7e07454c55c4d6045901b0dffe7dc8b3ede2f2a1d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2355657935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d72cd41a993ef9e2e8a27f46c779e436863c960203de3b83abc05ba2dede21c1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Tue, 03 Dec 2024 22:28:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Dec 2024 22:28:37 GMT
ENV GIT_VERSION=2.23.0
# Tue, 03 Dec 2024 22:28:37 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 03 Dec 2024 22:28:38 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 03 Dec 2024 22:28:38 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 03 Dec 2024 22:29:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 03 Dec 2024 22:29:29 GMT
ENV GOPATH=C:\go
# Tue, 03 Dec 2024 22:29:35 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 03 Dec 2024 22:29:36 GMT
ENV GOLANG_VERSION=1.23.4
# Tue, 03 Dec 2024 22:31:38 GMT
RUN $url = 'https://dl.google.com/go/go1.23.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '16c59ac9196b63afb872ce9b47f945b9821a3e1542ec125f16f6085a1c0f3c39'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 03 Dec 2024 22:31:40 GMT
WORKDIR C:\go
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
	-	`sha256:a004c1c7b02f231398b7cb286a6ff3cbedd49189f345ae809826001984c37d72`  
		Last Modified: Tue, 03 Dec 2024 22:31:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0147de9a0b674c4c9a244229bac83b72a43a4f99c51a0fcc3d1f666ed62c84f1`  
		Last Modified: Tue, 03 Dec 2024 22:31:47 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4c8ee2b20c4745393324fc220e06421a9b68276c73ac90e98b140e7767588a`  
		Last Modified: Tue, 03 Dec 2024 22:31:46 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e37921f9e80c8e335cc7289b02cc23ab4febaa860edce6170a6befb918bc6`  
		Last Modified: Tue, 03 Dec 2024 22:31:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f571300417b720b7b673799ff065ae24f6bc277256eaf7eb00dce5d518032170`  
		Last Modified: Tue, 03 Dec 2024 22:31:45 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69ff2e8c80a01d525f247ce24ecf51d531c4278b5fbcc3e687f4acd98d23fcb8`  
		Last Modified: Tue, 03 Dec 2024 22:31:48 GMT  
		Size: 25.4 MB (25448187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12487b8df01b8504922314879551c2bebf069fbd4366768793be1fd151e8abe4`  
		Last Modified: Tue, 03 Dec 2024 22:31:44 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c3ca413c7ffcb9db2345a1b6de07845e2d0a1f21bb54b996e410796944d0103`  
		Last Modified: Tue, 03 Dec 2024 22:31:44 GMT  
		Size: 349.2 KB (349238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43415261ffb5969840fbb05dee76cb8c25db8b3521db62818ef99f9a6daa794e`  
		Last Modified: Tue, 03 Dec 2024 22:31:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4eab5b85293accfc334e102dfa8468a6f0e5e6016ecb621747e35f296a91b3`  
		Last Modified: Tue, 03 Dec 2024 22:31:55 GMT  
		Size: 77.4 MB (77365842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69768a53f9f1d5424e0e81a07bd8a2fc942a3375df65e28f9b446f41ae37a77c`  
		Last Modified: Tue, 03 Dec 2024 22:31:44 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
