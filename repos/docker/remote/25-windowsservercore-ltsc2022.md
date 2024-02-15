## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:8f59deca1cc30739c35319ae64a1f8d18d0e73fbd26d94fbbb8e21a297443bd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:a030b8f58bd35531589b365afdbc30894465e64d57b47d25c3e85b8116902e0a
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1966357115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4e058ea18abe89fc05682fb6a07e2aee29e954e883e0eed99deff8b7b29ae4`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Wed, 14 Feb 2024 20:03:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Feb 2024 20:03:38 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 14 Feb 2024 20:03:39 GMT
ENV DOCKER_VERSION=25.0.3
# Wed, 14 Feb 2024 20:03:40 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.3.zip
# Wed, 14 Feb 2024 20:03:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:03:52 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 14 Feb 2024 20:03:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Wed, 14 Feb 2024 20:03:53 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Wed, 14 Feb 2024 20:04:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 14 Feb 2024 20:04:04 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.5
# Wed, 14 Feb 2024 20:04:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.5/docker-compose-windows-x86_64.exe
# Wed, 14 Feb 2024 20:04:05 GMT
ENV DOCKER_COMPOSE_SHA256=eb60363d21a5c85eff2d2e18a4ed94d84d5016be59471d77d520046fdd888aa9
# Wed, 14 Feb 2024 20:04:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc906b10e8bda5076dd5dbd104d11bec286803a58ca382dfa4e3aca61239b002`  
		Last Modified: Wed, 14 Feb 2024 20:04:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae31b4f4792eac3da5efa1fdd6371c196c29a28b960faed76da098f045e242a`  
		Last Modified: Wed, 14 Feb 2024 20:04:25 GMT  
		Size: 511.5 KB (511500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb394b8f98a8b4ad5c1a3d98cb3431aabd72461d7216f61f50fa8ec02375021`  
		Last Modified: Wed, 14 Feb 2024 20:04:24 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0277ee47dfb72444755af3883e83966f00d215b10b37772fdae0a2fee7a6289c`  
		Last Modified: Wed, 14 Feb 2024 20:04:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21250607601e9d0c187783f9c63427f79be130a95eb66b8525d87163453005de`  
		Last Modified: Wed, 14 Feb 2024 20:04:24 GMT  
		Size: 18.1 MB (18081883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ead08ba5d9ab45399eb8d5bb2735ff3233fcc07ca5ffb741ad628ad88d1e00b`  
		Last Modified: Wed, 14 Feb 2024 20:04:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83aa393f115457be678d81ea376a96a6177a9735c9cab37919146fdc333ad546`  
		Last Modified: Wed, 14 Feb 2024 20:04:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d883565905074a454cea7b7579ba50b001a5aa6af15fc545daf68026588e8a7`  
		Last Modified: Wed, 14 Feb 2024 20:04:20 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0490f2019a82d2eaa41b9202d85531214e42cbe127e4d051d6cd3ea826b5601d`  
		Last Modified: Wed, 14 Feb 2024 20:04:21 GMT  
		Size: 18.0 MB (18034195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c06655ca156b24c4245649689dba5f274c9dee24822ef087fe0f7db054b41f93`  
		Last Modified: Wed, 14 Feb 2024 20:04:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ab8e737858bfe94005107a8a8bbb0ecfa780952df090064efecbbd8bfb9490`  
		Last Modified: Wed, 14 Feb 2024 20:04:18 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e22bbd854a695849fe315aea53761dfe43a239a33ce15359eadfc9359d0b35e`  
		Last Modified: Wed, 14 Feb 2024 20:04:18 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:508274c6cc05242321eaeeef9a6be28f79642d7eed8036c4541e1721850f5ecb`  
		Last Modified: Wed, 14 Feb 2024 20:04:21 GMT  
		Size: 19.1 MB (19063762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
