## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c977e92d43f75641f9329cba4e250b276cc8692f7c87b45e1d52e2966e8afe40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2527; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2527; amd64

```console
$ docker pull docker@sha256:3a74728d72e51d3355068209ff7376ea1d9b4519dc5a9ea79bc34547104db7a0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2175235636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae54479d3ed190109cbe8ce5744fafa385ffb2a1eb3f13b7391f7aee539af987`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jun 2024 09:02:12 GMT
RUN Install update 10.0.20348.2527
# Wed, 12 Jun 2024 18:06:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jun 2024 18:07:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 12 Jun 2024 18:07:03 GMT
ENV DOCKER_VERSION=25.0.5
# Wed, 12 Jun 2024 18:07:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Wed, 12 Jun 2024 18:07:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:07:17 GMT
ENV DOCKER_BUILDX_VERSION=0.15.0
# Wed, 12 Jun 2024 18:07:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.0/buildx-v0.15.0.windows-amd64.exe
# Wed, 12 Jun 2024 18:07:18 GMT
ENV DOCKER_BUILDX_SHA256=f9285890c7d0b68ed36a07d4db062bfdc8db2059fa59a812cdbef438cfa3f774
# Wed, 12 Jun 2024 18:07:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 12 Jun 2024 18:07:29 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 12 Jun 2024 18:07:30 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 12 Jun 2024 18:07:30 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 12 Jun 2024 18:07:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cedf08888525e83e4a050655b4ec0d81647e59a69f7007a560df774a656da9bb`  
		Last Modified: Tue, 11 Jun 2024 17:49:21 GMT  
		Size: 729.6 MB (729579921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c74375a14d93005740576dec0825a52a749ae8b25dc50f18b6f6139267c66c`  
		Last Modified: Wed, 12 Jun 2024 18:07:47 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a99adf28a7004fb44632ae228a3c041d1db0e7025398ca2a6e565526cd23a7`  
		Last Modified: Wed, 12 Jun 2024 18:07:46 GMT  
		Size: 345.5 KB (345467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3a3b0e09018a24c6f842fb14ec36223509d58c20bc85c6841f718f29a39fa`  
		Last Modified: Wed, 12 Jun 2024 18:07:45 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a1c3494aeedd0921def6f3637f860ba24cb485c6e26d8a8e8b24709c11bf2e`  
		Last Modified: Wed, 12 Jun 2024 18:07:45 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b72c3d89899b48c22b14183f74a104ea0819a1f7e628e2fe22e5d11f8b486a`  
		Last Modified: Wed, 12 Jun 2024 18:07:47 GMT  
		Size: 18.1 MB (18061351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b631c646e24535479c058399c8a59413cf1dc7c1e602d5f4ce06edc39d1b50a5`  
		Last Modified: Wed, 12 Jun 2024 18:07:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14daae162d6b72272e3dcbb920d7880ea752640f006cd6502a5304800708c12c`  
		Last Modified: Wed, 12 Jun 2024 18:07:43 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c056fdcf0010d2ae2240a22e674adb8bdcc72e763440bc65780fef043ed4582`  
		Last Modified: Wed, 12 Jun 2024 18:07:43 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f471babdb2e0cf4d775c9e475d805153898a53e9cc7acd79312c6b1bb1e72d6`  
		Last Modified: Wed, 12 Jun 2024 18:07:44 GMT  
		Size: 19.0 MB (19012346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29ece12a57cbdb2c1441c760035c08833cbc5c3b42d56a557ffaa38b5bcd8b7`  
		Last Modified: Wed, 12 Jun 2024 18:07:41 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dcf5b0c66d816e651da00e3157ee5af461880a240c8b78c52a54f8d5ab81f99`  
		Last Modified: Wed, 12 Jun 2024 18:07:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2469a58d81971e8d7f717b703ff9e77457db86428df25b821dcb1f98b0856cb`  
		Last Modified: Wed, 12 Jun 2024 18:07:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bacd02b85834e870b5d6f71ded9bd972c0b579fc432f08cd252a50930245814`  
		Last Modified: Wed, 12 Jun 2024 18:07:44 GMT  
		Size: 19.6 MB (19626018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
