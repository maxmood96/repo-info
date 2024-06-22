## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:30f1ee34f9700504bcf0628039c49ccbdbb104825a3dd3825c131c3378459ed9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2529; amd64
	-	windows version 10.0.17763.5936; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2529; amd64

```console
$ docker pull docker@sha256:ee319f5920a4e4042e0d56e7c61801ea64f6c9e25814d6c88c00c8cf10706e5c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2174698038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ac18681edea4873c522bec9f9645cd8f7323b8acb8532e265f00482bb213e0`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 19 Jun 2024 19:58:05 GMT
RUN Install update 10.0.20348.2529
# Sat, 22 Jun 2024 00:01:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 22 Jun 2024 00:01:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 22 Jun 2024 00:01:51 GMT
ENV DOCKER_VERSION=24.0.9
# Sat, 22 Jun 2024 00:01:51 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Sat, 22 Jun 2024 00:01:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:02:00 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Sat, 22 Jun 2024 00:02:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Sat, 22 Jun 2024 00:02:01 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Sat, 22 Jun 2024 00:02:09 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 22 Jun 2024 00:02:10 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Sat, 22 Jun 2024 00:02:10 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-windows-x86_64.exe
# Sat, 22 Jun 2024 00:02:11 GMT
ENV DOCKER_COMPOSE_SHA256=b9878421deeff63bb4685a0ee502fc737429123f68ee40de326cdc9fab800c1d
# Sat, 22 Jun 2024 00:02:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb373ec9afdfc5f09b9380d981e0c61f9c7b48537b887135c7c66810086e705e`  
		Last Modified: Fri, 21 Jun 2024 00:27:54 GMT  
		Size: 729.6 MB (729591500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67700cc2cd05955a53a15c1090c378d4c829d88e238cc8d9dc45d757e5586570`  
		Last Modified: Sat, 22 Jun 2024 00:02:27 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e3ef3ddb22afbb3cebb734fafd51cf1c0b398825eb5096447ce0d903e2d634`  
		Last Modified: Sat, 22 Jun 2024 00:02:27 GMT  
		Size: 345.4 KB (345390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2a734f24b641ad18344ab22190e8c63d4b51ea39dacb9f59e1a2ecc6a2ea28`  
		Last Modified: Sat, 22 Jun 2024 00:02:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97523b39e8623ba1fec686f5d0bbef68ce6fb401d2f2d8b5145ecb6e9f68616b`  
		Last Modified: Sat, 22 Jun 2024 00:02:26 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24acb9509111bc3fbc2a574b1b966ad3f38a48da00f74cc905554f47afa55fc5`  
		Last Modified: Sat, 22 Jun 2024 00:02:27 GMT  
		Size: 17.5 MB (17520621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9deb3dac7ffe7ba2782cbb2d7e7395602e16e5e75fb16c74143974d95913b4c9`  
		Last Modified: Sat, 22 Jun 2024 00:02:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc90afb657a1f775604e3abfae04eeec640a3d6a8e93f8b18c5653b72306af8`  
		Last Modified: Sat, 22 Jun 2024 00:02:24 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df3207528a6ff38e328c16148168a724b86a3a2bcf57c2df9e4936e9ae4039fc`  
		Last Modified: Sat, 22 Jun 2024 00:02:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70b5b40a5fd3ba21c2a810766b6e6c3d364d6e9be4b649d078a6b5d8e877cbc`  
		Last Modified: Sat, 22 Jun 2024 00:02:25 GMT  
		Size: 19.0 MB (19010826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868beddda9b215734d190382f16fa45edbec3c57cc5b4ff3d6f6fb041464f5f2`  
		Last Modified: Sat, 22 Jun 2024 00:02:22 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86211ebfc4a0e96e9ce57a4e2fe86823bb82fcb817986f30be95eb0edd08157b`  
		Last Modified: Sat, 22 Jun 2024 00:02:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17accc06ca83ee5c0b60123d919bb64b40f555639e02c15dac245951cc40b6b9`  
		Last Modified: Sat, 22 Jun 2024 00:02:22 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a41df406c65e64cf5f5f969438529bba162ad6d037f2779818c7a0ff7c9ab9a7`  
		Last Modified: Sat, 22 Jun 2024 00:02:25 GMT  
		Size: 19.6 MB (19619345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.5936; amd64

```console
$ docker pull docker@sha256:9687ebc0f5f35492807524de258ac53122ee9cbafc0fdabbde2564171395d684
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2277382056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50c55efdb0f1becd5975dccaec840728b4661bb43dd5f5fd9bb3a189a6c76f8`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jun 2024 11:19:50 GMT
RUN Install update 10.0.17763.5936
# Fri, 21 Jun 2024 00:11:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 21 Jun 2024 00:12:23 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 21 Jun 2024 00:12:23 GMT
ENV DOCKER_VERSION=24.0.9
# Fri, 21 Jun 2024 00:12:24 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Fri, 21 Jun 2024 00:12:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 00:12:47 GMT
ENV DOCKER_BUILDX_VERSION=0.15.1
# Fri, 21 Jun 2024 00:12:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.15.1/buildx-v0.15.1.windows-amd64.exe
# Fri, 21 Jun 2024 00:12:48 GMT
ENV DOCKER_BUILDX_SHA256=d28cff3df9fdbb37aa7434edb09d8befe5e90e5ef5887807569b694f25bebd33
# Fri, 21 Jun 2024 00:13:08 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 21 Jun 2024 00:13:08 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.2
# Fri, 21 Jun 2024 00:13:09 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.2/docker-compose-windows-x86_64.exe
# Fri, 21 Jun 2024 00:13:09 GMT
ENV DOCKER_COMPOSE_SHA256=b9878421deeff63bb4685a0ee502fc737429123f68ee40de326cdc9fab800c1d
# Fri, 21 Jun 2024 00:13:29 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56a5fd77f8cb6921d3e283f98213bf8c163d3502a75b4a8e4a809a15654f7d1a`  
		Last Modified: Tue, 11 Jun 2024 17:22:31 GMT  
		Size: 570.1 MB (570060810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ac458a31fb6f4254a50255cdb0f3fe4881f4527147b967106f1237923288fd9`  
		Last Modified: Fri, 21 Jun 2024 00:13:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abd1293662bf62ab3fc68ee7c18e0399da1abe3f7c7b35a5655d9fd4f7d27cff`  
		Last Modified: Fri, 21 Jun 2024 00:13:35 GMT  
		Size: 493.2 KB (493220 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f2e56ffac20ff6ae19da3d7c75c6f2becc27e088ccf8c1a52a62f6f7de2633`  
		Last Modified: Fri, 21 Jun 2024 00:13:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37a499bbd2d1fec3c4827592bebe4a80e831f1e0a6b53b88fe110ee97c1ab06`  
		Last Modified: Fri, 21 Jun 2024 00:13:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d45db3fdcdad8719d44df349cc6df1d962d769edd984c8800b7aba229a4a80`  
		Last Modified: Fri, 21 Jun 2024 00:13:35 GMT  
		Size: 17.5 MB (17538373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1034ccd0bcffa58fd517cd75a541c474483f623c5d917154e74a92c05bc404`  
		Last Modified: Fri, 21 Jun 2024 00:13:33 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f991e110d0b77444d16cf9454c93736d3bc646dc2b5ab8b9f709aa6ed1364309`  
		Last Modified: Fri, 21 Jun 2024 00:13:32 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d2d67ec917a644fc96f68ff94cfad46b091915639aff173d2ed37e8f291e61`  
		Last Modified: Fri, 21 Jun 2024 00:13:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07387ec52cc0429e6c05d437bd56095f5bb6c61a86337879161aee69bc1b599d`  
		Last Modified: Fri, 21 Jun 2024 00:13:35 GMT  
		Size: 19.0 MB (19027748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5973e7d5788cded79b39760e6ece483eddce0663678b574534323cef3d27ff6`  
		Last Modified: Fri, 21 Jun 2024 00:13:32 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8531f3e7ea682c89c9814436b45b3035a07e192a38bc1d6e7b11b39f52f5f24b`  
		Last Modified: Fri, 21 Jun 2024 00:13:31 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe98308c554d247c336a1962e0087021e9e711a30ba0191f31a1b4934ac2cd58`  
		Last Modified: Fri, 21 Jun 2024 00:13:31 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebb458e25741ebc28eabe89229758f49deaa8d9f85772ca665b660374cecc2f`  
		Last Modified: Fri, 21 Jun 2024 00:13:34 GMT  
		Size: 19.6 MB (19629836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
