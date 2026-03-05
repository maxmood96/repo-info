## `docker:29-windowsservercore`

```console
$ docker pull docker@sha256:90ad4a37056b63a3882c8d3c12b728799c8c301cfcf077f0b54a0f07f4589965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `docker:29-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull docker@sha256:a72ce64c78274996c1b4b42d7a0f66f37175630ed095e8ba4e2a696b73abc496
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2026133456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fb24733fa85780e10415c1eead19dfee395c7ad5b5c7b0bb7b46a9cb04da12d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Thu, 05 Mar 2026 18:59:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Mar 2026 19:00:42 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Mar 2026 19:00:43 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 19:00:44 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Thu, 05 Mar 2026 19:01:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Mar 2026 19:01:00 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 19:01:01 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Thu, 05 Mar 2026 19:01:01 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Thu, 05 Mar 2026 19:01:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Mar 2026 19:01:11 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 19:01:12 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Thu, 05 Mar 2026 19:01:12 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Thu, 05 Mar 2026 19:01:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91d1a8a6e8a02bacaa0cb852af9b130f79b3e75217c941735e602588438341d`  
		Last Modified: Thu, 05 Mar 2026 19:01:29 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915ea27d9fcff3265f8621bcd58538383106512d8ee139843933e4aa2dac3703`  
		Last Modified: Thu, 05 Mar 2026 19:01:29 GMT  
		Size: 401.5 KB (401543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd10d9d7b58e5996fb583d0b0d10d055606d96f9edf196ff1f5742fdd10220d9`  
		Last Modified: Thu, 05 Mar 2026 19:01:28 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851d627862c692ace5c664d4125ca0b51d34d0d36620e45cc69347d1782b4f4`  
		Last Modified: Thu, 05 Mar 2026 19:01:27 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea3611e153866cd60e61b0cb5e1d10488d937bb671126d8b9a445e42bfef0cdb`  
		Last Modified: Thu, 05 Mar 2026 19:01:30 GMT  
		Size: 19.6 MB (19622332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa0b288bc9f43ef9edf51a4b865e0dc86c931e34102b33c9a926db1b273153c2`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071a5927eed307df7387e858c0a092a79362a038fb7a196d6284f2a836fd53a4`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 1.4 KB (1369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6b18e8aa1db4565b440e2467adaa75cbb4d144987fd6c20b4405e5d8ce70a7`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6447abe3658079578872007da50315083eee58828fb752c05af4f9333bac9a15`  
		Last Modified: Thu, 05 Mar 2026 19:01:29 GMT  
		Size: 29.7 MB (29666438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db544d374eecea25c6051e8e18b98719807c54789d9d109d2e7587a9fc0107d0`  
		Last Modified: Thu, 05 Mar 2026 19:01:24 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c94d4d5d67e7de268a916c2ca0a9cd33d175d5de6c7ba600caea238b0342ca5`  
		Last Modified: Thu, 05 Mar 2026 19:01:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7076172216a77708fe1042dbc178297940214b0c2b67229608d5b180a82521d5`  
		Last Modified: Thu, 05 Mar 2026 19:01:24 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2075710695e1e3ef40ee40ef482cbccc04111fa62f56d5da7dc61ba5d0c5352`  
		Last Modified: Thu, 05 Mar 2026 19:01:26 GMT  
		Size: 11.7 MB (11671331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:29-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull docker@sha256:5f4a5c4eda9eab527b544bf7a9b95b7dd2fece5aa7150b977352c6ec234c82ff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1923934611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba4e29eb44be08787b5b548fbf5080547b8ac1814cee437511e5ae1b35f67160`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Thu, 05 Mar 2026 18:53:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Mar 2026 18:54:52 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Mar 2026 18:54:52 GMT
ENV DOCKER_VERSION=29.3.0
# Thu, 05 Mar 2026 18:54:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-29.3.0.zip
# Thu, 05 Mar 2026 18:55:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Mar 2026 18:55:22 GMT
ENV DOCKER_BUILDX_VERSION=0.32.1
# Thu, 05 Mar 2026 18:55:23 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.32.1/buildx-v0.32.1.windows-amd64.exe
# Thu, 05 Mar 2026 18:55:24 GMT
ENV DOCKER_BUILDX_SHA256=47d76e47acf3c7611dd594c4b0909fec680ae6406b6fa775f6077b195837e2b9
# Thu, 05 Mar 2026 18:56:00 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Mar 2026 18:56:00 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.0
# Thu, 05 Mar 2026 18:56:00 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.0/docker-compose-windows-x86_64.exe
# Thu, 05 Mar 2026 18:56:01 GMT
ENV DOCKER_COMPOSE_SHA256=ee84e42b93c501cb0aa2caa84d76b5f30ca6fb92f070e289fc37be7332c5822a
# Thu, 05 Mar 2026 18:56:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2bc2e7f0f05f2d19245abe6bbf9bee5c5ba35482b3eb9bdcd63f4e7b662e64`  
		Last Modified: Thu, 05 Mar 2026 18:56:29 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fb854529e960db2186028d12bccb438515ef2e5ee44c31c4e7c2e8af277b490`  
		Last Modified: Thu, 05 Mar 2026 18:56:28 GMT  
		Size: 502.2 KB (502223 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d27af45f9b00441e9346c1440c6fb382f587e9c8624389c8f4159fe073397ad3`  
		Last Modified: Thu, 05 Mar 2026 18:56:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b53ff028e6961972c6290d925e1ba3a7750c09a56f57ca6750fa94a9a6ef2ac`  
		Last Modified: Thu, 05 Mar 2026 18:56:27 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46c60c7b796a7728869000db4d5039c8910d973d5893c8c6e35ed3f1f0defe1`  
		Last Modified: Thu, 05 Mar 2026 18:56:29 GMT  
		Size: 19.6 MB (19552767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e46fb1236511953f8638c95d06afe41a11f878407a5f7378ee726ab431281609`  
		Last Modified: Thu, 05 Mar 2026 18:56:26 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:288360be421c4e9dce141a77c43faaea7f9bdd5dfa039783f95145825cd06bd1`  
		Last Modified: Thu, 05 Mar 2026 18:56:26 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf39f00950f7123c834e6f223ad303efd3ad2da3ab4180069573889f7b23e2c`  
		Last Modified: Thu, 05 Mar 2026 18:56:26 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a8e91c8c48091ad6d18055ba33dcb797cbbb445bf9fc307ef5cf1b49a40bf2`  
		Last Modified: Thu, 05 Mar 2026 18:56:49 GMT  
		Size: 29.6 MB (29604873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1993d9295d4f6d222cae7f646c466ef0e2b17f1293923859e9c4f9d710b103f7`  
		Last Modified: Thu, 05 Mar 2026 18:56:24 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:505b19f86bc7a7117f5fcb99cea47b3866b4e6ce0594de2add869263a234f865`  
		Last Modified: Thu, 05 Mar 2026 18:56:24 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd04c209d2b4ec6f230ed618f4fd6bbf43baab76fa8b0a58804509d929879a0d`  
		Last Modified: Thu, 05 Mar 2026 18:56:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34e7636d52feff8ebfad0450f2b4e61f35555852b3ec576130ee410c89fcb8a`  
		Last Modified: Thu, 05 Mar 2026 18:56:26 GMT  
		Size: 11.6 MB (11605746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
