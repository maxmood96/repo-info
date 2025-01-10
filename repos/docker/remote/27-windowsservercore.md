## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:edb7aff1c0cd6c7c15802d3bc3d4c76873b2329b9fe50c75c97f50e9449e35fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6659; amd64

### `docker:27-windowsservercore` - windows version 10.0.17763.6659; amd64

```console
$ docker pull docker@sha256:17d1ca1503ccd918b9f134fb58a7e94a6b55605a487375dc958dd83a765680e2
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2073461807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52119a98321109fc04c5bdc9d5a5997da126c6b299e2e05092227fbbdfcc5ac5`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 05 Dec 2024 05:10:22 GMT
RUN Install update 10.0.17763.6659
# Thu, 09 Jan 2025 22:28:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Jan 2025 22:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 09 Jan 2025 22:29:47 GMT
ENV DOCKER_VERSION=27.4.1
# Thu, 09 Jan 2025 22:29:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.4.1.zip
# Thu, 09 Jan 2025 22:30:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 09 Jan 2025 22:30:03 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 09 Jan 2025 22:30:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 09 Jan 2025 22:30:04 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 09 Jan 2025 22:30:16 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 09 Jan 2025 22:30:17 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Thu, 09 Jan 2025 22:30:18 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-windows-x86_64.exe
# Thu, 09 Jan 2025 22:30:18 GMT
ENV DOCKER_COMPOSE_SHA256=f384ad29e5187745cad4c18a14ddafd5e7a748c68b5bd991599b1756e36d3bec
# Thu, 09 Jan 2025 22:30:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3308b54d35b61854238974280a5b0ecc72a98e2ead17d04f42770a7b35407090`  
		Last Modified: Tue, 10 Dec 2024 18:45:28 GMT  
		Size: 293.9 MB (293901821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7750dc03308256989666ff5b54c38b3a2c612c962192c83de4eb1f582ca937b1`  
		Last Modified: Thu, 09 Jan 2025 22:30:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dbe0537aa6aca34fc480d362d820e72c216e0298e460381cfbb5dcb5fd023fb`  
		Last Modified: Thu, 09 Jan 2025 22:30:39 GMT  
		Size: 472.5 KB (472525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe45cd9447359ded7b92b30cf20968456c9963557aae6f640a79b6e9e154bb96`  
		Last Modified: Thu, 09 Jan 2025 22:30:37 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e084105c5050f37f2a84321c45579ce3b732eafca7dacb323be6a6d0466d89`  
		Last Modified: Thu, 09 Jan 2025 22:30:37 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5632113851589ab8b783167c256f837cf86bc42cf5a08905a82e3ca1050d791e`  
		Last Modified: Thu, 09 Jan 2025 22:30:39 GMT  
		Size: 19.0 MB (18995177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6fc5b4da6366b80ed16ea446e845f9e47d993a065cccd224a4bf5c26a9ffad`  
		Last Modified: Thu, 09 Jan 2025 22:30:36 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1c4f578feffda9102418bc2ffcd55cf99c58f657c94a9e437200b4ab6e37ce`  
		Last Modified: Thu, 09 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e594fee58a2fad417e3fde8355dc41c0508bd2ab66d1729873f044f701a70680`  
		Last Modified: Thu, 09 Jan 2025 22:30:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ea03058c311bb36b7446687d979343ed3f3ecaf0b8a1a35a23c20666373964`  
		Last Modified: Thu, 09 Jan 2025 22:30:37 GMT  
		Size: 19.6 MB (19646983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:601a2adbccc0e8163567c2d53522349047c62ff729a5a3a1c6a4efbe2c8ff4bb`  
		Last Modified: Thu, 09 Jan 2025 22:30:33 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:477c2e6248c325fbcac1b955bb7066d647e306083381336c71c46addade98c49`  
		Last Modified: Thu, 09 Jan 2025 22:30:33 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:648ab5467de2471d85da31b50821da19a02285bd29d6edb1c98f0efea89d6074`  
		Last Modified: Thu, 09 Jan 2025 22:30:33 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff4279d2d18be75803362cc5a646d7d96b8fffd5030ddb9674444c5d344b414`  
		Last Modified: Thu, 09 Jan 2025 22:30:36 GMT  
		Size: 20.2 MB (20165195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
