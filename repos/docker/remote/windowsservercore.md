## `docker:windowsservercore`

```console
$ docker pull docker@sha256:32a64e25140b6c0f549d62bc3d39a8af19d8927243c86559791f6c2591939433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `docker:windowsservercore` - windows version 10.0.20348.2227; amd64

```console
$ docker pull docker@sha256:4fbc2286636b60cca286f1b837c953381d69eb2c3bf7c1dfdfbc297e20bddc00
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1955323622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ed19a1ab320dc00fecf73435a1ad35cd409f102a599e46429e8047afb4694e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Sat, 13 Jan 2024 02:03:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 02:03:16 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 13 Jan 2024 02:03:16 GMT
ENV DOCKER_VERSION=24.0.7
# Sat, 13 Jan 2024 02:03:17 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Sat, 13 Jan 2024 02:03:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:03:27 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 02:03:27 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Sat, 13 Jan 2024 02:03:28 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Sat, 13 Jan 2024 02:03:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:03:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 02:03:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-windows-x86_64.exe
# Sat, 13 Jan 2024 02:03:37 GMT
ENV DOCKER_COMPOSE_SHA256=4e0e387d67a65d92e3a7aca085f86b4b46ed5bd7a475f81921629e1d097178f0
# Sat, 13 Jan 2024 02:03:45 GMT
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
	-	`sha256:a764111b60b54df97a515cc896483140125ed65824ca0f6c15bd8427e7d5b776`  
		Last Modified: Sat, 13 Jan 2024 02:03:53 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa697cf34903a3c4bb6208281d67147ee6603d958e419b63dcb766998d9695de`  
		Last Modified: Sat, 13 Jan 2024 02:03:53 GMT  
		Size: 500.9 KB (500874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b47a36f27df25156b381723522ea7e9c19bcfda44cbd444845a625c0ca8316a`  
		Last Modified: Sat, 13 Jan 2024 02:03:52 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:653b216a3789bccfce323e88b40276cc1b17ede351d2486d2cabbac3236a2051`  
		Last Modified: Sat, 13 Jan 2024 02:03:52 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:027140c8a985639b84e0b70672ce468087907eb31151491199ebd1a811588e15`  
		Last Modified: Sat, 13 Jan 2024 02:03:54 GMT  
		Size: 17.5 MB (17535031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d9591428a7051a431ab49840c8ab1569488c2ffd575b244453c1676c21a50da`  
		Last Modified: Sat, 13 Jan 2024 02:03:50 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af59b8aedc958911d9dbf07cbc862d38f4160b61afcd6ca659ec535b774db88a`  
		Last Modified: Sat, 13 Jan 2024 02:03:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82a97540eb00d85e17c41dc43aa23b8b0fbdf2f7471bd5c10d938f0d7b76d12e`  
		Last Modified: Sat, 13 Jan 2024 02:03:50 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:030beca12551c010fce4cd7901b7f4a29875e716ab51e585fd02fb0051f43d8e`  
		Last Modified: Sat, 13 Jan 2024 02:03:51 GMT  
		Size: 18.0 MB (18026958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c04aeed41877f2da7034dbbceac48a995a9d6a39720749157987dffb9198e54`  
		Last Modified: Sat, 13 Jan 2024 02:03:48 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:840ff057712e5b0758e9cc3c5270e932b18eb0c3a82b0089c19b292200279d7c`  
		Last Modified: Sat, 13 Jan 2024 02:03:48 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1632d19b5c7da08d6194d0993d09158e67267ef2211e12ca4fa7f5ae6b349332`  
		Last Modified: Sat, 13 Jan 2024 02:03:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3c60e9795150504ea946e2f78aeb11ea9a5e411dc39647547e2e9b3f457c486`  
		Last Modified: Sat, 13 Jan 2024 02:03:51 GMT  
		Size: 19.0 MB (19036445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:78f7c236516822e2af047cf614e881619eeecaf761fbe5c38c7d548d2d7b89e6
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2124791769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c33c6aa8e8990e863f57e8f9d63482d188876759ae1813c268b43d519b41994`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Sat, 13 Jan 2024 02:05:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 13 Jan 2024 02:06:02 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Sat, 13 Jan 2024 02:06:03 GMT
ENV DOCKER_VERSION=24.0.7
# Sat, 13 Jan 2024 02:06:03 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Sat, 13 Jan 2024 02:06:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:06:32 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Sat, 13 Jan 2024 02:06:32 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Sat, 13 Jan 2024 02:06:33 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Sat, 13 Jan 2024 02:06:57 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Sat, 13 Jan 2024 02:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.0
# Sat, 13 Jan 2024 02:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.0/docker-compose-windows-x86_64.exe
# Sat, 13 Jan 2024 02:06:59 GMT
ENV DOCKER_COMPOSE_SHA256=4e0e387d67a65d92e3a7aca085f86b4b46ed5bd7a475f81921629e1d097178f0
# Sat, 13 Jan 2024 02:07:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b496088d3e14a39e14df8cf6f85a1f5370a649f173548295fdcf6753e2b454`  
		Last Modified: Sat, 13 Jan 2024 02:07:34 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:938a6e359e09738200ff1bfa10903c84592586a3c5f4b8d82e44c5374e854f9d`  
		Last Modified: Sat, 13 Jan 2024 02:07:34 GMT  
		Size: 484.9 KB (484895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597fb52eab7032cb1282f9cfe858c3f506f24addd7944ce5293cde6be197b785`  
		Last Modified: Sat, 13 Jan 2024 02:07:33 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bca1de37432a0dcfd878e99b0b0e0e84acb1dc299b6603a8161702bc6b5934`  
		Last Modified: Sat, 13 Jan 2024 02:07:33 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d01aa39ea86f4449b17c524c4c14aabf584a55ed575a0511f8223a413d3cc6`  
		Last Modified: Sat, 13 Jan 2024 02:07:34 GMT  
		Size: 17.5 MB (17527595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66f7fd402fdca17873c613b2a53b184013fdd1d041e5fbdc7302260a4fd721e`  
		Last Modified: Sat, 13 Jan 2024 02:07:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:039c5ce85115eeff703df5a42a3189266c20ce1ee356e617c50e0948a84add43`  
		Last Modified: Sat, 13 Jan 2024 02:07:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dff67c21a5a3c3070b6cba75aa4dacf0c42fdfcf551a8f5f80a8bdbd4256d99`  
		Last Modified: Sat, 13 Jan 2024 02:07:30 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9dfaef4fe69298f540011e7da52bfaa87c48d16498b5e8fabf589699ef1b765`  
		Last Modified: Sat, 13 Jan 2024 02:07:31 GMT  
		Size: 18.0 MB (18019541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ee37ea619718854c07eb8607138ab96b8e2869a2497cfe24f7fa75816056653`  
		Last Modified: Sat, 13 Jan 2024 02:07:29 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e84fa1c4eff30a86e1062dab19bf428eff79fcf0db6d9dccb88899a4c00c739`  
		Last Modified: Sat, 13 Jan 2024 02:07:29 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c57b3cd5073d2a082b08b9d662c3fe4f8eb903a44dcc6b56d0abf9224a1a3e6`  
		Last Modified: Sat, 13 Jan 2024 02:07:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9cf32f0c710730d7b5c731c41bf7e15b823540f762fc1d771f838d42cca09b5`  
		Last Modified: Sat, 13 Jan 2024 02:07:32 GMT  
		Size: 19.0 MB (19025511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
