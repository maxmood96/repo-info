## `golang:windowsservercore-ltsc2025`

```console
$ docker pull golang@sha256:d81cd1b1c43daac7fad4c49b8cbe546329f3f9fc092d9b3ce97a8f08463f4531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `golang:windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull golang@sha256:4efa0a780611576f91e307c96ca977ba80bde21721b7c892053cd977f5cae1b2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2603810951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8042b9d82af0fd70364abf966aefa31ebd3365205eb6bc633ef8ea660975ec4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Tue, 21 Jan 2025 23:31:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Jan 2025 23:31:49 GMT
ENV GIT_VERSION=2.23.0
# Tue, 21 Jan 2025 23:31:50 GMT
ENV GIT_TAG=v2.23.0.windows.1
# Tue, 21 Jan 2025 23:31:51 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.23.0.windows.1/MinGit-2.23.0-64-bit.zip
# Tue, 21 Jan 2025 23:31:51 GMT
ENV GIT_DOWNLOAD_SHA256=8f65208f92c0b4c3ae4c0cf02d4b5f6791d539cd1a07b2df62b7116467724735
# Tue, 21 Jan 2025 23:32:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Tue, 21 Jan 2025 23:32:05 GMT
ENV GOPATH=C:\go
# Tue, 21 Jan 2025 23:32:12 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 21 Jan 2025 23:32:13 GMT
ENV GOLANG_VERSION=1.23.5
# Tue, 21 Jan 2025 23:33:28 GMT
RUN $url = 'https://dl.google.com/go/go1.23.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '96d74945d7daeeb98a7978d0cf099321d7eb821b45f5c510373d545162d39c20'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Tue, 21 Jan 2025 23:33:29 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1666beabb132d31fa4a4e6695e9873e5be5d197d72d469a28f30cba119f1a0b7`  
		Last Modified: Tue, 21 Jan 2025 23:33:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79a152c3cbacf98e5431bd2b6390be6c690c26e744d9498a420dd347baa494a`  
		Last Modified: Tue, 21 Jan 2025 23:33:39 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61ace9e3906c3ab0d5ad18f5ae63af05611da8a241ea71374475ecef41465bf2`  
		Last Modified: Tue, 21 Jan 2025 23:33:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0bb63fd900a6e5f6781cfdd0aef3b0611f32c425332e74a96d99b476d38aff`  
		Last Modified: Tue, 21 Jan 2025 23:33:37 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efc18422f91b16f7cfeba6030b0e6be0e66667117bcbfae7974dd7fab3400fb1`  
		Last Modified: Tue, 21 Jan 2025 23:33:37 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27548d349410da6b72bb5e34d403f55366d183e332982efb8fef0172d462313a`  
		Last Modified: Tue, 21 Jan 2025 23:33:40 GMT  
		Size: 25.5 MB (25519841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99f337d32742ab190360843841e8a3ca85ec41dbddb3774a93350c9ca51a4e4`  
		Last Modified: Tue, 21 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ff95bdbdc498600b638c7f7b5cde2451ef2fba03aa8512d6319aa9bb666458`  
		Last Modified: Tue, 21 Jan 2025 23:33:35 GMT  
		Size: 408.3 KB (408310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8a30dcbfac164c2e3a88f0477d462304f48e3a59bbb0fb6a216774bef99f3f`  
		Last Modified: Tue, 21 Jan 2025 23:33:35 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb0e0b9a3220bca1c14b0cda867af3ce40a665173546da9f74367175f8e602c`  
		Last Modified: Tue, 21 Jan 2025 23:33:47 GMT  
		Size: 77.6 MB (77594616 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31a5128a5413a0d0f57499436f226f29d5ed653479888cd7c9a09dc853d3639c`  
		Last Modified: Tue, 21 Jan 2025 23:33:35 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
