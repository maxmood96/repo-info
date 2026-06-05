## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:987dd80249a616d7c4bf15898ec33774a54c0c538d3aff2280eb2224ef1d7186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

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
