## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d4994b493ff7c3698a0056280cb6a00b5a702d024527f2bcbe625267f576cb7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull docker@sha256:ed90491e665aa421332710c806ff29bf8714b5c3942d67d568b5408e929bbc0d
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199536001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e77764fd388c2c96d489a20821df64b0716ebe01ca57cb4cb80c5ef27d0ca3`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:17:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:17:41 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Aug 2024 20:17:41 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 20:17:42 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Tue, 13 Aug 2024 20:17:53 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:17:54 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 20:17:54 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Tue, 13 Aug 2024 20:17:55 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Tue, 13 Aug 2024 20:18:02 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:18:03 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 20:18:04 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Tue, 13 Aug 2024 20:18:05 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Tue, 13 Aug 2024 20:18:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:678bfa59c051f27e56bb26bd0a77ecb78d9fee8409a99d234847b0675b289abf`  
		Last Modified: Tue, 13 Aug 2024 20:18:20 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df7b6cfaa2e52f6fd24b2bbde5601bd5802b4e2df2c7971be9540465e36bef2`  
		Last Modified: Tue, 13 Aug 2024 20:18:20 GMT  
		Size: 372.3 KB (372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1be5b1ba8867140c29651ccb75e946d62636c62f7035c5170ab0cbd6e88f22`  
		Last Modified: Tue, 13 Aug 2024 20:18:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582435ae3e46a7908b38e394e61176b071b56c381b84fad3acd4615a469460a4`  
		Last Modified: Tue, 13 Aug 2024 20:18:19 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eafa03b9c637ec066b88251d571fa59c903bfdfc70c84d594fa98485e978f885`  
		Last Modified: Tue, 13 Aug 2024 20:18:20 GMT  
		Size: 18.4 MB (18421347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8e2020cb8eae93bc441a9a497fe5c05da4199a335eec6f257137a5791e79abf`  
		Last Modified: Tue, 13 Aug 2024 20:18:17 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84541ec70ae578584f7041bdcc282bea5f8eec8005d35c0871494d14f1cafca`  
		Last Modified: Tue, 13 Aug 2024 20:18:17 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0584e13659b2fdb1161ac09201ec8d6463ee95307a7f45dcf9dd053090746eb4`  
		Last Modified: Tue, 13 Aug 2024 20:18:17 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdc2d518eaf69a371269f2e848175ac9ff5c2f1e4ade33a6ce0f66776bb2be13`  
		Last Modified: Tue, 13 Aug 2024 20:18:19 GMT  
		Size: 19.3 MB (19265050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f585bf8c3fa1a60e5c6e895f6118ea86f1f5caf0d7053fd533f1befcf260aede`  
		Last Modified: Tue, 13 Aug 2024 20:18:16 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71d6e8648bd7108992317c355f03fae630cbf69362ce66b399defe17a015c110`  
		Last Modified: Tue, 13 Aug 2024 20:18:16 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eee15e4cb3dcd127528c340dddf72af54df4c7a39e5dc47dd7aaa1b19f26f5a`  
		Last Modified: Tue, 13 Aug 2024 20:18:16 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6465f309b12f0efb14118f10624c6ce45e8d911ca828ad78c35324a6573e4bd5`  
		Last Modified: Tue, 13 Aug 2024 20:18:19 GMT  
		Size: 19.7 MB (19700568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
