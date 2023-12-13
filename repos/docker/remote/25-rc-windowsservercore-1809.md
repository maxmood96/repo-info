## `docker:25-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:d9425a131d2233f8554f8bfecea3c27be483f8c8c4f49dd1756fc75e1b5037ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `docker:25-rc-windowsservercore-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull docker@sha256:b1af015dee967f96b760164c8760fac29f4a66031595083b97d6d3587fa06c98
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2114943798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb97fad577702d33a76970c4862c81973332f739c5c978b569c87fdc15dafcc1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Dec 2023 11:24:49 GMT
RUN Install update 10.0.17763.5206
# Wed, 13 Dec 2023 01:04:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 01:05:37 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Dec 2023 01:05:38 GMT
ENV DOCKER_VERSION=25.0.0-beta.2
# Wed, 13 Dec 2023 01:05:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-beta.2.zip
# Wed, 13 Dec 2023 01:06:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:06:08 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Wed, 13 Dec 2023 01:06:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Wed, 13 Dec 2023 01:06:09 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Wed, 13 Dec 2023 01:06:32 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:06:33 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Wed, 13 Dec 2023 01:06:34 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Wed, 13 Dec 2023 01:06:34 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Wed, 13 Dec 2023 01:06:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35ae5ad761bfd7e5fb48c234de8722eaa28e17e2c956816fecb417ab6259c29`  
		Last Modified: Tue, 12 Dec 2023 19:14:24 GMT  
		Size: 409.1 MB (409088642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc7c691d4b4494298ded236cf06ec30a3877f49af606715710f8344a7a71892`  
		Last Modified: Wed, 13 Dec 2023 01:07:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:192f6372aadfc95509daaaac4c410f76d50aae852811c82f2579740e22fe56d3`  
		Last Modified: Wed, 13 Dec 2023 01:07:09 GMT  
		Size: 474.8 KB (474787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73669d4da0d289b3a5381c0ef897e381c059daa1113a5ae3b7ebd66494295ba2`  
		Last Modified: Wed, 13 Dec 2023 01:07:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4ca6ccfdc396c2a5fbaaadacf7e4b7c436945faf4f25cd3f18f03e05ee5271`  
		Last Modified: Wed, 13 Dec 2023 01:07:08 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97ebfbd23172ba2c298619ec6b59b03a731ac32a9f1027f7ea3e2c48784898f3`  
		Last Modified: Wed, 13 Dec 2023 01:07:09 GMT  
		Size: 18.1 MB (18050561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e637bc632583ef923d99623d29c50ac16b1edffe3e3ebbdfa63192dc2d7feeb`  
		Last Modified: Wed, 13 Dec 2023 01:07:06 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51be4cbbdc939507c98198d658762d5fd55d0a1504d056d60c20fbe7ccc04b80`  
		Last Modified: Wed, 13 Dec 2023 01:07:05 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f22af0d818cffe5f23cb01c87118ca00b4918b4b4e12f93712133f0708d2449`  
		Last Modified: Wed, 13 Dec 2023 01:07:05 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c504c27fbd17f1d7ed7518b9fef52e342a85dfc1bec3d3508def8ede3212d30`  
		Last Modified: Wed, 13 Dec 2023 01:07:06 GMT  
		Size: 18.0 MB (18009285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcf284771c0e16d0e0c82a76b9eaf2bfef57c3b4513da372cbd3130d93c918d2`  
		Last Modified: Wed, 13 Dec 2023 01:07:03 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6f83e2846c82b447558a269ed63b4be05e9616d01e15dac557589b1bd869d49`  
		Last Modified: Wed, 13 Dec 2023 01:07:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:093e5e35c9c8d8989d399d3448bd160bd8f73f29425d21e81a6f76bdbd685320`  
		Last Modified: Wed, 13 Dec 2023 01:07:03 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62f6f460b9b50d07b9a9d5a446e9e8683f104ed245d7fb5306f8d0a708dd9e8e`  
		Last Modified: Wed, 13 Dec 2023 01:07:06 GMT  
		Size: 18.7 MB (18688508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
