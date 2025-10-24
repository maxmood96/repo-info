## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:6a649152eee64af88311da781bf666160d3776f68e558ffd610ea3af86fcce40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull docker@sha256:32fa63da127d19b70c2db9377698e4736dbcd7eafc4f7be6c209167bb1a28e7b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3287131753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7af06daf6c3f2fc3d4c8d14bf3db89cd87e77d202e258b8df464e0d270647e8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 24 Oct 2025 18:12:27 GMT
ENV DOCKER_VERSION=28.5.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.5.1.zip
# Fri, 24 Oct 2025 18:12:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:12:40 GMT
ENV DOCKER_BUILDX_VERSION=0.29.1
# Fri, 24 Oct 2025 18:12:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.29.1/buildx-v0.29.1.windows-amd64.exe
# Fri, 24 Oct 2025 18:12:41 GMT
ENV DOCKER_BUILDX_SHA256=3522d12875b71093a210fdc717c9b4be915d1617d41dd347e6dc3e7f2b99d784
# Fri, 24 Oct 2025 18:12:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 24 Oct 2025 18:12:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.40.0
# Fri, 24 Oct 2025 18:12:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.40.0/docker-compose-windows-x86_64.exe
# Fri, 24 Oct 2025 18:12:54 GMT
ENV DOCKER_COMPOSE_SHA256=835b6a7150d12e128fa9fd902abff6212ff3e55398683d57e213956558ead5df
# Fri, 24 Oct 2025 18:13:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5671b9b9319b80bc4a875153412928ecb5a5ecafe14f3becfb08c54de7c6c3b`  
		Last Modified: Fri, 24 Oct 2025 19:07:14 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e06252fd19ee5ca80d670626d56cdddd9d520afdc3bce2b9f26ee84bffc672`  
		Last Modified: Fri, 24 Oct 2025 19:23:45 GMT  
		Size: 341.8 KB (341820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28ffb87042511de2c04035624fa445b225e5e5e7013f9328687fe50c9a5af789`  
		Last Modified: Fri, 24 Oct 2025 19:23:53 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f45841cde28bd14bf63237aceac2b095667aeb9d36cc0569ff77858ca0150f7a`  
		Last Modified: Fri, 24 Oct 2025 19:23:56 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b93844afd54a72f37fad84b1e37dc59d5dcd714eb4535a9e71cc67638ab99e40`  
		Last Modified: Fri, 24 Oct 2025 20:07:33 GMT  
		Size: 20.8 MB (20755797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:409f42fb765462eb6a09eb0e5b253de4934f168db9f1c1e49d288a6b532f687a`  
		Last Modified: Fri, 24 Oct 2025 19:24:00 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58c7dc8f79f8107c04d26948725f3689f7602b5c96cefa94fb000e68e7c9824d`  
		Last Modified: Fri, 24 Oct 2025 19:24:04 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2653a1be445da554ec51cff58c55ece2513e87a21049261ad91fbb5b31824c9b`  
		Last Modified: Fri, 24 Oct 2025 19:24:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80a92afd1d14ec753750ac6feaf15ce0742a34feae4c07bc4ea2d71d048236c1`  
		Last Modified: Fri, 24 Oct 2025 20:07:32 GMT  
		Size: 23.1 MB (23138133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3382aae313087835ed1808628ef1865cbaa017af30e097c2110a58a32d709867`  
		Last Modified: Fri, 24 Oct 2025 19:24:12 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15035be2006083de469f546ade7c727ca553c411c44466893e05d0d6e39b667d`  
		Last Modified: Fri, 24 Oct 2025 18:23:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf8232186e63d984e531280adc51f5e39233062ae81f477782ada8a31c24f0d1`  
		Last Modified: Fri, 24 Oct 2025 18:23:17 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:835a1ec3edf23bddc21e1084a3d6feb07a789de3459e48d981ff4830583f5008`  
		Last Modified: Fri, 24 Oct 2025 18:23:20 GMT  
		Size: 22.5 MB (22537258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
