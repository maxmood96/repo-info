## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:06de7549d81005fa61fd19c3eb74b49e8c82c83077a9aaadf8be723dde037474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull docker@sha256:29b934118f6b68294cfa9ba43c01100c22565489673ce1ec5808ad6a6c84b505
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2303056951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a91814b94758873131e4e6ebddc8814484a99cd769a41865bf69cc0e75159e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:17:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:19:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 13 Aug 2024 20:19:11 GMT
ENV DOCKER_VERSION=27.1.2
# Tue, 13 Aug 2024 20:19:11 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.2.zip
# Tue, 13 Aug 2024 20:19:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:19:37 GMT
ENV DOCKER_BUILDX_VERSION=0.16.2
# Tue, 13 Aug 2024 20:19:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.2/buildx-v0.16.2.windows-amd64.exe
# Tue, 13 Aug 2024 20:19:39 GMT
ENV DOCKER_BUILDX_SHA256=0ee1234dc4bec883f9407211ae386052c45d13cf9052329f8aece8358cff5e9c
# Tue, 13 Aug 2024 20:19:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 13 Aug 2024 20:20:00 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Tue, 13 Aug 2024 20:20:01 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Tue, 13 Aug 2024 20:20:02 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Tue, 13 Aug 2024 20:20:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf924aaf03e00e1295b566bc932b1f3a1c2f1965653e9a9836691a6f479ffc68`  
		Last Modified: Tue, 13 Aug 2024 20:20:33 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b659890f3946927924800b365d4f3de02960f616490d65d7627b63b2fe88fc`  
		Last Modified: Tue, 13 Aug 2024 20:20:33 GMT  
		Size: 487.8 KB (487768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf506fa16bf760dd82e8185290afb16252197220fa04e00a7fb12250ed5f88f`  
		Last Modified: Tue, 13 Aug 2024 20:20:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584db5902b037ba1e470c57604ce970ffbfee65b585d31af64730cdf78378acc`  
		Last Modified: Tue, 13 Aug 2024 20:20:31 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:551e1940ac52181f873eb5472af0d7d7455bdbf9d28676ff4018645037afa4c6`  
		Last Modified: Tue, 13 Aug 2024 20:20:33 GMT  
		Size: 18.4 MB (18413507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918295343d81659466361ba96225e0fd7d0a884b650b5ad4c6f9f4ace80b1035`  
		Last Modified: Tue, 13 Aug 2024 20:20:29 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c13f66d65d9400c5cd8aa9dc82f8a58088e4c7cdd5a60df6d71f439685945ed`  
		Last Modified: Tue, 13 Aug 2024 20:20:29 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35787093b44473131054534fb327f636017d799ffa3a9f13538ed9f500994ecf`  
		Last Modified: Tue, 13 Aug 2024 20:20:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8896fc92f48da4085ec712d6ffae0373e3c3c699edbb4d3f5e7e2ce9ea9a6c3e`  
		Last Modified: Tue, 13 Aug 2024 20:20:30 GMT  
		Size: 19.3 MB (19255554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff013dccaffba9b700babd1de218cc304a4e41c3b71980b7d52cafe1e8a5b09e`  
		Last Modified: Tue, 13 Aug 2024 20:20:28 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55903d379975480b4eadef9f1be30ea23af85b212fbac504977551fe41cb0549`  
		Last Modified: Tue, 13 Aug 2024 20:20:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c275d16a94dfec5a348681a8762a1cb9f7accd2daa323a0c7c66d4e8659d0501`  
		Last Modified: Tue, 13 Aug 2024 20:20:28 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b5029b12c6a3858bd942adf86b4e7032a7749b8da14dc4874a48d0fed5f203e`  
		Last Modified: Tue, 13 Aug 2024 20:20:30 GMT  
		Size: 19.7 MB (19685211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
