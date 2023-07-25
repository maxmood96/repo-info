## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6446b2f91d9e216ea9430abc2619ab0abfb508c8a2fd55be5d52441b0a04eabc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1850; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.1850; amd64

```console
$ docker pull docker@sha256:f036505370e71fe6013e09eae58982bf19d779f261af758f03c3e0ca6e959fb6
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1791668357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53ea0a0809793c899cf1e9cb3de891686b773872e92353ab6872f21093da2aa`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Jul 2023 00:27:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 24 Jul 2023 22:15:13 GMT
ENV DOCKER_VERSION=24.0.5
# Mon, 24 Jul 2023 22:15:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.5.zip
# Mon, 24 Jul 2023 22:15:44 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 24 Jul 2023 22:15:45 GMT
ENV DOCKER_BUILDX_VERSION=0.11.2
# Mon, 24 Jul 2023 22:15:46 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.11.2/buildx-v0.11.2.windows-amd64.exe
# Mon, 24 Jul 2023 22:15:47 GMT
ENV DOCKER_BUILDX_SHA256=d9419c0838c8a08c2da28fcee585f48926c4dd64e5be1d96eb55da12fa3332d9
# Mon, 24 Jul 2023 22:16:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 24 Jul 2023 22:16:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.20.2
# Mon, 24 Jul 2023 22:16:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-windows-x86_64.exe
# Mon, 24 Jul 2023 22:16:20 GMT
ENV DOCKER_COMPOSE_SHA256=d381f0697ce5d469917ab343dd4e59ae404865af8a5cf43178005bf400f0113a
# Mon, 24 Jul 2023 22:16:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084e9081d64b30fd475f9121be79bf5756df76494ba98c3208a0e6c46228f7f6`  
		Last Modified: Fri, 14 Jul 2023 00:39:18 GMT  
		Size: 463.2 KB (463247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901deda7922d35795e3d4991c73cb1cab61c3b129a15bb04b3e7d123d0de0b60`  
		Last Modified: Mon, 24 Jul 2023 22:21:33 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d027eea06d0080daedf5ef523c93e969ec807b2a65dcd1021840f7e70db9f2a2`  
		Last Modified: Mon, 24 Jul 2023 22:21:33 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:486b855c5d89d784c7e85907326d05d26635441a754e9e426498138dc6fdd419`  
		Last Modified: Mon, 24 Jul 2023 22:21:36 GMT  
		Size: 17.5 MB (17465980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8dc0f5529504e867302acf706f596cbbe06f751ce571b8bbfd746e8b44b35db`  
		Last Modified: Mon, 24 Jul 2023 22:21:31 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56660e6caa6afda40f70e06ad0adb7679ddd6362b112bf884959a9daa03f43ff`  
		Last Modified: Mon, 24 Jul 2023 22:21:31 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60da8ddac8b835e0b3f3ca4464213330eb286a31ea01b6d75b4f6353e2511083`  
		Last Modified: Mon, 24 Jul 2023 22:21:31 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfc4f9f340fe4664aa4293c04caf8451644aa2f34e790ed08c60628376b6dc39`  
		Last Modified: Mon, 24 Jul 2023 22:21:34 GMT  
		Size: 17.9 MB (17902937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8577eb74030f9da73f6f4a8dfc61abfe3a516bc71c0cdaf04aa41aaa5dfea7f`  
		Last Modified: Mon, 24 Jul 2023 22:21:29 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2ae56b025d396a3597cfb2e9efa8779218d8b955a42b2d8dac86568f88eac8`  
		Last Modified: Mon, 24 Jul 2023 22:21:29 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4b75aa8a819fda1544fe1e0e3befc8d1863729ec8df3d31f37b4e8c7608d9e`  
		Last Modified: Mon, 24 Jul 2023 22:21:29 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:966a418a3938e0554b46c43cacefdbe319c43861b807d6ac33e85e49c1c98d38`  
		Last Modified: Mon, 24 Jul 2023 22:21:34 GMT  
		Size: 18.5 MB (18458205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
