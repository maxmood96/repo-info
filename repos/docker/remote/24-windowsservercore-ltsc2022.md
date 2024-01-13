## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:ef73728187b4717d2d03581f9c78f4f9c8e978c7349ca2eac83890b84a8f3962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:4fbc2286636b60cca286f1b837c953381d69eb2c3bf7c1dfdfbc297e20bddc00
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955323622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ed19a1ab320dc00fecf73435a1ad35cd409f102a599e46429e8047afb4694e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Sat, 13 Jan 2024 02:03:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 02:03:16 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 13 Jan 2024 02:03:16 GMT
ENV DOCKER_VERSION=24.0.7
# Sat, 13 Jan 2024 02:03:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Sat, 13 Jan 2024 02:03:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:03:27 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 02:03:27 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Sat, 13 Jan 2024 02:03:28 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Sat, 13 Jan 2024 02:03:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:03:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 02:03:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-windows-x86_64.exe
# Sat, 13 Jan 2024 02:03:37 GMT
ENV DOCKER_COMPOSE_SHA256=4e0e387d67a65d92e3a7aca085f86b4b46ed5bd7a475f81921629e1d097178f0
# Sat, 13 Jan 2024 02:03:45 GMT
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
	-	`sha256:a764111b60b54df97a515cc896483140125ed65824ca0f6c15bd8427e7d5b776`  
		Last Modified: Sat, 13 Jan 2024 02:03:53 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa697cf34903a3c4bb6208281d67147ee6603d958e419b63dcb766998d9695de`  
		Last Modified: Sat, 13 Jan 2024 02:03:53 GMT  
		Size: 500.9 KB (500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b47a36f27df25156b381723522ea7e9c19bcfda44cbd444845a625c0ca8316a`  
		Last Modified: Sat, 13 Jan 2024 02:03:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653b216a3789bccfce323e88b40276cc1b17ede351d2486d2cabbac3236a2051`  
		Last Modified: Sat, 13 Jan 2024 02:03:52 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027140c8a985639b84e0b70672ce468087907eb31151491199ebd1a811588e15`  
		Last Modified: Sat, 13 Jan 2024 02:03:54 GMT  
		Size: 17.5 MB (17535031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9591428a7051a431ab49840c8ab1569488c2ffd575b244453c1676c21a50da`  
		Last Modified: Sat, 13 Jan 2024 02:03:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af59b8aedc958911d9dbf07cbc862d38f4160b61afcd6ca659ec535b774db88a`  
		Last Modified: Sat, 13 Jan 2024 02:03:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a97540eb00d85e17c41dc43aa23b8b0fbdf2f7471bd5c10d938f0d7b76d12e`  
		Last Modified: Sat, 13 Jan 2024 02:03:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030beca12551c010fce4cd7901b7f4a29875e716ab51e585fd02fb0051f43d8e`  
		Last Modified: Sat, 13 Jan 2024 02:03:51 GMT  
		Size: 18.0 MB (18026958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c04aeed41877f2da7034dbbceac48a995a9d6a39720749157987dffb9198e54`  
		Last Modified: Sat, 13 Jan 2024 02:03:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff057712e5b0758e9cc3c5270e932b18eb0c3a82b0089c19b292200279d7c`  
		Last Modified: Sat, 13 Jan 2024 02:03:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1632d19b5c7da08d6194d0993d09158e67267ef2211e12ca4fa7f5ae6b349332`  
		Last Modified: Sat, 13 Jan 2024 02:03:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c60e9795150504ea946e2f78aeb11ea9a5e411dc39647547e2e9b3f457c486`  
		Last Modified: Sat, 13 Jan 2024 02:03:51 GMT  
		Size: 19.0 MB (19036445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
