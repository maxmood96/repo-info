## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:b7112326abea6d80243c51fcc91f9bb4cca7cf9e5f5058f858630bf352738c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.3091; amd64

```console
$ docker pull docker@sha256:6f5a1d58d3a295c56cf3487dee7e03235a593b49ffc54ffce7431fa10f78fb3b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2323222312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11458448354b46aecd66561bbbb390743d640df691af1e5d71f30dc50ff659dd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 21 Jan 2025 20:35:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Jan 2025 20:35:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 21 Jan 2025 20:35:14 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 20:35:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 21 Jan 2025 20:35:25 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 21 Jan 2025 20:35:25 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 20:35:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.windows-amd64.exe
# Tue, 21 Jan 2025 20:35:27 GMT
ENV DOCKER_BUILDX_SHA256=61123c807345d35525bc242bb182526cb0c10310eaf107bbcc97695be528c141
# Tue, 21 Jan 2025 20:35:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 21 Jan 2025 20:35:35 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 20:35:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Tue, 21 Jan 2025 20:35:36 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Tue, 21 Jan 2025 20:35:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7708a1d8eeacd2cc3ef23d36afdd035e4fd06683b3fa0eef7ba2676e3d97bf9e`  
		Last Modified: Tue, 21 Jan 2025 20:35:50 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07a074f7aa6353f7d4c776c9468654f2e33fce75050b464e5ddc51efe085021`  
		Last Modified: Tue, 21 Jan 2025 20:35:49 GMT  
		Size: 354.7 KB (354683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d65efb9628c3b66c7c12f5c4fd29c17a2a475f834eee5777dff48610d00e7e`  
		Last Modified: Tue, 21 Jan 2025 20:35:49 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaec66e2eaef12578a8eee1cd60f0d319ee82c838873009dc04ad05dfa196fe`  
		Last Modified: Tue, 21 Jan 2025 20:35:48 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c2867b0dcaed8c3542bcfc0bab7c4265d4119a6c4744b5e81d5ebb6602adf5`  
		Last Modified: Tue, 21 Jan 2025 20:35:50 GMT  
		Size: 19.2 MB (19161592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef05d9a1d493fc8bd1faee5b814727f57c9456678f87cef7e1ff79e5e1ac2f8a`  
		Last Modified: Tue, 21 Jan 2025 20:35:48 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd76eded3ebd9a22e40c1644a05e2595b67d0ed535abf3bde9c9aae8a7caa59f`  
		Last Modified: Tue, 21 Jan 2025 20:35:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78696a5e1fd4650022fcdbba7b13401cac129ed9ef7f9468d73671af727706f`  
		Last Modified: Tue, 21 Jan 2025 20:35:47 GMT  
		Size: 1.4 KB (1374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5944cc693ef786890a51eac7720f6c919e489ce5b0bd864cd9222ef97a1a4326`  
		Last Modified: Tue, 21 Jan 2025 20:35:49 GMT  
		Size: 21.1 MB (21139306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7414d4cba41b99f72c3fdb59e39686db1dd2d5a32864b0e9d1f0ec45391f5430`  
		Last Modified: Tue, 21 Jan 2025 20:35:46 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df079f762a735410253a5c4086620433c0187596e59c262ec844a1aab556111`  
		Last Modified: Tue, 21 Jan 2025 20:35:46 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f436c458c63d58bbe430894fa361de2df2879484f800c0057054d8631d294a`  
		Last Modified: Tue, 21 Jan 2025 20:35:46 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590ca98524d5be4347f23721029b6ffbc8a5fb0a1ca0680edf0b7445cc58653e`  
		Last Modified: Tue, 21 Jan 2025 20:35:49 GMT  
		Size: 20.2 MB (20169793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6775; amd64

```console
$ docker pull docker@sha256:221b1263563611445ed272fe601a2ef60621d7e9bb4188e3c3d1df301d9346c1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2183008867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e77ab7a0cdc3d613d2a36f5ec0e912776b35449fed6606598bae48c0dd064889`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 21 Jan 2025 20:35:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 21 Jan 2025 20:36:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 21 Jan 2025 20:36:34 GMT
ENV DOCKER_VERSION=27.5.0
# Tue, 21 Jan 2025 20:36:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.0.zip
# Tue, 21 Jan 2025 20:36:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 21 Jan 2025 20:36:48 GMT
ENV DOCKER_BUILDX_VERSION=0.20.0
# Tue, 21 Jan 2025 20:36:48 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.0/buildx-v0.20.0.windows-amd64.exe
# Tue, 21 Jan 2025 20:36:49 GMT
ENV DOCKER_BUILDX_SHA256=61123c807345d35525bc242bb182526cb0c10310eaf107bbcc97695be528c141
# Tue, 21 Jan 2025 20:36:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 21 Jan 2025 20:36:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.4
# Tue, 21 Jan 2025 20:36:58 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.4/docker-compose-windows-x86_64.exe
# Tue, 21 Jan 2025 20:36:59 GMT
ENV DOCKER_COMPOSE_SHA256=5df58bb738c7ac2712c031e15154b49f32f4026640d8c0539090d6e0a66d6dfd
# Tue, 21 Jan 2025 20:37:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd6b095143a1acfc1dc468f421c971f7bdd160fc522d3b71ed66145842c4c8ad`  
		Last Modified: Tue, 21 Jan 2025 20:37:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ada5849b6b1f68d709ea79de40133787fc8408ae09994a9f44decb930a60145`  
		Last Modified: Tue, 21 Jan 2025 20:37:12 GMT  
		Size: 338.8 KB (338826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5def4080a996f8f5956c399857b243f40748d3cd1fff254b895ff0650bc9e28`  
		Last Modified: Tue, 21 Jan 2025 20:37:12 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31b20a3e257c79c404c5dd0917aece6280d6686915fac961cda441256147470`  
		Last Modified: Tue, 21 Jan 2025 20:37:11 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2e76d9270d154efe561bebf01542a6cb5f7ded6a3ab187656a885295451b68`  
		Last Modified: Tue, 21 Jan 2025 20:37:13 GMT  
		Size: 19.2 MB (19157744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6a088fbaea7067a72d6514447dde3f6a97ed9007e54d441095e93f3b0e055d5`  
		Last Modified: Tue, 21 Jan 2025 20:37:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67eb581940775a6a0942141baff98fd5f5036c6ecf356bdd5ef29d5d623e600c`  
		Last Modified: Tue, 21 Jan 2025 20:37:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04113fcc5fbc396ba09045e258919eaec537ec240b38b9126331840405c19bfe`  
		Last Modified: Tue, 21 Jan 2025 20:37:10 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11653f59948e99a37353eccc7c5bcd9531bfdf0c0728fbccc46191b48777c42`  
		Last Modified: Tue, 21 Jan 2025 20:37:12 GMT  
		Size: 21.1 MB (21126698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96090b146e6be0c362a4ba7aa3daff87e1c28b333e6188a134e5e5c485bbfaa3`  
		Last Modified: Tue, 21 Jan 2025 20:37:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95829d9b74f994731e535eada077d3b7b4de5b3e21e1af3de6fc0cd00f93c0c`  
		Last Modified: Tue, 21 Jan 2025 20:37:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd951e1de42461bfc99a3c38db551394a9d6b3d875d94e101f4f0e9af7d4db9`  
		Last Modified: Tue, 21 Jan 2025 20:37:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89995df3595050f0c6c97903e06223c214f8e39bed8801d190a3f9775521fc95`  
		Last Modified: Tue, 21 Jan 2025 20:37:12 GMT  
		Size: 20.2 MB (20161776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
