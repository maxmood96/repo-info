## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:76a2595299d5d831461bbff176d00c8005cc1b58a48fe70127d90155b250253f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32860; amd64

```console
$ docker pull docker@sha256:189f1d53b9d0831a7663f55ac4dfcfe317baa879af86a90a44e1c83e9f9fbf6a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2262683896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c993dcdab4e74415b546e3486a219f555369a5b9db18c96ed98e36915f6572`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Thu, 21 May 2026 23:13:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:15:10 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:15:11 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:15:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:15:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:38 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:15:39 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:15:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:15:58 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:15:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:16:00 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:16:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c26092efbc05ba0447d81394df46314e3b86ab224685126b2d6dfd994d4dc11`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ade171b063bb36658cc0d1e2c9c6cb333ea25a3ad1e4129615adf825b64a46`  
		Last Modified: Thu, 21 May 2026 23:16:20 GMT  
		Size: 406.4 KB (406376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78577312456309bc4fe740995c1663317c15ecc17bcedded51adf9a9982366ca`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee76c01ce753f169a4b6e55abafceb2769603948efcc72907de3e6aeb33cce42`  
		Last Modified: Thu, 21 May 2026 23:16:18 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc27681d28a3246dcf30c481b3852d6dbdc170d9cf5b284e019a90ade4d9cee8`  
		Last Modified: Thu, 21 May 2026 23:16:21 GMT  
		Size: 20.3 MB (20271957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c75db7b4635a1d76c37b80319e3dd1bdff20dd7ef77265097ecdb2861b340b99`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d982239ff1380cf0818ab9cc60083eac7f15cd44054f9f67433be9035d8a31`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c096a591d4ea5f003d7be2a803cf5e81d42655e886b4df3ea31db5ab4f1289f`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f795f325466c0a11f5a6c88330d8ab8b3fcad025e8fc95a56b3cc2d15f7884bb`  
		Last Modified: Thu, 21 May 2026 23:16:32 GMT  
		Size: 23.9 MB (23933638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b824c613a9ba32b1fcec65a639d38947346d62eddad555e9a7e295010f6937d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62db1e13ba58abbe1229ca941f68bceaa49a84ce729b12c843e3c1914052407d`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7286144ed984b89e44b176cd42f189f5d30dc6bdd1357032bbb549bb0c96975`  
		Last Modified: Thu, 21 May 2026 23:16:15 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8922b65b3736da43bcb9ea86b5abf5ea19ee56a9c642200696decef2214beb0`  
		Last Modified: Thu, 21 May 2026 23:16:17 GMT  
		Size: 12.1 MB (12118551 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.5139; amd64

```console
$ docker pull docker@sha256:fecc0a5137c67dad8b14e94db06043867e6b74bb784840642f699cfd8d9abe16
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2179150500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52496b21f2e24bac1a6601b61b2de6417374b43f89a6f9cfd8eefedf65fdd4a7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Thu, 21 May 2026 23:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 21 May 2026 23:38:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 21 May 2026 23:38:15 GMT
ENV DOCKER_VERSION=29.5.2
# Thu, 21 May 2026 23:38:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.5.2.zip
# Thu, 21 May 2026 23:38:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:38:44 GMT
ENV DOCKER_BUILDX_VERSION=0.34.1
# Thu, 21 May 2026 23:38:45 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.34.1/buildx-v0.34.1.windows-amd64.exe
# Thu, 21 May 2026 23:38:46 GMT
ENV DOCKER_BUILDX_SHA256=41e1b3fff6541d5f5febb18ff4c9108bec30afd7bf9133b82783735c2078eac1
# Thu, 21 May 2026 23:39:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 21 May 2026 23:39:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.4
# Thu, 21 May 2026 23:39:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.4/docker-compose-windows-x86_64.exe
# Thu, 21 May 2026 23:39:13 GMT
ENV DOCKER_COMPOSE_SHA256=e1a8faff28c7433635201a2222171b727f33ecdb0ed367e54d162d00432f39aa
# Thu, 21 May 2026 23:39:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17fd8e1d39e88259a0e6383034d2a7ad6d90356547cec5bbbf94f3a3e0afc763`  
		Last Modified: Thu, 21 May 2026 23:39:40 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1756702264897e3d6bb006dbce5e5260ae7bc8fa54384b6a031c460ac01476e`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 505.7 KB (505666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da4ab93ed88956a88f0eb095aaf8977d5b9bbba18d08b7757eb1ccff28e80d2a`  
		Last Modified: Thu, 21 May 2026 23:39:39 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c2528cc62d1c88f5003aa2f0b62055544c66be0ec0d65cf6a8550455e0747`  
		Last Modified: Thu, 21 May 2026 23:39:38 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e531632899bf060a3ff8e9b29f0c3c81b857c0b311b97f241e35d94ffe66d3cb`  
		Last Modified: Thu, 21 May 2026 23:39:41 GMT  
		Size: 20.2 MB (20231436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34d5b3db47edaa5e44e34cad2ba31b4be5c5b6c483cef5a09b33460c4747302`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751d900578d8658aa1097acdfcd5f97aff829261a5e29a8f16b2f40effa4f532`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7eeb843d181536cfa4d4d838d626f63e191094c2468d26f3d0330a50f2b526c4`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b58742ef314900bc96dda8fc677f8a1b98faf7970eb6fa39992b3a0150a7d36`  
		Last Modified: Thu, 21 May 2026 23:39:51 GMT  
		Size: 23.9 MB (23901391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:435a34db22345529d906d3448943e90cfc37ae51e15ea8ec70cd87e01c5b16d8`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1f19e0160f0c9a3c97ced5e763b905a949f0f5af2882f68638e276a43a62af`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60db139392fbadfa06ac3c12862fab33f209dc6d2a7f076d7d0b52eec402dc3b`  
		Last Modified: Thu, 21 May 2026 23:39:35 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ddde0e1dba54298e42dcefa7d09742c8714bba4bc7d5a59eb1950f87975208`  
		Last Modified: Thu, 21 May 2026 23:39:37 GMT  
		Size: 12.1 MB (12079670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
