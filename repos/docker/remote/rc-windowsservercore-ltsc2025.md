## `docker:rc-windowsservercore-ltsc2025`

```console
$ docker pull docker@sha256:6603b4bc05dc83a653fa54301aedea46708317c9b1fb348174189ab440d838b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `docker:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull docker@sha256:dc5ac184139b5fbb2cb25b03c6f7b0a63d5ac365a828fce679ad535f115dbc06
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3565605003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b55efcc81d3e26570d627554e9bc88cadc3b4c4a59279cd426eb0762bda93275`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Mon, 01 Sep 2025 22:40:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Sep 2025 22:40:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 01 Sep 2025 22:40:54 GMT
ENV DOCKER_VERSION=28.4.0-rc.1
# Mon, 01 Sep 2025 22:40:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.4.0-rc.1.zip
# Mon, 01 Sep 2025 22:41:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:41:08 GMT
ENV DOCKER_BUILDX_VERSION=0.27.0
# Mon, 01 Sep 2025 22:41:09 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.27.0/buildx-v0.27.0.windows-amd64.exe
# Mon, 01 Sep 2025 22:41:11 GMT
ENV DOCKER_BUILDX_SHA256=1e89de288c9897990220d2ee695b50956d42a3a0792c0b070e9fee7711b9f896
# Mon, 01 Sep 2025 22:41:21 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 01 Sep 2025 22:41:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.39.2
# Mon, 01 Sep 2025 22:41:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.39.2/docker-compose-windows-x86_64.exe
# Mon, 01 Sep 2025 22:41:25 GMT
ENV DOCKER_COMPOSE_SHA256=6580793b1f612150646a9f8d02148c8d226a0033ed6e2e3273c0229b25e2f158
# Mon, 01 Sep 2025 22:41:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cea98d0c1789091563573a3eb308de0fc3b89ad455bfe334cff83ca172ff2af`  
		Last Modified: Mon, 01 Sep 2025 22:45:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa53585ff6eda04b234d1f028a74e25f290b3d5131c25811aacc6194746f0523`  
		Last Modified: Mon, 01 Sep 2025 22:45:07 GMT  
		Size: 390.2 KB (390231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6da70c49e45bf5e577fb060d369c8678d072e3f5b45941aa19188319ae6c05`  
		Last Modified: Mon, 01 Sep 2025 22:45:07 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee9e86337d234e5179f23411c347fcfb4350d58385f06e738b7ea388530aa4e`  
		Last Modified: Mon, 01 Sep 2025 22:45:07 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03e782e3047962de2b15d436a44ed465b8b094804dc364eb23050a66b11731c0`  
		Last Modified: Mon, 01 Sep 2025 22:45:09 GMT  
		Size: 20.8 MB (20814049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44751d38c101fb2385a456af8e9f18e86ef42065a802dc4f2354ae60b91b2542`  
		Last Modified: Mon, 01 Sep 2025 22:45:07 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af5ca0146d5ccdc847a2955fef1bbfd0eb6edf0752877ad3912f43b2d4c5d441`  
		Last Modified: Mon, 01 Sep 2025 22:45:07 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5cb425f207d26085b1b2ce1ad87d949cd393ea547e8cb84d65a5680d7ebce9`  
		Last Modified: Mon, 01 Sep 2025 22:45:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86042b8fb250b49a64282eabee7c01af6baab451824d31ca8d40e1ff9a7b4dc3`  
		Last Modified: Mon, 01 Sep 2025 22:45:09 GMT  
		Size: 23.1 MB (23138819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:549c662638665000dc44ccf112aea1f2c2e40ac493bb8af7f77117bf3017bb69`  
		Last Modified: Mon, 01 Sep 2025 22:45:09 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff5cd07dc829b77b8998f8a6be399c88aca1a5df5f03d110805a1af0198204f`  
		Last Modified: Mon, 01 Sep 2025 22:45:05 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131435291227c8a213b7ea23b589a5dd111bdb91c5025e22cd727b5620e72b65`  
		Last Modified: Mon, 01 Sep 2025 22:45:05 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8e54e8a4f5985ad615c80e5d27365f6bd95939a53266dd3a2e2ac7671908abe`  
		Last Modified: Mon, 01 Sep 2025 22:45:22 GMT  
		Size: 22.4 MB (22419588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
