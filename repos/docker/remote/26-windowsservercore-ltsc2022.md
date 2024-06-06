## `docker:26-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:335394b4d218b9d69b02260b7919ef7595de36630f6106a78a3a99a6d6c07250
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2461; amd64

### `docker:26-windowsservercore-ltsc2022` - windows version 10.0.20348.2461; amd64

```console
$ docker pull docker@sha256:b787c9789b3e1f229f1a18ecce89f90ed4af18db8d40c34b2e1f26b21df7f329
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2170865718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f7247690dbdd1dad74cfc715193b158738ff09462dff187094caa02e9599eb9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 05 Jun 2024 19:53:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 05 Jun 2024 19:54:51 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 05 Jun 2024 19:54:51 GMT
ENV DOCKER_VERSION=26.1.4
# Wed, 05 Jun 2024 19:54:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.4.zip
# Wed, 05 Jun 2024 19:55:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 05 Jun 2024 19:55:08 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 05 Jun 2024 19:55:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 05 Jun 2024 19:55:10 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 05 Jun 2024 19:55:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 05 Jun 2024 19:55:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 05 Jun 2024 19:55:20 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 05 Jun 2024 19:55:21 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 05 Jun 2024 19:55:29 GMT
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
	-	`sha256:d60926ad275a20f87cd180e251fe27c024cfdccfb4c917f519ce09b5479f200a`  
		Last Modified: Wed, 05 Jun 2024 19:55:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cff0349f472edc1a10481cb19a4cc565387a6dfe2beadcb40854334cbd1d821e`  
		Last Modified: Wed, 05 Jun 2024 19:55:39 GMT  
		Size: 359.8 KB (359830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8127ac9c6dfdd03a922655d18329d7f8a8f86de5ea7c9760284338ab44c6ae0b`  
		Last Modified: Wed, 05 Jun 2024 19:55:38 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66d3ad23e8c14c90a2737ec6b8757aa11e1f4050b21a7b5063cdea1065ec4578`  
		Last Modified: Wed, 05 Jun 2024 19:55:38 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff4d27ae7eb20cfd30e4eae656a52ad032b7b4c1cf1b38254c663567275fa6c`  
		Last Modified: Wed, 05 Jun 2024 19:55:40 GMT  
		Size: 19.3 MB (19253175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f12b2dd07d550959bc3684d0023d09e7bdd5d3eff99775bcfa6445898f9883d`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dc664c296e9f466b7059eec930faec106903f69057da835aa173b69958fc07`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:717c76f39c894f08e4b267de3c93e800fa2f4a95e91c7559b192f79e8887707e`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c475eed2f3ae1a218f11298c10e246ba03cfa5b7756973f0fbb37f98aff7a8d`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 18.9 MB (18931360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26ab9dfed534aac25935e94cffcad9c27f1083d8f2ee3ec46ed0e48c248e2ec6`  
		Last Modified: Wed, 05 Jun 2024 19:55:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb78d95032f41c0991d3325887cff15fdc96dc77faa53032b743a8f08227b06`  
		Last Modified: Wed, 05 Jun 2024 19:55:33 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7bf2312acea1db4b5c8b958af372082aceec3892d4d560bae3f2ec44f5c3f23`  
		Last Modified: Wed, 05 Jun 2024 19:55:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92ea4a144add9f5889379b66d67fe56e1cf88725d22a4f8d67475c9ab656876`  
		Last Modified: Wed, 05 Jun 2024 19:55:36 GMT  
		Size: 19.6 MB (19638389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
