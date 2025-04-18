## `docker:windowsservercore`

```console
$ docker pull docker@sha256:429c6cc329d558cde0f693432c7025e2ebd2997e97851488850d34cafdc3d804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `docker:windowsservercore` - windows version 10.0.26100.3781; amd64

```console
$ docker pull docker@sha256:1688b4283d6333dc6b062b9725f33e581febe882f118bdaca25c16a43952408c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3459681963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a67f4377ec1505bc64fdd5fba308d67690797d25ae8fae2c2abe3a8220b470`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:14:03 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:14:11 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:14:12 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:14:13 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:14:24 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:14:25 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:14:26 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:14:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:14:36 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:14:37 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:14:38 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:14:46 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:260c6bd48bf9b7bcd23a74ce27f83b531faea9e315ff6737ef884b00bd81da70`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d26d0fae6a860033208ee05de1b45fff21172f23e6c08fcb6c8ddd89a4cf120`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 370.8 KB (370783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42e04ee05f729c840466ec7fdbddf08441974dd64583ae57b0c2e1e82888dc02`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a31d3ae72d44e6ac1ba7d34ae1f04a19832141dd6bce84fcc466087f8b56eb`  
		Last Modified: Fri, 18 Apr 2025 03:14:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f75320aa722434dac44791dfa0fc684d4a9118fa6391061b2a6f8101d52a7`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 19.9 MB (19906717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3437ffb66e6fb89a8e52416a38c4e07715674914477817e827340751d33df40`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8902215ab64b3c66d798e6283552def1adaaa91ec7060d2b701324013ff287a5`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d0a4f89a37a7fcddfc7bba6da9b4f189b05df2f60d049e0deb935afa332f2bd`  
		Last Modified: Fri, 18 Apr 2025 03:14:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b207e20d43751d763b52f2c66c50dac0f795edac26bd54f2fceebbd844ac18b0`  
		Last Modified: Fri, 18 Apr 2025 03:14:52 GMT  
		Size: 22.4 MB (22368711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded394e9a68dc176a9ac6ae87bae98371ce9575ebf52a380abe1c57025a67662`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e11948f5717802bd1eaac711e6cdb65cbcaac908f474150dbbd248d948802859`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29097adaffd2b10496a62fdf22ccd89530230ca2141515caec61c5e4cff7d9e`  
		Last Modified: Fri, 18 Apr 2025 03:14:49 GMT  
		Size: 1.4 KB (1360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8af02f07dd826ea269773bc614ae42f76d01eec6273637e02431652a26045646`  
		Last Modified: Fri, 18 Apr 2025 03:14:53 GMT  
		Size: 21.9 MB (21862437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.20348.3566; amd64

```console
$ docker pull docker@sha256:995ca0bf38de1f8a0245f2caa155396da4f06cbc594336fb9c76897128890d91
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2338010035 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fe100f55f377339e6d5f4224211c47c2fbb6b253a25fa282fcc1576ced9f558`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:16:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:16:56 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:16:57 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:16:58 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:17:08 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:09 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:17:10 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:17:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:17:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:17:19 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:17:27 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b22ed7df539503b8409fa12a12fac0de1ecc8657bd576c4dcad98a9a93f6c3f6`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa96fabcddd098deceb4965e2923d655850837faf9387775bb7a3f7347379f68`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 348.4 KB (348428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af955c30c344b96d47b273fc240431ecb647b6d5e6b5a6db506fd0a46eeda828`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e779905e67487e73a71ba4407c8ecfdf2b013b20d213efb032bd04ad16cca2c1`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4805881421d38e32a8c7790733335e6261d0766591620a2b2ff692b5b1b0a0`  
		Last Modified: Fri, 18 Apr 2025 03:17:34 GMT  
		Size: 19.9 MB (19886290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35a8cfa1b6a752dcfa395a1f04be70be82b8e3b567e5e5068788dbb471737e3c`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60819df3ae15cadcce13014b660c523cb6b6de908488d5b054f4b3a9847a592b`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b4d3e5a621f70aa48fd9ba3cfa11d545e447fb079315c602e625b6f4ceeccb`  
		Last Modified: Fri, 18 Apr 2025 03:17:31 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4da2eae8290184aea1d6de343a3bd28a09a8797b29e585a267a77fe14ee5df`  
		Last Modified: Fri, 18 Apr 2025 03:17:33 GMT  
		Size: 22.3 MB (22346645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e9a652976a5b14d3f822b16d23e045465bbe41007f536e9adffe54db8f0687`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d342975a32de3069ec71a8b68ac01b3c48ed4667b43bdfb1184c425c513c7e7c`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864f4aa6948b12f6e4eaebbd858bced5d111337ee7ffc5944059dddbf7145b92`  
		Last Modified: Fri, 18 Apr 2025 03:17:29 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c001844b2a9a1d6bbb6fd855f7437999f2cb31fb9f22815db8a4a9579731e813`  
		Last Modified: Fri, 18 Apr 2025 03:17:32 GMT  
		Size: 21.8 MB (21834550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:windowsservercore` - windows version 10.0.17763.7249; amd64

```console
$ docker pull docker@sha256:76e33dc88f985d1beab4d78f43dd885d456de128945b4a6dd03981c5bb2f35bf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2229913583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f586db89c826ee7b52a5ebb6e4f0f9b89a87d4eb2eda2cd54dc67e02c90f1cdf`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:11:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:11:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_VERSION=28.1.0
# Fri, 18 Apr 2025 03:11:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-28.1.0.zip
# Fri, 18 Apr 2025 03:11:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:11:59 GMT
ENV DOCKER_BUILDX_VERSION=0.23.0
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.23.0/buildx-v0.23.0.windows-amd64.exe
# Fri, 18 Apr 2025 03:12:00 GMT
ENV DOCKER_BUILDX_SHA256=ba6f6ac5abbbf2e9a222fc0332b9f101f0709ced48cecb25147ddb3d143067c0
# Fri, 18 Apr 2025 03:12:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 18 Apr 2025 03:12:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.35.1
# Fri, 18 Apr 2025 03:12:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.35.1/docker-compose-windows-x86_64.exe
# Fri, 18 Apr 2025 03:12:13 GMT
ENV DOCKER_COMPOSE_SHA256=971d6000e2c70da19c20f8264330a7ec3962b1fd59601afeb7e3636bad89b8c9
# Fri, 18 Apr 2025 03:12:22 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:390143f98317407a20ac29c08b9ec3b59ab9a7cd865888e898464db9e33c4b1e`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:230494274935a2d45131a3ae53d73013b524f80b5f1c5c346f361572546c443d`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 337.0 KB (336986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ae671c2fb897de70375a2ffd366a9df2ca182b54ee1c98fc04054eed585c852`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b60498a9f6b4d861a2fb43e6765f711d9fc862decf8f6669268f935e417efca`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e96b8a20b826e815d7b12e8b80a6870a6d57fda4040e07e958ecbca9250a7`  
		Last Modified: Fri, 18 Apr 2025 03:12:32 GMT  
		Size: 19.9 MB (19878251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a665a369422bcdc54e164d7d15190b072e05a725bd7bb0b71b6e8122238bae0`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e2ec24a0da078daf54e38f2804f68f22646c0635fd9c07e9666160b6a75e8f3`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841757b89b0ec185e9e9c24a2bbaa990da0810e57f369e5c6e275cade454cd90`  
		Last Modified: Fri, 18 Apr 2025 03:12:28 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e71a487c601cdf1b95461f1d743ce1bc4d360fa55fb753d2c1f87c58987ea79`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 22.3 MB (22339705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3dd42e2c5ce5fadf18e468bfa810ec1a0a31db7526079ae284b593296a82e09`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f848fd528a82281bfcf00e5773ccdfe2c8f7cd77cab21abcefca9df3a3618626`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddcfefefef3315a12a85b7a2692ec7f43bd6cf67a23e3f69fdce2f31aa05c339`  
		Last Modified: Fri, 18 Apr 2025 03:12:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7b76f6dddb987140c5bd123843c626ccb3c54d67ec2c959df7fc666b6dbc8d`  
		Last Modified: Fri, 18 Apr 2025 03:12:30 GMT  
		Size: 21.8 MB (21821032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
