## `docker:26-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:a49ba0bbff228cece7110d8842f5851ac1426f620c5321a5596be9ea99b55b2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2529; amd64

### `docker:26-windowsservercore-ltsc2022` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:93d4f6ee714bc041e81a3a152d1629cc172bdd52c7ec7e67be0c9a55f76c91cc
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2176412954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3808e0ff5d412d9231dcd9f4944b6e513a824d0f576aecdff4f113d457981e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Fri, 21 Jun 2024 23:59:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jun 2024 23:59:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jun 2024 23:59:52 GMT
ENV DOCKER_VERSION=26.1.4
# Fri, 21 Jun 2024 23:59:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Sat, 22 Jun 2024 00:00:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:00:02 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Sat, 22 Jun 2024 00:00:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Sat, 22 Jun 2024 00:00:04 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Sat, 22 Jun 2024 00:00:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:00:13 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Sat, 22 Jun 2024 00:00:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-windows-x86_64.exe
# Sat, 22 Jun 2024 00:00:15 GMT
ENV DOCKER_COMPOSE_SHA256=b9878421deeff63bb4685a0ee502fc737429123f68ee40de326cdc9fab800c1d
# Sat, 22 Jun 2024 00:00:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61bbdfe042899c7f6c93ec2d3483cbd96363efce3661e9545ad6d3361ad54187`  
		Last Modified: Sat, 22 Jun 2024 00:00:34 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf3cbd0290dee0dd8860092d5c8fb754fdb58b587dd7d70a521bed02902348f2`  
		Last Modified: Sat, 22 Jun 2024 00:00:34 GMT  
		Size: 344.2 KB (344236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefeee2bdca7bfa022d621844a2a5fddd6cfbafd8687caa33eb6338db082436d`  
		Last Modified: Sat, 22 Jun 2024 00:00:34 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce695969df237d05a5c7b49fd57b9c9c5d5fa98d0bdc0f71f71d87dca636b012`  
		Last Modified: Sat, 22 Jun 2024 00:00:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a71812bcd266c5745d780df282f7aa6f11e5eefbd9a47dd96910fa7dee42b1`  
		Last Modified: Sat, 22 Jun 2024 00:00:35 GMT  
		Size: 19.2 MB (19239768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc1d138cc9292c8f9d6fdd8e9629527fcbdd06686a6903494cb5e4e95705602`  
		Last Modified: Sat, 22 Jun 2024 00:00:31 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50cca3f92cfbcdc809c9286fdf4d3388f489cc849715781197fd93c3be05cd6`  
		Last Modified: Sat, 22 Jun 2024 00:00:31 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:becd8967d9d4d3f6ec072469541053968b7a50029bfd384a740e748250e06799`  
		Last Modified: Sat, 22 Jun 2024 00:00:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7355eae8b97db02efb6e09b22781fb263f7f2b3fa8d874d3c3e314ba2ef493e5`  
		Last Modified: Sat, 22 Jun 2024 00:00:31 GMT  
		Size: 19.0 MB (19009504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed50262b54502eab8392c2b949f7c5e8fc3166ae2a46ced6db4599db0f1214ca`  
		Last Modified: Sat, 22 Jun 2024 00:00:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f74d1c298a951130f279b961d0495163182a7f69621aaa817422c39b6a3f32`  
		Last Modified: Sat, 22 Jun 2024 00:00:28 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06489cbea03577ad19f1eac4ee7c46474fbd4758421bdba72f83dc7c3304ee49`  
		Last Modified: Sat, 22 Jun 2024 00:00:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:096d9f1f13dede094b607a7b467aeb4726340e7eff94d8311c131619edb6d1bc`  
		Last Modified: Sat, 22 Jun 2024 00:00:31 GMT  
		Size: 19.6 MB (19617598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
