## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:1aed70a06e98849ba522c0e189fe229291a0c26e5c304faffafca5621ff2a2d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:ba777ce4ffefb7e1a583a0b952b175b2f37d9d93d3ecdc3325b334b36049a79f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262437168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88821562bde9244631c7e166f6acc156ddcf127956ef23332df624a7ce2a1d15`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 04 Jun 2026 18:05:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Jun 2026 18:06:36 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Jun 2026 18:06:37 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:06:39 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Thu, 04 Jun 2026 18:07:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Jun 2026 18:07:05 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:07:05 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 04 Jun 2026 18:07:06 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 04 Jun 2026 18:07:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Jun 2026 18:07:27 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:07:29 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 04 Jun 2026 18:07:30 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 04 Jun 2026 18:07:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e4c7b7fd97730db85cc8cb4e24f79703a02cc0f7f06635851629174bb44d30`  
		Last Modified: Thu, 04 Jun 2026 18:07:54 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc43a027f6b89b4d553ec7037bc17737a9eab9fa5380f0908825cbfb217a017`  
		Last Modified: Thu, 04 Jun 2026 18:07:54 GMT  
		Size: 406.6 KB (406649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ced300ab5391a7c38687e5b984ba803ec69b5c2d126d1a0c0d8047b12facb80`  
		Last Modified: Thu, 04 Jun 2026 18:07:53 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5864470dfe3d7bc2790e072a76be42ed74dd9371700e1f2797e5c16df5fc1ffe`  
		Last Modified: Thu, 04 Jun 2026 18:07:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d68dbbbfa1966dc74d4f6c5148b078e3d54784e374da07e5132546315fc5782`  
		Last Modified: Thu, 04 Jun 2026 18:07:55 GMT  
		Size: 20.0 MB (20022155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e37ac582299df92d3af3260e7064260c6fdcc843b61d6e73145232cf175cd4bb`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fd65284eb90d7f479096f37d4c60da09ad9bf562d7e971aba07a586e999a6eb`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31948ea43a781037597d869411c3f5a1e69fc5db903b69caa4dd5d859cbb6ae2`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc7ef594c12ebe34495352de41cd28c8def8f4919e85538782e3b12b2de75948`  
		Last Modified: Thu, 04 Jun 2026 18:08:08 GMT  
		Size: 23.9 MB (23935081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a668513393fadfacaec2bcb4393cf4b7595ee0a605ddd8e1b64203e2480acc`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fb3b86ccca4649a4f99fe1251e441f7a5b67cae43dd70a7980bde1e485f0e1`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938085c6b5b637765dbd2003897afadb4afc9b7e6f63d291dd41c703b75eaaa5`  
		Last Modified: Thu, 04 Jun 2026 18:07:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1431354d9ea3cf303ed27b340e79bd92000923d7c9e3496a5c9061dc5da0087b`  
		Last Modified: Thu, 04 Jun 2026 18:07:51 GMT  
		Size: 12.1 MB (12119822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:b35a73fee1ad3aa7a8bb2474821202a871462976de8a7b4fac7ef500e8622ab4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178752788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9189320e97dd643f6540d8cd86cb34933d577f8fc027a62f385ca10a1d6027a0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 04 Jun 2026 18:08:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 04 Jun 2026 18:09:33 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 04 Jun 2026 18:09:34 GMT
ENV DOCKER_VERSION=29.5.3
# Thu, 04 Jun 2026 18:09:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.3.zip
# Thu, 04 Jun 2026 18:09:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 04 Jun 2026 18:09:55 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 04 Jun 2026 18:09:56 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 04 Jun 2026 18:09:57 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 04 Jun 2026 18:10:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 04 Jun 2026 18:10:10 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 04 Jun 2026 18:10:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 04 Jun 2026 18:10:11 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 04 Jun 2026 18:10:28 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbff79e4cfab3735574b59b5e2a50633baa6542fe7250c4f43ca083fea2c5af`  
		Last Modified: Thu, 04 Jun 2026 18:10:38 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93530bc92ab3a4ef9a82f1874c29d37af93e500abcbc60321ca972f9b592d2e`  
		Last Modified: Thu, 04 Jun 2026 18:10:38 GMT  
		Size: 495.0 KB (495010 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e7261a1ca07b5e4588a448ac440818069baee0d118739b79e8565269eee85d9`  
		Last Modified: Thu, 04 Jun 2026 18:10:37 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fcb99bb2c1ce89e4a46375ab81667884b07bf0bd88c86b564fa155bb552381c`  
		Last Modified: Thu, 04 Jun 2026 18:10:37 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f5a728dfd160ca777f31bb4d6e0f7f1c45a937017e7b1f86dae21e892ffeaa`  
		Last Modified: Thu, 04 Jun 2026 18:10:39 GMT  
		Size: 19.9 MB (19935454 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402666b63fc10a50f6b1187d82183f5d5a973021a304b293a424b459148134a4`  
		Last Modified: Thu, 04 Jun 2026 18:10:35 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b47d3935f96c96416edc98f216112f60f392730b25fe333adf002dcf0af3ae2`  
		Last Modified: Thu, 04 Jun 2026 18:10:35 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c12df1ec8bad09d0a6a56436f03ddbcc3656e66131f9daccdeb5fa75f48d1e0`  
		Last Modified: Thu, 04 Jun 2026 18:10:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c744fd11bd241c34103fff62813d96e660e5466a0dc71162dc54fba14b64a2`  
		Last Modified: Thu, 04 Jun 2026 18:10:45 GMT  
		Size: 23.9 MB (23855475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c0b7c75d0874d56edf072e72c4cd0e3e125a0289fa69c11914deef3cdf33415`  
		Last Modified: Thu, 04 Jun 2026 18:10:33 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade367201a9ae65b9665f57ef008ca725b73e927b784fb0bffe99f5a529ed95a`  
		Last Modified: Thu, 04 Jun 2026 18:10:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa09b9b4f32bdb4d2b6230bde7f64e1eb3e46fd00ee5c5a8c25392a46c88aa41`  
		Last Modified: Thu, 04 Jun 2026 18:10:33 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cd417e06beb96b26eaf732a76401cba25f99223a4af0f30eceec47d1c722be`  
		Last Modified: Thu, 04 Jun 2026 18:10:35 GMT  
		Size: 12.0 MB (12034362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
