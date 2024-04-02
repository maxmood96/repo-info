## `docker:windowsservercore`

```console
$ docker pull docker@sha256:8ae67efdfe41725885a1ad1aef9789305dddf846b94157077225d7035164303c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2340; amd64
	-	windows version 10.0.17763.5576; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:d5db1f7d4f8c994279d8d5dce25b65688c10b6002fda76e220e5c3c803bb03e2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2014380189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a62f86a295c4aab4a44289838a6af4d3770cfb23a7c55b031379d5d3cbe961c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Mon, 01 Apr 2024 23:49:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:51:25 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Apr 2024 23:51:25 GMT
ENV DOCKER_VERSION=26.0.0
# Mon, 01 Apr 2024 23:51:28 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.0.0.zip
# Mon, 01 Apr 2024 23:51:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:51:52 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 01 Apr 2024 23:51:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 01 Apr 2024 23:51:55 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 01 Apr 2024 23:52:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:52:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 01 Apr 2024 23:52:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Mon, 01 Apr 2024 23:52:11 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Mon, 01 Apr 2024 23:52:21 GMT
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
	-	`sha256:da1f9962ef35d4d08edd8c0d24528d2ad4bac864eaa7214defae04a0e4f09acc`  
		Last Modified: Mon, 01 Apr 2024 23:52:34 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e3e8dfc0eb3d787e171ba44502cb987d4afcd5af94251e43b9ecc6f2428549`  
		Last Modified: Mon, 01 Apr 2024 23:52:34 GMT  
		Size: 496.7 KB (496667 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3e8c593ef3c1486ffbb60703210cfeb3819af65fe4ed985df2eb31cd902452c`  
		Last Modified: Mon, 01 Apr 2024 23:52:33 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d6fa7cb58e40e4af1d144f0c9c7685e5372420434324feb3c5a668983556bb8`  
		Last Modified: Mon, 01 Apr 2024 23:52:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16d02c78aecac0454cb8b52f7cda79b107bb6051d70fc24c77ed96db80389b5`  
		Last Modified: Mon, 01 Apr 2024 23:52:36 GMT  
		Size: 18.1 MB (18118122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e3188a4c8d2a2787280046c2a940a22f1988c44234e2c8ccd5baa1856a25686`  
		Last Modified: Mon, 01 Apr 2024 23:52:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efb3982b6a6a9d667781f24386dc65cbb47840895fac5ca0ecac372eb7576820`  
		Last Modified: Mon, 01 Apr 2024 23:52:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f70b1e1951e8d98b0a1cf215d6969f834be2545825fac7abacb60edfc6b5467`  
		Last Modified: Mon, 01 Apr 2024 23:52:31 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c71ab1904b9e9d3b4efd73be2cee0ec063a29d1a61fc023f109e69594d62578b`  
		Last Modified: Mon, 01 Apr 2024 23:52:31 GMT  
		Size: 18.8 MB (18795328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5dea88fdd0632577ef152548c0141e1bab955339661b35e7524341503619045`  
		Last Modified: Mon, 01 Apr 2024 23:52:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c868600d8491a646c603b85dd6b54a6516900d37c19df24c7fafdfd60df167e0`  
		Last Modified: Mon, 01 Apr 2024 23:52:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cae32af746e18c421f9b9586fe98a6da255f6e77b4114aa2c506a92e84325ec`  
		Last Modified: Mon, 01 Apr 2024 23:52:28 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fe44f5e2f6445e7e2865d2dc3be01b66e6ecef42d531dd90054139980062580`  
		Last Modified: Mon, 01 Apr 2024 23:52:31 GMT  
		Size: 19.5 MB (19499447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5576; amd64

```console
$ docker pull docker@sha256:4e499d09ba345d980ffe78dd400c4d9f0ef2284b5b4c3185bc4ebd893f0bbe09
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2182147946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32a403716847de44127d69a354b3f241984887e520e8ca114c2c1e365f31084`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Mon, 04 Mar 2024 01:18:21 GMT
RUN Install update 10.0.17763.5576
# Mon, 01 Apr 2024 23:49:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Apr 2024 23:50:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Apr 2024 23:50:53 GMT
ENV DOCKER_VERSION=26.0.0
# Mon, 01 Apr 2024 23:50:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.0.0.zip
# Mon, 01 Apr 2024 23:51:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:51:27 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Mon, 01 Apr 2024 23:51:27 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Mon, 01 Apr 2024 23:51:28 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Mon, 01 Apr 2024 23:52:01 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Apr 2024 23:52:01 GMT
ENV DOCKER_COMPOSE_VERSION=2.26.1
# Mon, 01 Apr 2024 23:52:02 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-windows-x86_64.exe
# Mon, 01 Apr 2024 23:52:03 GMT
ENV DOCKER_COMPOSE_SHA256=d8a386d375ef26a77be0bee97516b0287d93acafb3976806f42e2b76c6904125
# Mon, 01 Apr 2024 23:52:32 GMT
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
	-	`sha256:49ef31e75a22949996a922d432e539b77e3ff81bcf7a021fbeb9ddc464d4187e`  
		Last Modified: Mon, 01 Apr 2024 23:52:41 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39e917dc03a4b8d5786a826c74bf16e144f621a94305a161608481674f8424ac`  
		Last Modified: Mon, 01 Apr 2024 23:52:41 GMT  
		Size: 497.3 KB (497331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1321b2bf96470b896d833b52c12fb933cf81f93eaf0d54ec03eaa64c71df7979`  
		Last Modified: Mon, 01 Apr 2024 23:52:40 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d434b8d44f34281339e42c6c32c646f9654605dd95508025e06dc12b3fc244`  
		Last Modified: Mon, 01 Apr 2024 23:52:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a16c2d13ed238b2a574df5f274d943bf28249ae22e7e6b2517bed805e9f46a`  
		Last Modified: Mon, 01 Apr 2024 23:52:42 GMT  
		Size: 18.2 MB (18166568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:125b771bea7102e00bbb7d0b77b46f3dd9cb3b629c2e56dd30ef744debef3255`  
		Last Modified: Mon, 01 Apr 2024 23:52:38 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3b55a07b3f847ac9933b521fca2bf9206349dea6e884243dc8d08a87975889`  
		Last Modified: Mon, 01 Apr 2024 23:52:38 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7d9d51e6224c6f4feeb142b98dac77c63c0b044181e53c766cc59407c645c7`  
		Last Modified: Mon, 01 Apr 2024 23:52:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2777e030af1b4fdf76d6a4087048dbda2720cc5478b626fb850f9cf3618bbab`  
		Last Modified: Mon, 01 Apr 2024 23:52:39 GMT  
		Size: 18.8 MB (18833956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf9e80eb8cc4334fee6ea3568a6adae9811ba302e1f4512d82c36c34d33063d`  
		Last Modified: Mon, 01 Apr 2024 23:52:36 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea19569a5f9c9aabbe7e10adb28594ed798432b0825077ab67fd6ebe3f2c6b9`  
		Last Modified: Mon, 01 Apr 2024 23:52:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d6fd1f98a8c919812c1bddd736c9e94a950ffa3fcfdb168c6c9835ffc32eb4`  
		Last Modified: Mon, 01 Apr 2024 23:52:36 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90bb42b84466aa4fd9b3f4a2a321d1c0c90f90e31dcb2b7bfd408ae8fa7e80a6`  
		Last Modified: Mon, 01 Apr 2024 23:52:39 GMT  
		Size: 19.5 MB (19538447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
