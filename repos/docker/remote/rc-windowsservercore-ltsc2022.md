## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:5258aacc07b661b5dcc2e531c83fe53717edcaf99e316ff9ec69ea52e8a95f12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:035c05fcce3198152b4157e0ad39cf52f7ababb12f0d56a4ad95c64677516744
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038020088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e8f28cd22d672c311b91be19969103d99bebbcbcfcb93b521abfebae661081`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Fri, 03 Apr 2026 16:44:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:45:20 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:45:20 GMT
ENV DOCKER_VERSION=29.4.0-rc.1
# Fri, 03 Apr 2026 16:45:22 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.4.0-rc.1.zip
# Fri, 03 Apr 2026 16:45:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:45:33 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:45:35 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:45:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:46:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9da6bec9129477f95248df012e3c95af897071a17f295005157697d398f7a8a`  
		Last Modified: Fri, 03 Apr 2026 16:46:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431b75303dee1a94631986a8d853d10b4954aaf33183462263298acb84c04a1a`  
		Last Modified: Fri, 03 Apr 2026 16:46:13 GMT  
		Size: 502.7 KB (502740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c254d8f2576834e1e2d179c36c3f54cd49bb79ac5e3aa4cba5b38634c57e234`  
		Last Modified: Fri, 03 Apr 2026 16:46:12 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095d0ea30e4edaf819bc0be1eda06ade8abb9ce866f352d4231d4bde13f3c960`  
		Last Modified: Fri, 03 Apr 2026 16:46:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d68affeec4efbe4b05efc3ae1e3f71aa81b43ee481df24ca807f46cc7a0fc`  
		Last Modified: Fri, 03 Apr 2026 16:46:14 GMT  
		Size: 20.1 MB (20145774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1dc5f43325b5b602b59c5d972f49fd08c807203a494c8d48e9c502836d9e58`  
		Last Modified: Fri, 03 Apr 2026 16:46:10 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23fc5cf9f86530c3cbacf67a16ade26b9dcd3bdf8fc5f489c2c038cb872913a`  
		Last Modified: Fri, 03 Apr 2026 16:46:10 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a46e4088c8296ddb01eb9bf19c7f7ee7bd32efa49e8d5ee2fad2366f7faaddb`  
		Last Modified: Fri, 03 Apr 2026 16:46:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88dd606db010eece3badf6b6f978f4ad5587bf711e973dab82cc352869a558c`  
		Last Modified: Fri, 03 Apr 2026 16:46:23 GMT  
		Size: 23.4 MB (23434424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bcba0754c5a5b20e37b8258d0c23e2c907bc84c5299eecac20cf862a818b91`  
		Last Modified: Fri, 03 Apr 2026 16:46:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9dc27b70d34bebea3433443de19bd77ff4787d228e128ff259ae16c64d6958`  
		Last Modified: Fri, 03 Apr 2026 16:46:09 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764d925495d3487d672141eaf3ccaceaa1a407e19a6dadcb33487b426241dfe6`  
		Last Modified: Fri, 03 Apr 2026 16:46:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd771fd7ddb4e6a40933bfe63393c1df876459af1c746145baea179b10d7113`  
		Last Modified: Fri, 03 Apr 2026 16:46:11 GMT  
		Size: 11.6 MB (11643994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
