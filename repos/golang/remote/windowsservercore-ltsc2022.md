## `golang:windowsservercore-ltsc2022`

```console
$ docker pull golang@sha256:24e95a78a6501430ba841c6932a9f0a3d0d020f59727f9797e8a09f8a6ab859b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `golang:windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull golang@sha256:d63418b9cf7627fc8e93b0db588ac268a66363d1a6d6be59dc884fcdbd8fa5be
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2407426836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9eeb655d8ce27a0b7b924353e44876312efc432ad8a57f1dcd256cce2e30acd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Thu, 05 Jun 2025 19:27:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Jun 2025 19:27:01 GMT
ENV GIT_VERSION=2.48.1
# Thu, 05 Jun 2025 19:27:02 GMT
ENV GIT_TAG=v2.48.1.windows.1
# Thu, 05 Jun 2025 19:27:03 GMT
ENV GIT_DOWNLOAD_URL=https://github.com/git-for-windows/git/releases/download/v2.48.1.windows.1/MinGit-2.48.1-64-bit.zip
# Thu, 05 Jun 2025 19:27:04 GMT
ENV GIT_DOWNLOAD_SHA256=11e8f462726827acccc7ecdad541f2544cbe5506d70fef4fa1ffac7c16288709
# Thu, 05 Jun 2025 19:28:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:GIT_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:GIT_DOWNLOAD_URL -OutFile 'git.zip'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:GIT_DOWNLOAD_SHA256); 	if ((Get-FileHash git.zip -Algorithm sha256).Hash -ne $env:GIT_DOWNLOAD_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive -Path git.zip -DestinationPath C:\git\.; 		Write-Host 'Removing ...'; 	Remove-Item git.zip -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\git\cmd;C:\git\mingw64\bin;C:\git\usr\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("git version") ...'; 	git version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 19:28:32 GMT
ENV GOPATH=C:\go
# Thu, 05 Jun 2025 19:28:39 GMT
RUN $newPath = ('{0}\bin;C:\Program Files\Go\bin;{1}' -f $env:GOPATH, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Jun 2025 19:28:40 GMT
ENV GOLANG_VERSION=1.24.4
# Thu, 05 Jun 2025 19:30:57 GMT
RUN $url = 'https://dl.google.com/go/go1.24.4.windows-amd64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'go.zip'; 		$sha256 = 'b751a1136cb9d8a2e7ebb22c538c4f02c09b98138c7c8bfb78a54a4566c013b1'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash go.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive go.zip -DestinationPath C:\; 		Write-Host 'Moving ...'; 	Move-Item -Path C:\go -Destination 'C:\Program Files\Go'; 		Write-Host 'Removing ...'; 	Remove-Item go.zip -Force; 		Write-Host 'Verifying install ("go version") ...'; 	go version; 		Write-Host 'Complete.';
# Thu, 05 Jun 2025 19:30:58 GMT
WORKDIR C:\go
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Thu, 15 May 2025 19:25:06 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72f4aadbb8b02245006768330af5ea5b31ea0852a8ad30f1a19d88e3a92f5c64`  
		Last Modified: Thu, 05 Jun 2025 19:31:42 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a28e7282133be00a06c24b4362b9fe3204ad1afc7f9e04d958fc63887164fee`  
		Last Modified: Thu, 05 Jun 2025 19:31:44 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:677253b09f334f1855066ca4928950c32fecd2040910ea8ac1cfeeb9ef888033`  
		Last Modified: Thu, 05 Jun 2025 19:31:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bcb461d88cbedd160bbc5a00cdabd05399a3674e938fc4fb43ed3a450ac6f9`  
		Last Modified: Thu, 05 Jun 2025 19:31:44 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0aeebf9fb7661b6e87b595e8c8060f0e765a9c210cb1e3ea58e04414bd36f40e`  
		Last Modified: Thu, 05 Jun 2025 19:31:49 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f14c62b064a5ceb4630a030c3a6feaa7ab3e3e7155a0a6de6797bafcb097242f`  
		Last Modified: Thu, 05 Jun 2025 19:32:14 GMT  
		Size: 51.2 MB (51215597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fec7fb67192f40da3304349c4bfa52a0296ab85c5ae9ec01c1e620cbccb2deef`  
		Last Modified: Thu, 05 Jun 2025 19:31:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4075bf8480cf36e01ecd44235179e1e98b02cbb888964878948f5299ca503ae`  
		Last Modified: Thu, 05 Jun 2025 19:31:51 GMT  
		Size: 314.4 KB (314374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bbc0f653f5598792e249d3fcd6c5ee0899dbeadb882033ac73f22d60323114`  
		Last Modified: Thu, 05 Jun 2025 19:31:52 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c382c912e8acd86f63da560ccef77570ecd60f4d5a8cbf1c37ff4113a9c8049`  
		Last Modified: Thu, 05 Jun 2025 20:00:41 GMT  
		Size: 82.3 MB (82258319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137f56501bc2ff0db6dd54b894d78751f8c8e21083ad5862964e08b4e4107b77`  
		Last Modified: Thu, 05 Jun 2025 19:31:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
