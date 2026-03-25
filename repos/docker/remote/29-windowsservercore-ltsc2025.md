## `docker:29-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:fdd48859b2b14b2fa4af458fcea153cfd95e8ce7429e66286229f28b47e507b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `docker:29-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:42419a818a06c8b0bdb32d28efe864c1965f849d4d58dac6450fb35578530636
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2142463243 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:095982a564f926ffd785368388022d0f792a5f393f83c25b2b334b3f0ee3c25f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Wed, 25 Mar 2026 18:28:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Mar 2026 18:29:47 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 25 Mar 2026 18:29:48 GMT
ENV DOCKER_VERSION=29.3.1
# Wed, 25 Mar 2026 18:29:50 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.1.zip
# Wed, 25 Mar 2026 18:30:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:11 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Wed, 25 Mar 2026 18:30:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Wed, 25 Mar 2026 18:30:13 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Wed, 25 Mar 2026 18:30:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 25 Mar 2026 18:30:35 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Wed, 25 Mar 2026 18:30:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Wed, 25 Mar 2026 18:30:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Wed, 25 Mar 2026 18:30:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c48ff63fd51e54c1621e1ef191ba1ffb5babb91295c52763e73038877ddbcc0`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05646e87bcc7eebcf75f1a96ca80aa255bd6868601cdf94768601c8078d9b4b7`  
		Last Modified: Wed, 25 Mar 2026 18:30:55 GMT  
		Size: 374.0 KB (373997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edba92fa22a5c1bc563c18f651db43bfdc9c0720c21fff8d046d759875e121d1`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b934d13e109edc08e9a08ca989659aded111b61867e75aa39cc626586e14b6d`  
		Last Modified: Wed, 25 Mar 2026 18:30:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ff304ba5506cff7b400064688c74084a2ff60a244b484160e1be812e7672e3d`  
		Last Modified: Wed, 25 Mar 2026 18:30:56 GMT  
		Size: 19.6 MB (19594910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47622b1e857ba4fe582334af32ea59c3b58783ab368030f1d2259ae216996aaa`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a676a9fc9cb7650a5a61aad602e864237a2410b300b3babac5f0cfb4c9f31bf9`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d698051d32bbd456b5de7801253c16270739faf8954ce78f45f3a7e95830067`  
		Last Modified: Wed, 25 Mar 2026 18:30:52 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b8f6f29800e2912ff8cd1d9696f47141cb71560b98c73b71157c6b39d77665`  
		Last Modified: Wed, 25 Mar 2026 18:31:04 GMT  
		Size: 29.6 MB (29639971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbee4f4914616df04e2f56d66e020a4ca506723690da654928872871a3d1130`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36549e61114f7f53657411a2bc956fd69c15ae2f08beb6f977143978b7447c7a`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:111317c19214d92002469ac71ea269b2b838ae7163f090cf6796b17aeccea76d`  
		Last Modified: Wed, 25 Mar 2026 18:30:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ee1dd44d7e561101a0c094be20961ded0b2b663201441b16b06bbace8b589ab`  
		Last Modified: Wed, 25 Mar 2026 18:30:53 GMT  
		Size: 11.6 MB (11646539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
