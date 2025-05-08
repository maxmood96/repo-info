## `docker:28-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:4cf54abce2ac2e064aff516baf94c32669e59cfb9dcf407e4f460c9acf8bce7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `docker:28-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:4ccb6c991dd74c258b0a81186edeb90078284bf7868cd6229e64b904feaf302c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459732365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63714859c74e91240eefa337a42c1e598680505bff97dedb00a7f0bc1389aea7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Wed, 07 May 2025 18:32:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 07 May 2025 18:32:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 07 May 2025 18:32:53 GMT
ENV DOCKER_VERSION=28.1.1
# Wed, 07 May 2025 18:32:53 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.1.zip
# Wed, 07 May 2025 18:33:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:33:05 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Wed, 07 May 2025 18:33:06 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Wed, 07 May 2025 18:33:07 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Wed, 07 May 2025 18:33:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 07 May 2025 18:33:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.0
# Wed, 07 May 2025 18:33:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.0/docker-compose-windows-x86_64.exe
# Wed, 07 May 2025 18:33:20 GMT
ENV DOCKER_COMPOSE_SHA256=9916ce82e444bb68e539ab36b947c2edb95f74e5a640c2661255f2c340b5cfee
# Wed, 07 May 2025 18:33:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22921e3ab6c5efd79126d7b585b9662a46f531bea91ab8bbe89589ced76f3ac7`  
		Last Modified: Wed, 07 May 2025 18:33:38 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a7dcb894df5c8b61d49608702a3aa54639715a6579dfcdd38267512627e410`  
		Last Modified: Wed, 07 May 2025 18:33:38 GMT  
		Size: 381.5 KB (381462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:231b6b67c8c492cfe88623eceb316dc412d6c2f2b20129b748c5e1efce4b6a71`  
		Last Modified: Wed, 07 May 2025 18:33:36 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2949e8ccba79103f9c7dc2641e0087ab6ac874547c98d1bc9583d51078eff48b`  
		Last Modified: Wed, 07 May 2025 18:33:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f2e8fa625a918a2559842565dc67a65b26e1b9e889094e98bdbf38d6ebd3c3`  
		Last Modified: Wed, 07 May 2025 18:33:38 GMT  
		Size: 19.9 MB (19916530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaf15783e93b1eee0a7bfaab79219d4072e4ffe1de96dfd182f24321ae576734`  
		Last Modified: Wed, 07 May 2025 18:33:35 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a6b05e54c87d00fbf3780f914b7b18b04acc4b6556aed0e6dc5a6a6c39fe2d`  
		Last Modified: Wed, 07 May 2025 18:33:34 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c24cda0de71389806c3606237a322864557d14666704712020cffa71f4869937`  
		Last Modified: Wed, 07 May 2025 18:33:34 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:229788863bc3cad2edfb77f5bae705ea18d0d2bdcb95d51cf5e00ee4351e6909`  
		Last Modified: Wed, 07 May 2025 18:33:36 GMT  
		Size: 22.4 MB (22379423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682e77b9e62531589283552fb3c08071ce46004ac75bad354cf02576a197a99a`  
		Last Modified: Wed, 07 May 2025 18:33:33 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cabc16bdfe2f2f4086f6a7e264e6484afc6b9d7ca99e7899de33982fcedf3a73`  
		Last Modified: Wed, 07 May 2025 18:33:33 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:267336a44bf64337c1a5943fe87e1a2bc1d704339bc18398428ea65b3aba784e`  
		Last Modified: Wed, 07 May 2025 18:33:33 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132e9db793bc65d39032c50e2140f23833dd94f4f351aff6532915fe1d208ef1`  
		Last Modified: Wed, 07 May 2025 18:33:36 GMT  
		Size: 21.9 MB (21881450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
