## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:7d7d435576337eed170ed36a4fa20841534c75de821229af0875151110226aa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull docker@sha256:96d43ae4d991ddfa53c9ab8d3da5be764d4ea3c7add0bdc1eebdede609ade246
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338721222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e139aa7d79ea5a31db763229aca954ab4c22dd08f84558a45eceada6d12eb03c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Fri, 23 May 2025 18:59:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 May 2025 18:59:45 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 23 May 2025 18:59:45 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Fri, 23 May 2025 18:59:46 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Fri, 23 May 2025 18:59:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 18:59:56 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Fri, 23 May 2025 18:59:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Fri, 23 May 2025 18:59:57 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Fri, 23 May 2025 19:00:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 23 May 2025 19:00:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.2
# Fri, 23 May 2025 19:00:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.2/docker-compose-windows-x86_64.exe
# Fri, 23 May 2025 19:00:06 GMT
ENV DOCKER_COMPOSE_SHA256=82ebec0022949087f883b3dffa0d7e57a2a141203ad31c012381d2754962c905
# Fri, 23 May 2025 19:00:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78e15449054f393fa0be69bca57f4e37d030e59e0093c42f2ae60f2d70ca111a`  
		Last Modified: Fri, 23 May 2025 19:00:21 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6791f2711b3497f5ff9d281a8db42412a13f4aa4285881dc4ac8fa74af397d28`  
		Last Modified: Fri, 23 May 2025 19:00:22 GMT  
		Size: 356.6 KB (356587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:219cafef75b1d6a6b9c1f7ca38f30c9afa381312521a90442c9996eb9f357bf9`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:193197c4313525e2b4e9b28aca7c4e42f069b7ea4428f0dac55968d1a15adbf0`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640d8f49b99add9a4d820be6aa4f072ac32dd189eb7cdaf4a93a18d692aa4a32`  
		Last Modified: Fri, 23 May 2025 19:00:22 GMT  
		Size: 20.5 MB (20452117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea33b3f215c80e7e531cebba8d66a1849473b85e5d3555bed94e4761fc22e524`  
		Last Modified: Fri, 23 May 2025 19:00:18 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcebc271467f124e68de72ac2407b0912809580b158cad6ee3f8af5f56d5cf8`  
		Last Modified: Fri, 23 May 2025 19:00:18 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c0fedb0f306e9ecc03e3df7711e85e11e72853f3af38261b23411ea49c86925`  
		Last Modified: Fri, 23 May 2025 19:00:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d9f486d4d9cb9136298e740017cf02265c70a2ff79622e69066e220124d687`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 22.3 MB (22261452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2081484829036cf12b2e8f03c9ca478d45a06d3ef055ffe7d4db39a9677f73b4`  
		Last Modified: Fri, 23 May 2025 19:00:17 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8293f261f2933e7722de6ab1967364997211b609cd9cc11da8759d6101ad4ad`  
		Last Modified: Fri, 23 May 2025 19:00:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:603c129d87c2e5edf0eeed364436892c2e0237ce73c3023f1a0b0966f7ac0030`  
		Last Modified: Fri, 23 May 2025 19:00:17 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584775f0f553495fbe9410171084e3bf52f13ad12755a2b281947130912e2134`  
		Last Modified: Fri, 23 May 2025 19:00:20 GMT  
		Size: 22.0 MB (22011394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
