## `docker:26-windowsservercore-1809`

```console
$ docker pull docker@sha256:26314cfd499253170cdfc441a6930294fffa2e83d9bee3658dcacf266dfc0d5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `docker:26-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull docker@sha256:78f8a57b236118968510980910fd8d0fa5201209a938133c91c831871b8a2908
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2238101254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32fc69beb33538cf80d78a59e2efdce7fb6b16cf6c61bcd49bca4af37b832c68`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 21:59:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 22:00:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 29 May 2024 22:00:51 GMT
ENV DOCKER_VERSION=26.1.3
# Wed, 29 May 2024 22:00:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-26.1.3.zip
# Wed, 29 May 2024 22:01:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 29 May 2024 22:01:23 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 29 May 2024 22:01:24 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 29 May 2024 22:01:25 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 29 May 2024 22:01:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 29 May 2024 22:01:56 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.1
# Wed, 29 May 2024 22:01:56 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.1/docker-compose-windows-x86_64.exe
# Wed, 29 May 2024 22:01:57 GMT
ENV DOCKER_COMPOSE_SHA256=354e903701dbd3e7ee3c4259de928367776864bb850efe677d129202638843db
# Wed, 29 May 2024 22:02:19 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53e3107afe19a65f43ef233c5bcb15d4ed1273412e73ef901d82eed55f900c60`  
		Last Modified: Wed, 29 May 2024 22:02:25 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f61efabcadc0f394b043e7aafcace1e4251caf99683fac2c82abae6751fc1bb`  
		Last Modified: Wed, 29 May 2024 22:02:25 GMT  
		Size: 512.4 KB (512406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28da0e7eee3fd7f32e7a7ff481f177443481b83977fa2ab9296b983c1cb3828d`  
		Last Modified: Wed, 29 May 2024 22:02:24 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705933e71cc9fe32fdfdc130a2a28c646c1a5acff3dfeb5d22d6e43ee9307c7b`  
		Last Modified: Wed, 29 May 2024 22:02:24 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d79a114c2f83d6a5dcca71c4108e330419d308eac19f36743cb7a49dc4b2d9`  
		Last Modified: Wed, 29 May 2024 22:02:27 GMT  
		Size: 19.3 MB (19264137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30ac500427ccbf167ddba180cc62984b0ca99f42bb316062d872f3e8ca26479`  
		Last Modified: Wed, 29 May 2024 22:02:23 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3df7926d91fb377d3919bf095c7f4075d68af3e568b40c91b17037a52007a6c`  
		Last Modified: Wed, 29 May 2024 22:02:23 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d4c6bd250877848c1a746e4c2c1741f7bff2063dab05169c37765359b09ec3e`  
		Last Modified: Wed, 29 May 2024 22:02:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1904db0a23aa5a175a7077378950b0a75cde7862cadec00bdde285ecd835e202`  
		Last Modified: Wed, 29 May 2024 22:02:24 GMT  
		Size: 19.0 MB (18950171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a38b1624679a6e9660f91245c6fe4b54a87dcb58789b62bce16884e865734cf`  
		Last Modified: Wed, 29 May 2024 22:02:22 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67828b497ea701adcc0cc6b6f0cdb989f521733d0fdd5a4d2f470c1ff466eefa`  
		Last Modified: Wed, 29 May 2024 22:02:22 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64106bdf8bcc56d64cf867e81bce651bf7d97f8e44c9cb4eface9a9a86d10d9`  
		Last Modified: Wed, 29 May 2024 22:02:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27eda69818df766e88ace87559955bd05a1cb027a656e5347ea9a67b9012eec`  
		Last Modified: Wed, 29 May 2024 22:02:25 GMT  
		Size: 19.7 MB (19651420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
