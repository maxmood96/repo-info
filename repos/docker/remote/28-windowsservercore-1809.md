## `docker:28-windowsservercore-1809`

```console
$ docker pull docker@sha256:ac53b66739b0c0eef4db41f8d2ea61b5a896b50b4215355c1a31f32ead9cd656
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `docker:28-windowsservercore-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:0a694638bc3152b57c933b27342a3675817c76fe00b6e473ddf7569acb752858
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216825684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f28e7bd7c2a77861878ea9d6acc2c71f7f5f06e846a61d3447f6d5333c367a69`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Fri, 14 Mar 2025 20:22:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 14 Mar 2025 20:22:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 14 Mar 2025 20:22:54 GMT
ENV DOCKER_VERSION=28.0.1
# Fri, 14 Mar 2025 20:22:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.1.zip
# Fri, 14 Mar 2025 20:23:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:23:08 GMT
ENV DOCKER_BUILDX_VERSION=0.21.2
# Fri, 14 Mar 2025 20:23:08 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.21.2/buildx-v0.21.2.windows-amd64.exe
# Fri, 14 Mar 2025 20:23:09 GMT
ENV DOCKER_BUILDX_SHA256=480d8f92cbb58a9c25227b070de90f0d24531f6a82be1f18b55950714ad52f15
# Fri, 14 Mar 2025 20:23:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 14 Mar 2025 20:23:19 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Fri, 14 Mar 2025 20:23:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Fri, 14 Mar 2025 20:23:20 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Fri, 14 Mar 2025 20:23:30 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed918122fc29d1ad29df866b313bce7001d47ac1eb47062e4235994521aef586`  
		Last Modified: Fri, 14 Mar 2025 20:23:39 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cd329e02e93a958cd27d04d45a380670c9d25f0fd7d06e62522c8b70baf8e7a`  
		Last Modified: Fri, 14 Mar 2025 20:23:39 GMT  
		Size: 339.4 KB (339420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60059bb6810810d7fd065fdc61f8f620ad5a195503e861cb7cd6b2d638fecb74`  
		Last Modified: Fri, 14 Mar 2025 20:23:38 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d1c9f5395896c289e6089101131c105321a3869ba6dd90e3950be2adc74c3b`  
		Last Modified: Fri, 14 Mar 2025 20:23:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab3ac701ca298923890a22b35dbdf2811d83ac7ad47cd329cbfe93c5deb49dc4`  
		Last Modified: Fri, 14 Mar 2025 20:23:39 GMT  
		Size: 19.8 MB (19815150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ebd6e37566eae8442f166b1107e57e98f66ff6e80718cfc1f7cf8061f7bee1`  
		Last Modified: Fri, 14 Mar 2025 20:23:36 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f82c328b654329fdfeedec58a10c0622ac05de5ef2fbcf213575b18d0ddb6d`  
		Last Modified: Fri, 14 Mar 2025 20:23:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5b5f4d03be59c4be11f3157cc59a36dea48da05b4a8ebdaed5e13e0a2c1dcdd`  
		Last Modified: Fri, 14 Mar 2025 20:23:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0bea2b6f7984f4b6aca23c9e0bf53b4586c96e09eb75d9914c06d1e63a4e8c`  
		Last Modified: Fri, 14 Mar 2025 20:23:37 GMT  
		Size: 22.7 MB (22740895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035b7581971c5d79ebc58ffdb94bb5df3fd9514696e4515ddb6ef80845b5a997`  
		Last Modified: Fri, 14 Mar 2025 20:23:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a11663aaf86370562ddb2f14941d1012988a41b2a8723e1cdfd217a951144a5`  
		Last Modified: Fri, 14 Mar 2025 20:23:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd77d2ca98e41f2583ed3da2d477d7217f482cb971d7decc53c9a20eb798b4dd`  
		Last Modified: Fri, 14 Mar 2025 20:23:34 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22db86579608f100db6522d1ed570194e7e942c453a471207da13d66670a9c38`  
		Last Modified: Fri, 14 Mar 2025 20:23:37 GMT  
		Size: 22.3 MB (22283834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
