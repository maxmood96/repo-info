## `docker:27-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:93a477823cd309ef79290a399959703c76773e5155000892de6af06bd8d4e538
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `docker:27-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:405e693bc29383dfaf6e973687bf5f939b5973b89f78117284d3dce8b1cfe8fe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520629697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8de568273b2d55aa406e8e3df3e87e953b908d111d1585d0f1074cd395601f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 12 Sep 2024 23:06:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 23:06:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Sep 2024 23:06:46 GMT
ENV DOCKER_VERSION=27.2.1
# Thu, 12 Sep 2024 23:06:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Thu, 12 Sep 2024 23:07:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Sep 2024 23:07:01 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Thu, 12 Sep 2024 23:07:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Thu, 12 Sep 2024 23:07:03 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Thu, 12 Sep 2024 23:07:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Sep 2024 23:07:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Thu, 12 Sep 2024 23:07:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-windows-x86_64.exe
# Thu, 12 Sep 2024 23:07:19 GMT
ENV DOCKER_COMPOSE_SHA256=8603f4e6936e752793f7edf3f45ed67cb1b8ed8c7b1dabc5721384299bfebd7f
# Thu, 12 Sep 2024 23:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2b76973ba80014c7e4c1d928a1a48b8a9eb70d4d0be30e3ec940c03d99be3a`  
		Last Modified: Thu, 12 Sep 2024 23:07:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c52885658aa962688b752d11811d45d43bef445e75e57fc5a14064558ded0f5`  
		Last Modified: Thu, 12 Sep 2024 23:07:37 GMT  
		Size: 341.9 KB (341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead9e67a940a471a586a4516a804edc4d3cf82949e805c8b25d5ee6818058921`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad2af61af8b64812005cebcb0773a9ea01a7e309030ece195e82976fa233d73`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9415c1343cdbd788dd09414664ecfc4610eceb380cd195e9d1307b2f2b356742`  
		Last Modified: Thu, 12 Sep 2024 23:07:37 GMT  
		Size: 18.9 MB (18913517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd41bc0b9bfd5008aef5f2a2b352f03fd981a96074fc38e8b6834015359dc74a`  
		Last Modified: Thu, 12 Sep 2024 23:07:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139be8568ce6e33024c303ff04a8e5df2cf8f66d875c3769e951f159df929df2`  
		Last Modified: Thu, 12 Sep 2024 23:07:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792668dc6d874e1bb541d77edfd6c8d9129743ed28028598747d3120c9aca0f7`  
		Last Modified: Thu, 12 Sep 2024 23:07:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d61431112e35dd7bb61efb83c7c2ec2c03e3160c8bc0643390cd0a221864427`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 19.3 MB (19269180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff28526aa2b8e567eb9d2601ade782df3d2e461c57a22bb4c5b3914c61d4b29`  
		Last Modified: Thu, 12 Sep 2024 23:07:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a400e047f39e5033ae2833ffd362aa3b77cdec0662edbb526c04ffa428fbc`  
		Last Modified: Thu, 12 Sep 2024 23:07:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d07564c0fbdea5d9bcf44bd7c7519c83b87d1b9f57fa92afa064b86f5a7cd7`  
		Last Modified: Thu, 12 Sep 2024 23:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e4c4be24a83623531a3ca568bd7bad0fdc2b750d4c5d072ba9fa01cb0d9712`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 19.9 MB (19901121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
