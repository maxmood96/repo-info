## `docker:windowsservercore`

```console
$ docker pull docker@sha256:65f3742a5f0d0163bfe66a26296d372a6645ea15464c9e9259d143dd42e95fd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull docker@sha256:8084d47f9c866ffb0fc6c74d818412ff1196f96066e4460f40ddb325112e0dcc
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3460019679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d8eb0a28181dcd66cffe910466b7bc06081957269945180b9e3be0f83af31bd`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:26 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:39:26 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:39:27 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:39:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:39:38 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:39:39 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:39:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:39:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:39:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:39:50 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:39:59 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90663cbdd92914b16d1b360ec39197f6848f810c2e3d5f75368367b755fb29a5`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6859709f79778e74c7ef624e307d1930c0f780d10be536cb85d9893936b1d2`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 364.7 KB (364741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f3f9fb8993e6eddeb12b79a24923159ad4bba9c61def71fa12ee3f22eb949b`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b566c3c24e01288e140412f9834c019e4e2e71145ed6b6b079795f86b97424f2`  
		Last Modified: Wed, 09 Apr 2025 00:40:04 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fc5f946c4df03788d89b893a24b781d0bf21407cc2582ef5194f0eaea08db74`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 19.9 MB (19876882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ff2a3d26ad4275972b61ccdede64c0ddf0788bfa910b1275b74d172e5082198`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f04ad96060e962414395bc1991729228e8ca1e139d5b228efc120a55e2b9cab5`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb45857c62165be6ffbdcee3d0a6ae915dec7440305fc6ebfc274ca67879d0de`  
		Last Modified: Wed, 09 Apr 2025 00:40:02 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946bf5bea56a89ae65bdacd4edde0517f360ff8ebcabd76df02411213a273c01`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.8 MB (22779634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6100d6c301fb149b342ede708f60d3cb8e10a3c1e9e3836c1baf34221724cef0`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8d08118b8b7f3b7ff9643a05fa0fabf35417f346904745264b1b7878d575e1d`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eba8922e187bf58aaae3a9c3e2e9e8cfb6b00b0ad16a4e8cd5a47b91da0443a6`  
		Last Modified: Wed, 09 Apr 2025 00:40:01 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93978eb25ad6c40ce8eccddc334dfe92007d5cc7ed7df32eaef8dd97ec678442`  
		Last Modified: Wed, 09 Apr 2025 00:40:05 GMT  
		Size: 22.3 MB (22307251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull docker@sha256:0fe4c4d0f5c80021c50c85d104ea9454679f65eef396c515473415b2f3551677
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2336245643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2260686200048a8ce26b4461ef2e6b0b73d9ce4353bad23921ebc2a3c91998b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 00:53:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 09 Apr 2025 00:53:44 GMT
ENV DOCKER_VERSION=28.0.4
# Wed, 09 Apr 2025 00:53:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Wed, 09 Apr 2025 00:53:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:53:56 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Wed, 09 Apr 2025 00:53:57 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Wed, 09 Apr 2025 00:54:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 09 Apr 2025 00:54:05 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Wed, 09 Apr 2025 00:54:06 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Wed, 09 Apr 2025 00:54:14 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bd31ce4b72c969f090b09e0d47519bd245635b8a0766cad50a94e5285269e7f`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611d42417bb7b25c9cbe870a1d686b89d1d9756d80d42e4fd6e078d9f81ce4a`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 346.1 KB (346062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb06dc8ecf1b08f1190ad1c0d83e1fdabc1c8d67fc1ac6cb12116132b4f03468`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008480b629bc35e084765059b6f319dc7ff56f6ddd835cde71f710a1d1b3d636`  
		Last Modified: Wed, 09 Apr 2025 00:54:18 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd8c50ac98d04810f7b347835e962e1cc758aeb4ba0ee8a7231139b95c1d2bde`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 19.9 MB (19852659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107085d17762a97b5dc8bd94314f73c5a529607173545e1afaca9a1d379c104d`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271fac6913f53452e4c148e110e15c1cf204cafbed62e7609172534dea68b05f`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58c075328080e6995af18ba0d46caacfb2d481e3bfd03bd1e1feb30c92ef355`  
		Last Modified: Wed, 09 Apr 2025 00:54:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff40e518cab6103cc2dbbed344e68095afb68f480c2690b74900f7a7412e1ae9`  
		Last Modified: Wed, 09 Apr 2025 00:54:19 GMT  
		Size: 22.8 MB (22756339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a62709feb8f58e8269a332f8cb621fcd984c1c3316283ccded16919bf71cda`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6acbdb8f48fcce734907c9a41f60cd59f358e65c812a3a4981f5e8b3276d52e`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1edc9932a94ae1c328f7a4190d5780f481b8890967cbc0e915a092e9a8f0871`  
		Last Modified: Wed, 09 Apr 2025 00:54:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ececc62a636024315de22ccaac302436c36e77452a38b7f08b83dca6b0795455`  
		Last Modified: Wed, 09 Apr 2025 00:54:20 GMT  
		Size: 22.3 MB (22283301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull docker@sha256:a07b73a00a3c52cf508c570e374efc24be0c453d86c9452fcea303ba531ffc8a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216893552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a9a00b1e30a51e5c8dc78b5d38184a68cda33f84d782e8bf6ef53aa9e235d7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Tue, 25 Mar 2025 21:33:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 25 Mar 2025 21:34:13 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 25 Mar 2025 21:34:13 GMT
ENV DOCKER_VERSION=28.0.4
# Tue, 25 Mar 2025 21:34:14 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.0.4.zip
# Tue, 25 Mar 2025 21:34:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:25 GMT
ENV DOCKER_BUILDX_VERSION=0.22.0
# Tue, 25 Mar 2025 21:34:26 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.22.0/buildx-v0.22.0.windows-amd64.exe
# Tue, 25 Mar 2025 21:34:27 GMT
ENV DOCKER_BUILDX_SHA256=446acafb777dc8e8b458a56ce5af3c216260e5170a3e89382b8e4b1dd5853778
# Tue, 25 Mar 2025 21:34:36 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 25 Mar 2025 21:34:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.34.0
# Tue, 25 Mar 2025 21:34:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.34.0/docker-compose-windows-x86_64.exe
# Tue, 25 Mar 2025 21:34:38 GMT
ENV DOCKER_COMPOSE_SHA256=3c6d3548d9dae2939ada367ffdf416aa0e2d282bc6a41d2b49eaa016994c112c
# Tue, 25 Mar 2025 21:34:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a524a0e9cb7afa4d4cd71cd32e949c44f21cba76046ad004d2d6d09870f93ca`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c847dbfeb702fcf37b419ad4ed9aa7e21d43d27bf895a29d8da424b6b58d57dc`  
		Last Modified: Tue, 25 Mar 2025 21:34:57 GMT  
		Size: 340.0 KB (339963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edce44d57bdec9498491ec04581f5193d08ac7cfe87170c1368d3f2456d40268`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c046029f114363dc51b43457767bcb3f623e3c8f32e8ca7f9b2db9d7972f56`  
		Last Modified: Tue, 25 Mar 2025 21:34:56 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23ee9950b1bd1e3a417a9674a6ed4ba90d4b0101a2aad3d904faf071830bd11`  
		Last Modified: Tue, 25 Mar 2025 21:34:58 GMT  
		Size: 19.9 MB (19859748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d5786612fd2d55be281d632baaa5e172f6bd8458061b5ecf3bffedb71d6de9`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15d0a2088c740ff617b174a979824713e0ad78fe077aa205af5340a6aa886e39`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be71a201934e91595d89a5cda2c3f1824c4766cda3ae640a1e8f7dd00e3a33ad`  
		Last Modified: Tue, 25 Mar 2025 21:34:54 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7dd615d0c7c6f688705646fd983a540cca62d8d975b8fd767e83954950ba82d`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.8 MB (22763343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e870735d52bdad39865ea0295c463823531285214d901abdf128dca151e17c5`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2e5d174601f7707cecf5521b4bdf1b1198187a4844a00a623a89d78257bdb1`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b7fcbbabcb3464ee277100b9f6fd1c395109f1ce5de50e92adc5431a6beb04`  
		Last Modified: Tue, 25 Mar 2025 21:34:52 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:176d290ac87077c88ca4ce30853fd4d9020a6eb3dbc3df72610e011d5869d562`  
		Last Modified: Tue, 25 Mar 2025 21:34:55 GMT  
		Size: 22.3 MB (22283549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
