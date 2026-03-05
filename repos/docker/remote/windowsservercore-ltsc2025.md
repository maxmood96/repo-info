## `docker:windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:aa78f3c793d1165f83ee2f02437004195ebf5d6a1098451d27b497c3a30de79c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `docker:windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:a72ce64c78274996c1b4b42d7a0f66f37175630ed095e8ba4e2a696b73abc496
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2026133456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb24733fa85780e10415c1eead19dfee395c7ad5b5c7b0bb7b46a9cb04da12d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Thu, 05 Mar 2026 18:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Mar 2026 19:00:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Mar 2026 19:00:43 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 19:00:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Thu, 05 Mar 2026 19:01:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Mar 2026 19:01:00 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 19:01:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Thu, 05 Mar 2026 19:01:01 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Thu, 05 Mar 2026 19:01:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Mar 2026 19:01:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 19:01:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Thu, 05 Mar 2026 19:01:12 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Thu, 05 Mar 2026 19:01:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91d1a8a6e8a02bacaa0cb852af9b130f79b3e75217c941735e602588438341d`  
		Last Modified: Thu, 05 Mar 2026 19:01:29 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915ea27d9fcff3265f8621bcd58538383106512d8ee139843933e4aa2dac3703`  
		Last Modified: Thu, 05 Mar 2026 19:01:29 GMT  
		Size: 401.5 KB (401543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd10d9d7b58e5996fb583d0b0d10d055606d96f9edf196ff1f5742fdd10220d9`  
		Last Modified: Thu, 05 Mar 2026 19:01:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851d627862c692ace5c664d4125ca0b51d34d0d36620e45cc69347d1782b4f4`  
		Last Modified: Thu, 05 Mar 2026 19:01:27 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3611e153866cd60e61b0cb5e1d10488d937bb671126d8b9a445e42bfef0cdb`  
		Last Modified: Thu, 05 Mar 2026 19:01:30 GMT  
		Size: 19.6 MB (19622332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0b288bc9f43ef9edf51a4b865e0dc86c931e34102b33c9a926db1b273153c2`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071a5927eed307df7387e858c0a092a79362a038fb7a196d6284f2a836fd53a4`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b18e8aa1db4565b440e2467adaa75cbb4d144987fd6c20b4405e5d8ce70a7`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447abe3658079578872007da50315083eee58828fb752c05af4f9333bac9a15`  
		Last Modified: Thu, 05 Mar 2026 19:01:29 GMT  
		Size: 29.7 MB (29666438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db544d374eecea25c6051e8e18b98719807c54789d9d109d2e7587a9fc0107d0`  
		Last Modified: Thu, 05 Mar 2026 19:01:24 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c94d4d5d67e7de268a916c2ca0a9cd33d175d5de6c7ba600caea238b0342ca5`  
		Last Modified: Thu, 05 Mar 2026 19:01:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076172216a77708fe1042dbc178297940214b0c2b67229608d5b180a82521d5`  
		Last Modified: Thu, 05 Mar 2026 19:01:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2075710695e1e3ef40ee40ef482cbccc04111fa62f56d5da7dc61ba5d0c5352`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 11.7 MB (11671331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
