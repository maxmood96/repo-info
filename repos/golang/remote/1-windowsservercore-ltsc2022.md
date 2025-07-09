## `golang:1-windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:6a4a8a88a9cbe9ab4ddf040afc8275ac024f7bda9692bddfc9ff7899641e2743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `golang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull golang@sha256:9efad8d209428fe3503591226d4000347db2332ab55becd385c321cea3ffa8b5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2414523091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd5e336dc6b430ea854467e340f69c9f2f49cfe0135093f6bace08f2970f00a9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 05 Jul 2025 05:31:06 GMT
RUN Install update 10.0.20348.3932
# Wed, 09 Jul 2025 18:07:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:07:09 GMT
ENV GIT_VERSION=2.48.1
# Wed, 09 Jul 2025 18:07:11 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Wed, 09 Jul 2025 18:07:12 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Wed, 09 Jul 2025 18:07:13 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Wed, 09 Jul 2025 18:07:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:07:30 GMT
ENV GOPATH=C:\go
# Wed, 09 Jul 2025 18:07:36 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Jul 2025 18:07:37 GMT
ENV GOLANG_VERSION=1.24.5
# Wed, 09 Jul 2025 18:09:20 GMT
RUN $url = 'https://dl.google.com/go/go1.24.5.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = '658f432689106d4e0a401a2ebb522b1213f497bc8357142fe8def18d79f02957'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Wed, 09 Jul 2025 18:09:22 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b829944a73d1d8ad37eaa13c64bf9189b6895cc5b45b79bb3563fa325d94b6a7`  
		Last Modified: Wed, 09 Jul 2025 00:17:04 GMT  
		Size: 818.4 MB (818411069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb34ef43be114d70bcc50842e3a588e19de16cb9915b8f7759137ed93cf15d35`  
		Last Modified: Wed, 09 Jul 2025 19:08:26 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c72eb82b06c5805b0f79839ace8de982b1aee48233d628810077eca5e394882`  
		Last Modified: Wed, 09 Jul 2025 19:08:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0acb41435d2edb559f603778d4ef837302bac35d66a485a648fc6a10ebfe7f2`  
		Last Modified: Wed, 09 Jul 2025 19:08:27 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e35d82dd2b62167d373b7637ae29fcb6a9956acb840269591f695dba40af00b`  
		Last Modified: Wed, 09 Jul 2025 19:08:27 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0f11fe1282b57c8265f468f954c2e6d94e280920bbdf97e225f736cf426b8`  
		Last Modified: Wed, 09 Jul 2025 19:08:28 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51d9cca5a153aae36fa8b61eb1a61861736d09616644323eb1dde541ec797717`  
		Last Modified: Wed, 09 Jul 2025 19:08:33 GMT  
		Size: 51.2 MB (51209736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b3159133c8183d0f9f5ea8f5afe01656822c2ca4ad9d7c24b96be8838a196a`  
		Last Modified: Wed, 09 Jul 2025 19:08:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:136f870214093721ea447f92091cc1559e9abd2b3a6ce6085cea2a2df6067497`  
		Last Modified: Wed, 09 Jul 2025 19:08:30 GMT  
		Size: 344.6 KB (344588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b0d0e6a6a1527c9f44e1279ec4107fb787e333ed4ed225a667f06a5ad736c67`  
		Last Modified: Wed, 09 Jul 2025 19:08:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26d8bd1ea4678c3bfc2fa9ac289a8bf54ca5a091fbedb2c48520f0c640ce1710`  
		Last Modified: Wed, 09 Jul 2025 19:08:38 GMT  
		Size: 82.4 MB (82354876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c7e755b9ca62ff7c49646eb41043e9f5d7a697d30aebe0695f5234c50cb2d5`  
		Last Modified: Wed, 09 Jul 2025 19:08:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
