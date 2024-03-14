## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:fcaddb916ac53ad62fa97f37689df3b880c5e757537cb8d800ee649a7ccf765c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull docker@sha256:a8613d82186d9c5baabb977605e7fce07c3d5f1dc610d5bde7e589e09597ecbd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2013397085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ec2b2f1402648b607fd36135d5d38cb33eca711de1e98cb34d31137346f4f17`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Thu, 14 Mar 2024 17:55:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Mar 2024 17:55:29 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Mar 2024 17:55:29 GMT
ENV DOCKER_VERSION=24.0.9
# Thu, 14 Mar 2024 17:55:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Thu, 14 Mar 2024 17:55:39 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 17:55:39 GMT
ENV DOCKER_BUILDX_VERSION=0.13.1
# Thu, 14 Mar 2024 17:55:40 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.13.1/buildx-v0.13.1.windows-amd64.exe
# Thu, 14 Mar 2024 17:55:40 GMT
ENV DOCKER_BUILDX_SHA256=6b113e84cbc3cd645646aa82f00a7f7d3737cc10375b4341e0aca0de0c997c75
# Thu, 14 Mar 2024 17:55:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 14 Mar 2024 17:55:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.7
# Thu, 14 Mar 2024 17:55:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.7/docker-compose-windows-x86_64.exe
# Thu, 14 Mar 2024 17:55:50 GMT
ENV DOCKER_COMPOSE_SHA256=1a5ffa12cff51a65f4e5e8874ed46b0783cfbc8f5ef837f5b9523decf1afd1d0
# Thu, 14 Mar 2024 17:55:58 GMT
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
	-	`sha256:6e2c4a05918f0191705a380b7b3632757947ea81e2f340d0886e095703869430`  
		Last Modified: Thu, 14 Mar 2024 17:56:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4ee370d1664eae4e2da1f89383d1f4c0a2b68dc42ec7e3f4eb5690414a8feef`  
		Last Modified: Thu, 14 Mar 2024 17:56:08 GMT  
		Size: 494.1 KB (494052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62e0bbfebb8872dcba7a831d806090efb01971080ae97b30d7e5a19f9bd7dbc5`  
		Last Modified: Thu, 14 Mar 2024 17:56:08 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8034f563698cef6e1af1af52c20cc9e3d59f389082c88c4b56fe95942c9f8ea`  
		Last Modified: Thu, 14 Mar 2024 17:56:06 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ce8ceb1b8e665dae4c6912e7c4b4b5fa0aff979744fbd91ae91382df5ed584b`  
		Last Modified: Thu, 14 Mar 2024 17:56:08 GMT  
		Size: 17.5 MB (17531868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24381276353629657cb2598f54d6a9cd59ee547d6144bcdb6c23be4057cc01e6`  
		Last Modified: Thu, 14 Mar 2024 17:56:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff6693189eb3d09d0cf49949d042c1cf396ea6d6b67b6a7fc99dd02bf7259dfd`  
		Last Modified: Thu, 14 Mar 2024 17:56:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d0a3427c31e205fed33f03584de925c4c858f29ad24734216809aaaef36d1f`  
		Last Modified: Thu, 14 Mar 2024 17:56:04 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e03127d21dc4d3b1fe4d63cf427ce50aaf583b12f52981f64c0a9d1e53c938a1`  
		Last Modified: Thu, 14 Mar 2024 17:56:05 GMT  
		Size: 18.8 MB (18827609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069619e508e14c03fb28513ca4afb7e871177c21e9002c9aa2a3fc1410b5445e`  
		Last Modified: Thu, 14 Mar 2024 17:56:02 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2114a5716d97b0fdd6f508be36151a26dfa3404ec98fd1cad957c5513ddc36`  
		Last Modified: Thu, 14 Mar 2024 17:56:02 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378064cb16efdc2ba7ed69ea8edce032bb44a3ce564e0e01471949090ba7c1d9`  
		Last Modified: Thu, 14 Mar 2024 17:56:02 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cff3f39c0864defb5f1813fb030d7b69c13ef2d61af792c7a22cdb10f9d881`  
		Last Modified: Thu, 14 Mar 2024 17:56:05 GMT  
		Size: 19.1 MB (19072923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
