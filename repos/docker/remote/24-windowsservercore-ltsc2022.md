## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:e1d41c0560b00ca9357a973d6e357e17ce20a637a0f14e1a9e4f52708b6e53f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull docker@sha256:f64d8cf61eb0861cd27dc9fbb7d68245fb4dbd31be8c97285dd795117623e0a0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169092039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9003bf795b91cc17bb2e644efd7f693777d4e931fd57766b7cd5870401f01e47`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 22 May 2024 22:55:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 May 2024 22:55:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 May 2024 22:55:33 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 22 May 2024 22:55:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 22 May 2024 22:55:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:55:46 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 22:55:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 22 May 2024 22:55:47 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 22 May 2024 22:55:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:55:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 22:55:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Wed, 22 May 2024 22:55:58 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Wed, 22 May 2024 22:56:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b998151686eefb94d03cef13a6bd47c3b829c6cd02b5898c5763ef8172b21aa`  
		Last Modified: Wed, 22 May 2024 22:56:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef5a26f249591f9361e4ab6d1d4dddb9046b17d6dc22caf75d4d3febba4c8c5`  
		Last Modified: Wed, 22 May 2024 22:56:17 GMT  
		Size: 347.7 KB (347745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356d1e858be19b37a07fc5c4410e9b96a6fbde28473e524aaf1deced389b4cda`  
		Last Modified: Wed, 22 May 2024 22:56:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d62238c3dafa754d614d8ffb607289c12b3e20eab9b7192963802c995f45540`  
		Last Modified: Wed, 22 May 2024 22:56:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86ccd96c7882e028c701d251bebc45dd19ed0cbe5a517d12dec3d2696fe85`  
		Last Modified: Wed, 22 May 2024 22:56:17 GMT  
		Size: 17.5 MB (17521247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da0d675278e5a34804290aa783e5dfa3bd632ae71831e90d51992a8db58381`  
		Last Modified: Wed, 22 May 2024 22:56:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2476015d7ba84d414b824b0a3a6c615b0da5a29bb5ee28202061ced5148e4d2b`  
		Last Modified: Wed, 22 May 2024 22:56:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dea17365a061f2cc92f0414bf29dba55707b4bffb15cfa0eed8c31e5a220b1`  
		Last Modified: Wed, 22 May 2024 22:56:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02bbc39042afda5832b8b8f0c22281a0d41c5744eab1bf0df1a92ba76bc16c3`  
		Last Modified: Wed, 22 May 2024 22:56:14 GMT  
		Size: 18.9 MB (18919233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84e30d66a3d1486f44c6b3b00b90cdcd0c8f576b8685c21bf7c2ef2706f6d9b`  
		Last Modified: Wed, 22 May 2024 22:56:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d6cca4f2d86d9766daf7300cfa9dba7b708368a59fb5ddf2c121db3131356a`  
		Last Modified: Wed, 22 May 2024 22:56:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b47e3485cef56a78e0ed73008d079278bc10133c2e1948a47e776ffc452e7a`  
		Last Modified: Wed, 22 May 2024 22:56:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e248e5ed21f036eb826b1e406ed29e4663258af85d2d7a90487fbdbbe615c68`  
		Last Modified: Wed, 22 May 2024 22:56:14 GMT  
		Size: 19.6 MB (19620763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
