## `docker:27-rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:7a98cf41efd849b4c6bb248c0243635c5e9c79cc735aff9823451be4a61ef815
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `docker:27-rc-windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:b815f9d53f9b439a9066c3b3e837d0b3313975710150476c77b72c3ec23c98a3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778688897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856400659c312b95c9a1114378b13e3bd955404754827e9d75271470668dd090`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 17 Sep 2024 23:03:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Sep 2024 23:03:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 17 Sep 2024 23:03:36 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Tue, 17 Sep 2024 23:03:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.1.zip
# Tue, 17 Sep 2024 23:03:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 17 Sep 2024 23:03:52 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 23:03:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 17 Sep 2024 23:03:53 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 17 Sep 2024 23:04:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 17 Sep 2024 23:04:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 23:04:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-windows-x86_64.exe
# Tue, 17 Sep 2024 23:04:12 GMT
ENV DOCKER_COMPOSE_SHA256=4eda107dc1f83a57116c57595d39e6a0ff63e696a52230ea277bd7fa7977c8d7
# Tue, 17 Sep 2024 23:04:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc57543c54b658cb7045bf462d4009ac0421eed94b9e0287719767a286deac4`  
		Last Modified: Tue, 17 Sep 2024 23:04:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec15f36b37bee7ad11ba4fd2539527ac4170d450ec6c5a32a6f14bd7d875218`  
		Last Modified: Tue, 17 Sep 2024 23:04:41 GMT  
		Size: 340.3 KB (340281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bc20c8bbd37453563ca40f2a0357770fc4befb075a045b3cec15d5c7a1d227`  
		Last Modified: Tue, 17 Sep 2024 23:04:40 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cc1cc5dfd529aa58c7bd8e092620a42caf2bb870507609230ea18f2ee7347c`  
		Last Modified: Tue, 17 Sep 2024 23:04:40 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff71b07ac624e67fee061cc55eb7408bbc073439b22928a7bfcdffdbf336fd0b`  
		Last Modified: Tue, 17 Sep 2024 23:04:41 GMT  
		Size: 18.9 MB (18885686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8cbc70e85a5939bcba4e234e2e0fa8a66382f02fee02de276c832921e5e6c8`  
		Last Modified: Tue, 17 Sep 2024 23:04:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5d7b971f0f0ef852c4bd70318b693e52882fe680f49671a2691907c6c70ab4`  
		Last Modified: Tue, 17 Sep 2024 23:04:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440163b90688c11131e903254536f6c94e863d54476509ebab9b6f2948a70f7e`  
		Last Modified: Tue, 17 Sep 2024 23:04:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01140b6cbf792ca3bd3398bbeda5855c83c8250e43ec8533f8bc26b1a557c4c5`  
		Last Modified: Tue, 17 Sep 2024 23:04:39 GMT  
		Size: 19.3 MB (19278262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aca7d79e081c9614739aa541f01884179a27adc1740da9a4a813e7fc33eca3`  
		Last Modified: Tue, 17 Sep 2024 23:04:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c89f5d18bfea5b83ba2e14a7124bac5b432d6af0b574cfe18ef4e30fcf0d2`  
		Last Modified: Tue, 17 Sep 2024 23:04:36 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0fccbd360bb96083e026dd492f90ba8b81b4ef648027883b0ed299cb96c397`  
		Last Modified: Tue, 17 Sep 2024 23:04:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3915161b20e5d9417e376ff41f645931ec8aea303b95333866d4f462b55a1535`  
		Last Modified: Tue, 17 Sep 2024 23:04:39 GMT  
		Size: 19.9 MB (19904666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
