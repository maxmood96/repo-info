## `docker:26-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:2b0be846047834576f17f0cfa860afecc9c842b55213627a19006bd5c650dd88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `docker:26-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull docker@sha256:5661da21b1b7e0621a54a099d4901efcd5cfa7ae8c65bbc976920ef96ebc8015
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056348025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad980b7e1427e763c6c181d5fa66c67bb85e107e376c0648a94ed042df847f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Wed, 10 Apr 2024 00:01:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Apr 2024 00:02:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 10 Apr 2024 00:02:03 GMT
ENV DOCKER_VERSION=26.0.0
# Wed, 10 Apr 2024 00:02:04 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.0.0.zip
# Wed, 10 Apr 2024 00:02:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 00:02:15 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Wed, 10 Apr 2024 00:02:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Wed, 10 Apr 2024 00:02:16 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Wed, 10 Apr 2024 00:02:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 10 Apr 2024 00:02:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Wed, 10 Apr 2024 00:02:25 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Wed, 10 Apr 2024 00:02:26 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Wed, 10 Apr 2024 00:02:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5b5bf09fd9fc1bf5662a3774a437ad157c7cd319d4602d48d0ab604b4e921d`  
		Last Modified: Wed, 10 Apr 2024 00:02:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5eb0ed1f5ee660280a01995260be19c800465b12f75a7fe4a1f4a5a549c519`  
		Last Modified: Wed, 10 Apr 2024 00:02:42 GMT  
		Size: 480.5 KB (480502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd77b6244e27b00bdca3c26c04b78c494bddbd0a14d2bd9cb6f6857ef2f50365`  
		Last Modified: Wed, 10 Apr 2024 00:02:41 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da03a54d83efd5ccba75800bf0f773827344cf04a4d7e2ce3dc2923e6834ccd5`  
		Last Modified: Wed, 10 Apr 2024 00:02:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7b07154c8fae51396f42a9e6f27add87f8802f27bff89ef3cda4ac7b5abc54`  
		Last Modified: Wed, 10 Apr 2024 00:02:43 GMT  
		Size: 18.1 MB (18140556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cec1fb25d11d91824ed6eeb0bbf444f1cad87a00f72859053235263306dcfccf`  
		Last Modified: Wed, 10 Apr 2024 00:02:40 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a30754c42d41c73ea1db8ce20d5ecc2fb19ea729f4a05943543d1da1910a7257`  
		Last Modified: Wed, 10 Apr 2024 00:02:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5782371a895bb6c2b66e0c956aceeb65e74ec797b0a1a9183f94eef90a499d`  
		Last Modified: Wed, 10 Apr 2024 00:02:40 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0481566fc9abe95fd91db3f1ec962d79170bc509605742f9ebb1c93f07ef3a8`  
		Last Modified: Wed, 10 Apr 2024 00:02:41 GMT  
		Size: 18.8 MB (18817862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa4950961828f8c271b7401a72af1a4675cd9b6d8f943224e75e1cbd1dd1f35`  
		Last Modified: Wed, 10 Apr 2024 00:02:39 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d0261d3ff5220d313c39ba0ec1f198b9aacbb9d3835bf5ab6e97752a7527c8`  
		Last Modified: Wed, 10 Apr 2024 00:02:38 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e5c856fd9e1ab16f18da3991148e84c3ca197153b920ac987e174190d29f713`  
		Last Modified: Wed, 10 Apr 2024 00:02:39 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67161697b4593a4be9769fe39955081a35e72e94045cfb4c2bb8957d5f82d96d`  
		Last Modified: Wed, 10 Apr 2024 00:02:41 GMT  
		Size: 19.5 MB (19523638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
