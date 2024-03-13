## `docker:26-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6afcaa7a6ec8115a9b635bf8054ae2ce57fc1751fe2fd9cd52b846a3c4d8d6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:26-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:e15561939bbba0ceb996cf95c8ddfd9b76f7adc583f82449d75f3b37662cab66
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013981937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5645dd7dce43b51dde8bf8f871ce57bdd474665579d48b5b607fd8853031adaf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Wed, 13 Mar 2024 00:00:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 00:01:03 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 00:01:04 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Wed, 13 Mar 2024 00:01:05 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Wed, 13 Mar 2024 00:01:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:01:15 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Wed, 13 Mar 2024 00:01:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Wed, 13 Mar 2024 00:01:17 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Wed, 13 Mar 2024 00:01:25 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:01:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Wed, 13 Mar 2024 00:01:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Wed, 13 Mar 2024 00:01:28 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Wed, 13 Mar 2024 00:01:37 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c76c06c6cefd620f1bee631d3ef0cb4b5ff2f43cb6c4bc467f42a7957ed91ed`  
		Last Modified: Wed, 13 Mar 2024 00:01:46 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0c20501e700e6e2adca49de03fdade1fb63bf129f9e6193d1a147f93eeac2c`  
		Last Modified: Wed, 13 Mar 2024 00:01:46 GMT  
		Size: 497.9 KB (497923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:373dba251ff34f7ecb6a53345205a84853ef07b44005451433ce72d2e988d7a0`  
		Last Modified: Wed, 13 Mar 2024 00:01:45 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd101e8a5265161c1dc68504d4fe27aabf826a118d6267a29a0731157563e79a`  
		Last Modified: Wed, 13 Mar 2024 00:01:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb041f2a3a5e0e57b49f27337781c13a78def17456dde6a13833a7821712a6ca`  
		Last Modified: Wed, 13 Mar 2024 00:01:47 GMT  
		Size: 18.1 MB (18100234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db0516b989b3d824b58070d56ce76cbdb4857a91452aa1db612b35f2069564e`  
		Last Modified: Wed, 13 Mar 2024 00:01:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0470169505f5837d28dd1ce070fa69ab74724a4f0eae5d205582cb00e8e98`  
		Last Modified: Wed, 13 Mar 2024 00:01:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0d0334251bd3022ebf23025a7ade51d3679a24be762ea1d2465926748fc72d`  
		Last Modified: Wed, 13 Mar 2024 00:01:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e84106122f4b6ffdf7adbd8c82f5c4f6bfe3202f127230391286545d2519544`  
		Last Modified: Wed, 13 Mar 2024 00:01:44 GMT  
		Size: 18.8 MB (18833827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a44fe63ca105fe5b6353ac6e10e6a2df0f6876c7524d203d19464d5d805bd04`  
		Last Modified: Wed, 13 Mar 2024 00:01:41 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22a7d4c3e425c2c9d4c327f6af8a219034a8567bf7f978bf20e57eafb5d789b`  
		Last Modified: Wed, 13 Mar 2024 00:01:41 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0756dbf6a1fc368caa6df132fd109bc845b8425d3b3389ee31084188e94d071e`  
		Last Modified: Wed, 13 Mar 2024 00:01:41 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd3d0f820574a277b52d61896a9d3b23b63f4c9d0b9f19dfb14cd5b2400d723`  
		Last Modified: Wed, 13 Mar 2024 00:01:44 GMT  
		Size: 19.1 MB (19079355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
