## `docker:28-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:87ff9f5f1ec7f8d0cf2d85d80bb8822435ca72bf385d689c6d0e8edac653905d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `docker:28-rc-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull docker@sha256:d795fc8194cd50c7b7262a40166c89261c1164cb9c46132d2585c3c7cda3530c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2227543848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98e5c044a74f87fa926d78667ef770793d5970fd9744fedffcec866cad451d7d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Sat, 12 Apr 2025 00:52:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 12 Apr 2025 00:52:40 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 12 Apr 2025 00:52:40 GMT
ENV DOCKER_VERSION=28.1.0-rc.1
# Sat, 12 Apr 2025 00:52:41 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.1.0-rc.1.zip
# Sat, 12 Apr 2025 00:52:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:52:52 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Sat, 12 Apr 2025 00:52:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Sat, 12 Apr 2025 00:52:53 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Sat, 12 Apr 2025 00:53:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 12 Apr 2025 00:53:02 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.0
# Sat, 12 Apr 2025 00:53:03 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.0/docker-compose-windows-x86_64.exe
# Sat, 12 Apr 2025 00:53:03 GMT
ENV DOCKER_COMPOSE_SHA256=bca44d55a7e612c53a80092661dd5db05aefb936e1eccd7ce06fdb02be7df3c3
# Sat, 12 Apr 2025 00:53:12 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8abdb6f82b099e8ff452eaeca9fc5249b213a8309e280c8a338dbbb921e0890f`  
		Last Modified: Sat, 12 Apr 2025 00:53:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05679a57590b05908261d4a952156d93de5f78c263841bf401c0fec5369a28df`  
		Last Modified: Sat, 12 Apr 2025 00:53:21 GMT  
		Size: 343.0 KB (342960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7203f70c27dcc86d5754accefa55500005a70208301c4745960a7a1c2e788a5`  
		Last Modified: Sat, 12 Apr 2025 00:53:20 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61032f1f6d05f123f680206cea1db3ed81188dc3712b86aff454501c7c431776`  
		Last Modified: Sat, 12 Apr 2025 00:53:19 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95c880aecd7a1808bdbb1eb42f51c42b0094f81ab166d52716b6c9aff694e47d`  
		Last Modified: Sat, 12 Apr 2025 00:53:21 GMT  
		Size: 19.9 MB (19874753 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4113a3249a1f710c46ebf5f545bd95fba42456a10cd8c3a467e08499603eabb`  
		Last Modified: Sat, 12 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0403fb18519c614b2094b3bd6fbd9d08a17a40dd65c4950a60f3c50f752570`  
		Last Modified: Sat, 12 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5699130cc7e0a5cb6a750577c87b6f85be557a54431f4adec3355b7024423dc`  
		Last Modified: Sat, 12 Apr 2025 00:53:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0958221aa46dc9274c3b0ed01689c49cf1f7e34015d7e7c273503d7f4c4b11bf`  
		Last Modified: Sat, 12 Apr 2025 00:53:19 GMT  
		Size: 22.8 MB (22759967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d305a1ffced5869ab11321142265499b844c366c020ebacbf4a8598970fb393`  
		Last Modified: Sat, 12 Apr 2025 00:53:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b619282481058ce6f9807e615ac17a24c3600c7f2cdd96e0bdf620f0fa1eae99`  
		Last Modified: Sat, 12 Apr 2025 00:53:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a3b7f242b9d0ff6de6adca6aa9955aa14e21b80a78017211ff318cad70df96`  
		Last Modified: Sat, 12 Apr 2025 00:53:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e6a4883bb0926852a400f48818d6569f8bd70a63b8e687c7c08d636817b579`  
		Last Modified: Sat, 12 Apr 2025 00:53:19 GMT  
		Size: 21.8 MB (21828588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
