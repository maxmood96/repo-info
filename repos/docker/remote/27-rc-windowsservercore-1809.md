## `docker:27-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:f71b0733b694df00e30a2b2b24bc46c0b96e94c9c356bdc871b378198b127542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `docker:27-rc-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:3b72c0748264d6f11c49d3ba8bc695675137a36b7820252d828d43b2f7fffca2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069526287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d110c3e98d52505af939b11f89aee6de032edac50d070b1c397c411da34aa8cb`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Wed, 20 Nov 2024 00:24:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 20 Nov 2024 00:26:08 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 20 Nov 2024 00:26:09 GMT
ENV DOCKER_VERSION=27.4.0-rc.2
# Wed, 20 Nov 2024 00:26:09 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.4.0-rc.2.zip
# Wed, 20 Nov 2024 00:26:30 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 20 Nov 2024 00:26:30 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Wed, 20 Nov 2024 00:26:31 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Wed, 20 Nov 2024 00:26:31 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Wed, 20 Nov 2024 00:26:41 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 20 Nov 2024 00:26:42 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Wed, 20 Nov 2024 00:26:42 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-windows-x86_64.exe
# Wed, 20 Nov 2024 00:26:43 GMT
ENV DOCKER_COMPOSE_SHA256=30be0d2d5df4d032ffeee3f8c5e6dccc2ef1b2911732055778c3584e9e69bb4b
# Wed, 20 Nov 2024 00:26:54 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb82df1ef0f5885d868da450506aff30775ba5421c9d9214833798007b44fd9`  
		Last Modified: Wed, 20 Nov 2024 00:27:03 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41b3d187a6e2a3a55367f4279880fde7e2876752b13210d7344e65d867ffb08`  
		Last Modified: Wed, 20 Nov 2024 00:27:03 GMT  
		Size: 485.8 KB (485753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d122184c7b9a19d5cb2bd24f787c44a3a6b1ff894556d2f004f1ea7c0bd46f`  
		Last Modified: Wed, 20 Nov 2024 00:27:01 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eccd52e83e9f602939bcbb4e468ff02f79ca5d672fbb1f0ab3f421569163c092`  
		Last Modified: Wed, 20 Nov 2024 00:27:01 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce59cc5276ebc6f2f6256e812065a5b5dc3a0f272a2b613160c3f21cb7d4f52f`  
		Last Modified: Wed, 20 Nov 2024 00:27:03 GMT  
		Size: 19.0 MB (18991224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5507e792047a5a3a609853bfacae7f67a4e2b079e549077a6daa8924d830e5`  
		Last Modified: Wed, 20 Nov 2024 00:26:59 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26442f43ec0bd89f3fb1c8acfd14478f7c70d9f34f160acaef68c25c5adde34`  
		Last Modified: Wed, 20 Nov 2024 00:26:59 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8b2b1fc3b34193f2ac546132fc9a34a2aba51973967785f37acb5aa871a1aa1`  
		Last Modified: Wed, 20 Nov 2024 00:26:59 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f09d94db95ea6080ea87eff044bb333a29e2ae9207e1798e0e81c0fd41101e`  
		Last Modified: Wed, 20 Nov 2024 00:27:01 GMT  
		Size: 19.4 MB (19404432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a1ed521dd1dd8608506ffbcd3718c009ef327650959f31da0dee3622d75eef`  
		Last Modified: Wed, 20 Nov 2024 00:26:58 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e0ec01abea87465cd24416536873a290dbdb907b5421db78fcdd189b26a12b`  
		Last Modified: Wed, 20 Nov 2024 00:26:58 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea3a6b842604f95011aad1989d8cc96c6b4d89f48a3908cfcc69e67bf25b880`  
		Last Modified: Wed, 20 Nov 2024 00:26:58 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53a0e267b54cfdaabca9e3361d66b97169b8f9e0f513a80803ba60303c708e54`  
		Last Modified: Wed, 20 Nov 2024 00:27:01 GMT  
		Size: 20.0 MB (19979202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
