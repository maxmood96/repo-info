## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:605a0ffffcafebc8a212b7a9a996243d98f8204756e56e71a80c9c53e8b7ccea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:658bfac5edd306851677ea7c4114d4fd2579059bb4dce4f00fa97b2a4a61500f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1954920184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba32b3aa6dbc9269e0e88799cafe7eff480202bec3a9a76544a5755c7b3a62b8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:03:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 11 Jan 2024 00:03:02 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 11 Jan 2024 00:03:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Thu, 11 Jan 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:03:13 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 11 Jan 2024 00:03:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Thu, 11 Jan 2024 00:03:14 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Thu, 11 Jan 2024 00:03:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 11 Jan 2024 00:03:24 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 11 Jan 2024 00:03:25 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Thu, 11 Jan 2024 00:03:26 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Thu, 11 Jan 2024 00:03:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2937f841f30812e56ab5644ccf9f95dad697ac4c2eec900a12d480c8c3091a94`  
		Last Modified: Thu, 11 Jan 2024 00:03:40 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b9d424a679d6445e4d0aa544ef7ef7257c8850e4a9c625966f312719017a23`  
		Last Modified: Thu, 11 Jan 2024 00:03:39 GMT  
		Size: 478.4 KB (478374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bdbbc3723195c60b5d03ebfc70c62a97152c7c1f73d2c6e774ed022591beefc`  
		Last Modified: Thu, 11 Jan 2024 00:03:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7b2422947457c2da10329cf0da29431cf07e7c6f1185512b90088dcfdc61e8d`  
		Last Modified: Thu, 11 Jan 2024 00:03:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c303d4fce0b77134fac7bc0b4772c8bda62a512823166f472fd2c0aee226d402`  
		Last Modified: Thu, 11 Jan 2024 00:03:39 GMT  
		Size: 17.5 MB (17514647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d943a949e8da4f894434af8a9e26d91432a4696fdceb1cc6171d0533783c175`  
		Last Modified: Thu, 11 Jan 2024 00:03:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58da8836fad3103fa6c0278b1259d16a5aa8d0367e2ccfbade10cae8d52a65f8`  
		Last Modified: Thu, 11 Jan 2024 00:03:37 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4912387384052f8b3fa766a9c36f63d725d7316fd998871bc3f066d69f06f923`  
		Last Modified: Thu, 11 Jan 2024 00:03:37 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10930b66cae5b9d0ffba7d7d252b86a7811696aaa4b96978cefc518e9d619393`  
		Last Modified: Thu, 11 Jan 2024 00:03:38 GMT  
		Size: 18.0 MB (18009393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7afa1a6b052af515f77ffab9bba75813521d3cf27be843ae0cfe978bc503c35`  
		Last Modified: Thu, 11 Jan 2024 00:03:36 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79a231696796d49ed61a1d707f47af94bf85b61888744821d2fa725ee2354312`  
		Last Modified: Thu, 11 Jan 2024 00:03:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e8db9a89e565565927f192bb7ab029c2524babfa581fa6e4690d85ffb9e377`  
		Last Modified: Thu, 11 Jan 2024 00:03:36 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e482163ed55c0fd714f23ebb2b65f6d609371a56677bad0c83ff3cbdc8a0a769`  
		Last Modified: Thu, 11 Jan 2024 00:03:38 GMT  
		Size: 18.7 MB (18693169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
