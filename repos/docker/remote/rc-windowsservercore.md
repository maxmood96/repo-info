## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:187ecac2d421e3e9c08712f485d248ebd0fc1d52706abb849c28ed0e187d92bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `docker:rc-windowsservercore` - windows version 10.0.20348.2340; amd64

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

### `docker:rc-windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:b0bd5fb3b8b69be9f935b36263ba9f67c393a779f61507cd4e362a2270412b3f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2181660394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89160038a36a69449b2cd36f2327815dfa7a11f9f2557dffc52135b8095b3986`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Wed, 13 Mar 2024 00:00:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Mar 2024 00:00:59 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Mar 2024 00:01:00 GMT
ENV DOCKER_VERSION=26.0.0-rc2
# Wed, 13 Mar 2024 00:01:00 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-26.0.0-rc2.zip
# Wed, 13 Mar 2024 00:01:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:01:31 GMT
ENV DOCKER_BUILDX_VERSION=0.13.0
# Wed, 13 Mar 2024 00:01:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.0/buildx-v0.13.0.windows-amd64.exe
# Wed, 13 Mar 2024 00:01:33 GMT
ENV DOCKER_BUILDX_SHA256=001dd8c707862d7c7a7bc17ebb024922ee304bddad1bca11da5b3b3ff18effa6
# Wed, 13 Mar 2024 00:02:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Mar 2024 00:02:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Wed, 13 Mar 2024 00:02:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Wed, 13 Mar 2024 00:02:04 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Wed, 13 Mar 2024 00:02:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a22a88a4a0d197cb745939f382a7898094af0a089fce3173f283651a01da996b`  
		Last Modified: Tue, 12 Mar 2024 17:24:49 GMT  
		Size: 474.5 MB (474479569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a450511872bd4fb40f3cadb12956a857f22b40fc2af1313573967b171abb04`  
		Last Modified: Wed, 13 Mar 2024 00:02:44 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02ad1b5b768e055a44080e549de53434f38a0df13953e8813763ab13e577dc`  
		Last Modified: Wed, 13 Mar 2024 00:02:44 GMT  
		Size: 495.5 KB (495516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dad9fb28ba7c5c11d2a571f8f5449243b1a1bfc72a70b6cf633d8bd98a10eb56`  
		Last Modified: Wed, 13 Mar 2024 00:02:42 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39b36d197c455034ef31270112c5d4dfb5aee9cdfe490cd6df3f9c01b48d6779`  
		Last Modified: Wed, 13 Mar 2024 00:02:42 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9aacad36f362e807f77239771fa680d4d98dd89896508c9946be4bcdee9ca65b`  
		Last Modified: Wed, 13 Mar 2024 00:02:44 GMT  
		Size: 18.1 MB (18115454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec1ae033359eab29e860a6aca4dd4e8fa8504b090c0c6eb6c1ef1e59c773fb`  
		Last Modified: Wed, 13 Mar 2024 00:02:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd619dfd467857a02fd6fa3293ff7ac8fff68399a8329846a2cc548bdd7ad3b0`  
		Last Modified: Wed, 13 Mar 2024 00:02:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe5e36faca16bb434398f227eeb062bf2e4f47150cfd68d1faa8ee598b4ea76`  
		Last Modified: Wed, 13 Mar 2024 00:02:40 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8b35f2482a9a5186d4a9850fb623dbdf426f547939e489ebdefbd2c1169f5ae`  
		Last Modified: Wed, 13 Mar 2024 00:02:41 GMT  
		Size: 18.8 MB (18845787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ce28b8ccf0cb9cffe87256fb37fe73ce50a104327ad3f2e783281c650a86cc`  
		Last Modified: Wed, 13 Mar 2024 00:02:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c77e3a517a602fbfcd714f6810001c594cd10c1a0ce4473fbef9b4aa43586c2`  
		Last Modified: Wed, 13 Mar 2024 00:02:38 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f2fce7f92f0b9fc4209637e735d8aa4cc9909ed7e6fdf8636eefddbfe4c29`  
		Last Modified: Wed, 13 Mar 2024 00:02:38 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9575b0c23636029bf92fd2f43ebf280b4075170c1d34c207ea9492b22cc730`  
		Last Modified: Wed, 13 Mar 2024 00:02:41 GMT  
		Size: 19.1 MB (19092014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
