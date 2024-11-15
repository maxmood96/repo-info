## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:b51e0ac26f78e7d49838cf8d3ddc0d3e55629718d4383016740ee5a151a77b46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull docker@sha256:b273c8c547b3978c5cbb5bd835f5f60c33232dacfa14d1882a1f249c20ebc9f8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311176431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15b4f8d2756ffef7c6ec1b862794f607e80d349aa19a48b219c914f1291060e3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:09:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:09:15 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 14 Nov 2024 20:09:16 GMT
ENV DOCKER_VERSION=27.3.1
# Thu, 14 Nov 2024 20:09:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Thu, 14 Nov 2024 20:09:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:09:26 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Thu, 14 Nov 2024 20:09:27 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Thu, 14 Nov 2024 20:09:28 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Thu, 14 Nov 2024 20:09:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 14 Nov 2024 20:09:37 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.3
# Thu, 14 Nov 2024 20:09:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-windows-x86_64.exe
# Thu, 14 Nov 2024 20:09:38 GMT
ENV DOCKER_COMPOSE_SHA256=30be0d2d5df4d032ffeee3f8c5e6dccc2ef1b2911732055778c3584e9e69bb4b
# Thu, 14 Nov 2024 20:09:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a165e881d70522cab9df83fff67de061a3143cd4d34e289b38c53e7aba813b7f`  
		Last Modified: Thu, 14 Nov 2024 20:09:55 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63277f029df5b99a8344f9636e670976707453f025b2556242433753a1849366`  
		Last Modified: Thu, 14 Nov 2024 20:09:55 GMT  
		Size: 365.3 KB (365279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74eca852d971a6f483aa029a97f1ec0161614dbc88ceea4cb8f2c78ac6b189a`  
		Last Modified: Thu, 14 Nov 2024 20:09:53 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce8ecc2e835123f25805e1b695b1504ce2680703aea769a7d7f5d2e381b7e42b`  
		Last Modified: Thu, 14 Nov 2024 20:09:53 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0501ef7b3271b9766371cee044222fa018e6179c46abea87f01f8ef3254278a3`  
		Last Modified: Thu, 14 Nov 2024 20:09:55 GMT  
		Size: 18.9 MB (18893621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c23d6835ed745052417a7d25585fa258109370e2ea3d8b04e1b210c847682e1`  
		Last Modified: Thu, 14 Nov 2024 20:09:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:083f7e83c95a739d40493140b441083086ef55ba2b678895fdcbc8978be6c44d`  
		Last Modified: Thu, 14 Nov 2024 20:09:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14f01bba31359f033310091ded976cc4f7f07c6c3318aff3036559d889896bb3`  
		Last Modified: Thu, 14 Nov 2024 20:09:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a101cdbb0aeb39d93671fa3b1709a4f637dd6325f06bcb5ef0805e08d81eafa`  
		Last Modified: Thu, 14 Nov 2024 20:09:52 GMT  
		Size: 19.4 MB (19420462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2c3e48ff991e8d676b69dd95c48613c82533ac1d36b78f931803fb9770b945`  
		Last Modified: Thu, 14 Nov 2024 20:09:50 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68480c3a195e5238b8c0227b79003c93927323407c689c82afd0774193214f00`  
		Last Modified: Thu, 14 Nov 2024 20:09:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26aa9b92a24f485b6e1debe2b8c87a64757101062e381b922613c1956ffc8626`  
		Last Modified: Thu, 14 Nov 2024 20:09:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e823b652997413c1164126a3f823c8f4851c231ace7c248adc1288aada3053`  
		Last Modified: Thu, 14 Nov 2024 20:09:52 GMT  
		Size: 20.0 MB (20001282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
