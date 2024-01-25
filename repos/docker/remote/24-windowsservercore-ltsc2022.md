## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d2b46a315d3da8b66e7b00b9a9616ec77072da0c2149d1b2d4359ccf44173003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:e86be3683f9047c0cee22c5801da87063833c73cc81a1cf753e67b6023f0bd13
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955280236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4080a77c6e474317ba67106093078e0fd4bd0f5fa964377ce60e09408562635`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Wed, 24 Jan 2024 20:49:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jan 2024 20:49:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 Jan 2024 20:49:54 GMT
ENV DOCKER_VERSION=24.0.7
# Wed, 24 Jan 2024 20:49:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Wed, 24 Jan 2024 20:50:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 24 Jan 2024 20:50:05 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Wed, 24 Jan 2024 20:50:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Wed, 24 Jan 2024 20:50:06 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Wed, 24 Jan 2024 20:50:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 24 Jan 2024 20:50:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Wed, 24 Jan 2024 20:50:15 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-windows-x86_64.exe
# Wed, 24 Jan 2024 20:50:15 GMT
ENV DOCKER_COMPOSE_SHA256=107586a56c0efb53cdd164f8de2c06d9737f4e142c80b6d7d9f5aa2be956425e
# Wed, 24 Jan 2024 20:50:24 GMT
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
	-	`sha256:015a62fe186fdc1d10c4b64ea9d60f50901da8f345e3335557c96f8467065fec`  
		Last Modified: Wed, 24 Jan 2024 20:50:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb983d377f6c9dfbc9d5e96af9eed89ed8b8828e046d9d1d38df48eba541f5f`  
		Last Modified: Wed, 24 Jan 2024 20:50:33 GMT  
		Size: 490.1 KB (490143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1b520f1b82300199f0db1c2e2987c9d97db75b964cc678a82bf55d94139979`  
		Last Modified: Wed, 24 Jan 2024 20:50:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad65f58a123b2bd0a459dab7693ae6429420a61db5cc8f2f0dea7f1fef49c2e8`  
		Last Modified: Wed, 24 Jan 2024 20:50:32 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf29455b990fcbf622128c7abe088132662502600e677a093aea6355bf53889e`  
		Last Modified: Wed, 24 Jan 2024 20:50:33 GMT  
		Size: 17.5 MB (17522830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fb48594f2e75e68028dd3894a529c6179fa0df584cdfb735247967cf30ba638`  
		Last Modified: Wed, 24 Jan 2024 20:50:30 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69732cfa0413c9913d5e3b16d42f50f8bccbd6758aefb1576047a1b8c7759192`  
		Last Modified: Wed, 24 Jan 2024 20:50:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755eb87acaa8487211e425b2e1b8877d4432bb653448d535cf78688ab9567780`  
		Last Modified: Wed, 24 Jan 2024 20:50:29 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eb5960d2df0443fe5ddedf8820fa623be337630d2e3dcd7da815ab86a2961a6`  
		Last Modified: Wed, 24 Jan 2024 20:50:30 GMT  
		Size: 18.0 MB (18015309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d32fa531a9a1699e81167623fba0d00a389e547cec1acd84e30bdf47b642efc7`  
		Last Modified: Wed, 24 Jan 2024 20:50:27 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80723502ec9aa4a57b50e68ffc5ea5e1506ccb4345fe3e709c4bd5457925ea56`  
		Last Modified: Wed, 24 Jan 2024 20:50:27 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:690ee7e0dc9363532c821e7630c58a4712c500cbe8c3be1e56e7347f2c66fca1`  
		Last Modified: Wed, 24 Jan 2024 20:50:28 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91b530b3e28bf96e5f9f2d3126caaacee547fdd07e2c51fa4d593bb7632b0a17`  
		Last Modified: Wed, 24 Jan 2024 20:50:30 GMT  
		Size: 19.0 MB (19027664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
