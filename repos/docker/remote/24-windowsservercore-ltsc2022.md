## `docker:24-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:6acd73b4d62909faf387090cfedb66aba97e56092f48ca8b9f2cb8924fea8075
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `docker:24-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:0a515f1b778c1b46d16844416c10ced4b5c7232c8f14cc4bd89fc9eccd51f9af
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955300162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:369b8598839a4e9869209c799bd2312b02312e2c34566551309afe6bb42e1bc8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Fri, 26 Jan 2024 01:49:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jan 2024 01:49:57 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 26 Jan 2024 01:49:58 GMT
ENV DOCKER_VERSION=24.0.8
# Fri, 26 Jan 2024 01:49:59 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.8.zip
# Fri, 26 Jan 2024 01:50:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 26 Jan 2024 01:50:13 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Fri, 26 Jan 2024 01:50:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Fri, 26 Jan 2024 01:50:14 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Fri, 26 Jan 2024 01:50:23 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 26 Jan 2024 01:50:23 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.3
# Fri, 26 Jan 2024 01:50:24 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.3/docker-compose-windows-x86_64.exe
# Fri, 26 Jan 2024 01:50:25 GMT
ENV DOCKER_COMPOSE_SHA256=107586a56c0efb53cdd164f8de2c06d9737f4e142c80b6d7d9f5aa2be956425e
# Fri, 26 Jan 2024 01:50:34 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699ca5e21121bf70c2966270f293876d67cd8e09e2c2c955e3a8dad52c582893`  
		Last Modified: Fri, 26 Jan 2024 01:50:43 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac853a4746e94c7596a43138161754cb5b0e38625e336ead5e4e4f1a844f382c`  
		Last Modified: Fri, 26 Jan 2024 01:50:44 GMT  
		Size: 493.4 KB (493423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c329dbf5f8a99c35ecd9041dfd9ae8702d28bcc2ff14b18176c49d783125bd0`  
		Last Modified: Fri, 26 Jan 2024 01:50:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a53845c5b28a80de3cceac57ec71445f1e078a2857078807db89e845f14ceae`  
		Last Modified: Fri, 26 Jan 2024 01:50:42 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5bbf8e2050623ee1f025b58ee7b58fa0e29b9ba925eae01d0afc6dbe94938d3`  
		Last Modified: Fri, 26 Jan 2024 01:50:44 GMT  
		Size: 17.5 MB (17532358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:657418c765d85561ee14f56927457c97d00cea5576c4d99385ff46e64cc165e2`  
		Last Modified: Fri, 26 Jan 2024 01:50:40 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:933f48a370e0a379fb04b59717dbd22c3dac7dece1311e4c199705b79721e1b7`  
		Last Modified: Fri, 26 Jan 2024 01:50:40 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6cb965f7cfea6bb18b6a58bee024077ffd527f731a26132ab830e0fbe1e791`  
		Last Modified: Fri, 26 Jan 2024 01:50:40 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20bc7261299dcd4f96c6144e672687cfb63e161de2ad52d111c1f64f40ef68da`  
		Last Modified: Fri, 26 Jan 2024 01:50:41 GMT  
		Size: 18.0 MB (18018490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82994a159e8edce8c256f32d354af52f6b5a37fad0e3618bdb1b56b1705684c1`  
		Last Modified: Fri, 26 Jan 2024 01:50:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a828499c112a318f9b4764050c72ace6af33e5c8d30a5acbc071f9a0af4ef2df`  
		Last Modified: Fri, 26 Jan 2024 01:50:38 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d248462e2ccfded2de5425d0d32007d97f18b3a78513bd459c36b742d66c25d4`  
		Last Modified: Fri, 26 Jan 2024 01:50:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c5af266e77a0e74cfd46c3f8bc7c17ed53f686aeff97778864336435fad8c4`  
		Last Modified: Fri, 26 Jan 2024 01:50:41 GMT  
		Size: 19.0 MB (19031587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
