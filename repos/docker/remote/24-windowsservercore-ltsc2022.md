## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:0509994e3ef2dbfd83b3772ec09f3a2f208efdff3b295f74554d05f78e6f4e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull docker@sha256:523463374362c87de368f11ecf54561aca024cec3ebaea00266c645fa221f184
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1966593897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d01c8868ba18237db1d6caa88197b8f5dcceb11a0e83582fad305d218c1924b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Fri, 08 Mar 2024 16:55:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 08 Mar 2024 16:56:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 08 Mar 2024 16:56:35 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 08 Mar 2024 16:56:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Fri, 08 Mar 2024 16:56:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:56:52 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Fri, 08 Mar 2024 16:56:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Fri, 08 Mar 2024 16:56:53 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Fri, 08 Mar 2024 16:57:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 08 Mar 2024 16:57:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Fri, 08 Mar 2024 16:57:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Fri, 08 Mar 2024 16:57:03 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Fri, 08 Mar 2024 16:57:11 GMT
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
	-	`sha256:ecc5232d4d7bacbc62c3ad9b07edd7fc05adf50d504acc1e3b1fb7062b5c2d0d`  
		Last Modified: Fri, 08 Mar 2024 16:57:17 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:650864f5ea2c3128729b14ddf3e3e673305dff0b51e1456e4bd3b12f0c11d788`  
		Last Modified: Fri, 08 Mar 2024 16:57:17 GMT  
		Size: 492.0 KB (491991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1335d444d7d224316c5c086b4017f7f7989c11720273d3e78e018b4865d8c6e`  
		Last Modified: Fri, 08 Mar 2024 16:57:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98564a0cde21b9de6d4570781dd149b27d957b72ff09afd1fc439ad807a6b080`  
		Last Modified: Fri, 08 Mar 2024 16:57:16 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24548c6f9687a1a31563928cc9d0e5b2e86e794be0de5f9a5ab872f73aea1350`  
		Last Modified: Fri, 08 Mar 2024 16:57:17 GMT  
		Size: 17.5 MB (17533426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ef416d39ce601f6e1769fa596cab456ff68bf344de030609bb144832c9a383`  
		Last Modified: Fri, 08 Mar 2024 16:57:15 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0d855ddfafbfbd7cdfe38f88fcccc2f459f1a33d1985fbd80e634d956a68847`  
		Last Modified: Fri, 08 Mar 2024 16:57:14 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25d43d857a4acc1bfddf04295940b50b3f1ca79816cbc3305fe9429ed38d961b`  
		Last Modified: Fri, 08 Mar 2024 16:57:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3590b3dbfdd21d46c4167becc2854026bd53d2c55468f4517fb09060459f971`  
		Last Modified: Fri, 08 Mar 2024 16:57:16 GMT  
		Size: 18.8 MB (18828119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171397fdc1bc52ca6988bdcd6635d77fa74c3a9d8878fcc8c167840bad0e9578`  
		Last Modified: Fri, 08 Mar 2024 16:57:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01584f66a613e26438770592eef87844d370e0de989ec85352ebcfb3ba99e09a`  
		Last Modified: Fri, 08 Mar 2024 16:57:13 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3b50a88921971878be409f5b9647ef5b28e3a9efbb23edb584e592e12ba960c`  
		Last Modified: Fri, 08 Mar 2024 16:57:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d250c33be5f8b51b44c325752fa822dadbbb8b3e76ce195cb857a419a294069`  
		Last Modified: Fri, 08 Mar 2024 16:57:16 GMT  
		Size: 19.1 MB (19074579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
