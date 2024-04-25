## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:0ab427c8ed1be5d2ee35b3425697ba8071400ada7b9d119c532537f40f91c386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5696; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.5696; amd64

```console
$ docker pull docker@sha256:8a9cef41267ca7eac2a88051fb9fe25b4cdfa337f0d57cab733d36ad089f331b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2222725353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:356dc984aa416a66fd23d7c4a737392e385bdd7cce687bcd2c372a812fe46bd9`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Thu, 25 Apr 2024 18:53:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Apr 2024 18:55:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 25 Apr 2024 18:55:03 GMT
ENV DOCKER_VERSION=26.1.0
# Thu, 25 Apr 2024 18:55:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.0.zip
# Thu, 25 Apr 2024 18:55:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 25 Apr 2024 18:55:37 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Thu, 25 Apr 2024 18:55:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Thu, 25 Apr 2024 18:55:38 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Thu, 25 Apr 2024 18:56:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 25 Apr 2024 18:56:07 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Thu, 25 Apr 2024 18:56:08 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Thu, 25 Apr 2024 18:56:08 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Thu, 25 Apr 2024 18:56:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c44c068d740a5623182331ca59649ac6db50d6ebd67096cb7550e3cb97bb0d`  
		Last Modified: Thu, 25 Apr 2024 18:56:43 GMT  
		Size: 1.4 KB (1358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47e105b5bcd79128559f0255003b91e287f0374843823489d80fb684e1bb678a`  
		Last Modified: Thu, 25 Apr 2024 18:56:43 GMT  
		Size: 495.2 KB (495182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:249a2a87aff581573ddea1ee96b1e97789afb3df9b4da5cf66674d845674612e`  
		Last Modified: Thu, 25 Apr 2024 18:56:43 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a5a705d5b25498c44514ec2eabfa23f029f69ea5af3a7a745e8f671b14d1ea5`  
		Last Modified: Thu, 25 Apr 2024 18:56:41 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:475b57adbedfcb85a5c35a5a922d19cb82fb7982a17680682e61c64d084b5087`  
		Last Modified: Thu, 25 Apr 2024 18:56:43 GMT  
		Size: 19.2 MB (19234724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0de8d746a55f3c445207e8481f12b780373c419f8aa29d21df817ee875afd8a`  
		Last Modified: Thu, 25 Apr 2024 18:56:41 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c624ce1a768dce6b8bc4ca3fe551934170d1ee70c099e9f61cd0fd1cd67050f7`  
		Last Modified: Thu, 25 Apr 2024 18:56:39 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:029a5660434865aa3368bb893fd98366c9c1f3dd72fdcab7674c2a1e2ce14df2`  
		Last Modified: Thu, 25 Apr 2024 18:56:39 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6e2339a7a8b0fec0a6b68248b20724871767dcf5513572b78aa84a0db2dbb4`  
		Last Modified: Thu, 25 Apr 2024 18:56:40 GMT  
		Size: 18.9 MB (18925040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab0a593235497e488b79e08055e2bbf3dbcc0bdd5237f2470f1ab2934533c9c8`  
		Last Modified: Thu, 25 Apr 2024 18:56:37 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d473c14be7c6c196a10112c0dd95cbd7d141312328a66c0f6f99b090a7eb6bb`  
		Last Modified: Thu, 25 Apr 2024 18:56:37 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1757c0e2a6c0ee8a6be05e349d1ee5d1a6a4ab47ece896834ff6e072433de8a5`  
		Last Modified: Thu, 25 Apr 2024 18:56:37 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a63ca60bcde9534d45e03c011b86a365b86cbeace990b18f4deb00f6ac43b0`  
		Last Modified: Thu, 25 Apr 2024 18:56:40 GMT  
		Size: 19.6 MB (19630174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
