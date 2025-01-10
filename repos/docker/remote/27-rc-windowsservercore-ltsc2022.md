## `docker:27-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:f0ff9dce9c42381541507120fda9a4e6ffae9e7fd7ccf1db0cca0c74a544070d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `docker:27-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull docker@sha256:34c8def198551f1459d069bd5d4d37df4100afe874339a550015e35c5280c9d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313129839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c879b100b69e4588217fec80ac9427eb48b8583df5a57875fa7acff211cf3846`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Thu, 09 Jan 2025 22:28:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 09 Jan 2025 22:30:16 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 09 Jan 2025 22:30:17 GMT
ENV DOCKER_VERSION=27.5.0-rc.2
# Thu, 09 Jan 2025 22:30:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.5.0-rc.2.zip
# Thu, 09 Jan 2025 22:30:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 09 Jan 2025 22:30:37 GMT
ENV DOCKER_BUILDX_VERSION=0.19.3
# Thu, 09 Jan 2025 22:30:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.3/buildx-v0.19.3.windows-amd64.exe
# Thu, 09 Jan 2025 22:30:38 GMT
ENV DOCKER_BUILDX_SHA256=fc24c33d547764ffc67ed430f5561c4d1bcbbee73df47648668331fa1cc2f289
# Thu, 09 Jan 2025 22:30:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 09 Jan 2025 22:30:47 GMT
ENV DOCKER_COMPOSE_VERSION=2.32.2
# Thu, 09 Jan 2025 22:30:48 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.32.2/docker-compose-windows-x86_64.exe
# Thu, 09 Jan 2025 22:30:48 GMT
ENV DOCKER_COMPOSE_SHA256=f384ad29e5187745cad4c18a14ddafd5e7a748c68b5bd991599b1756e36d3bec
# Thu, 09 Jan 2025 22:30:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e64f3ca98ebbeaabbe9caa8a22cf59bc40d9d102d2526d1049bd68a910921bf9`  
		Last Modified: Thu, 09 Jan 2025 22:31:03 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c556be6783cdbb2c773a11684d233d0b303cceca2409d251ca495028eb4e8b32`  
		Last Modified: Thu, 09 Jan 2025 22:31:03 GMT  
		Size: 357.0 KB (356971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db5363d85636ed44a6ab46f57b9f37cd884f03ec2ce37d0e33cd96233b9138`  
		Last Modified: Thu, 09 Jan 2025 22:31:02 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b435965c81c2e8fb61ce8a0eadf77cfb0e2f9886595430f0033e80e767731f3c`  
		Last Modified: Thu, 09 Jan 2025 22:31:02 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:159da7e211e53c5b7ddeec749a6c40bc4434d55aa46675a838d8e577c3dac69f`  
		Last Modified: Thu, 09 Jan 2025 22:31:03 GMT  
		Size: 19.1 MB (19131765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1584497e6e0be075b115c53cc08d3ac3095f7ab38fdfc856d8cb48449bb7e060`  
		Last Modified: Thu, 09 Jan 2025 22:31:01 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0348525302a5482ba9b0d399d7eacc24af94672045c97ecb89568235ded2564b`  
		Last Modified: Thu, 09 Jan 2025 22:31:01 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3147b65b25122a7c3e76ab0b163ff239af806851dbe1337f4cceccfe784799f`  
		Last Modified: Thu, 09 Jan 2025 22:31:01 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9f472ac9bf23724607ca28bcc8bf1acc04896b2d5e40f90e05234e1dfef84e0`  
		Last Modified: Thu, 09 Jan 2025 22:31:03 GMT  
		Size: 19.6 MB (19615417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa14a61e024eeab3914a555cf693f8281b9bdb37f9ddb1cc3148658be9d36f7`  
		Last Modified: Thu, 09 Jan 2025 22:31:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ee6431a575ea313a3aca6d1c013e02216a2a470e4eae7992499d19398ae8ab`  
		Last Modified: Thu, 09 Jan 2025 22:31:00 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625c47e3aecbfdba39fc9ee46db788bcfb5edb0fa800215f469c44defd7d81db`  
		Last Modified: Thu, 09 Jan 2025 22:31:00 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e92dc6bab1ddd4745640a6d67475207ee6ca87cb4ba8efe6494172cba722a6b`  
		Last Modified: Thu, 09 Jan 2025 22:31:03 GMT  
		Size: 20.1 MB (20140505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
