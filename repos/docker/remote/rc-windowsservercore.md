## `docker:rc-windowsservercore`

```console
$ docker pull docker@sha256:e3e8a7176afbf21cda7d0a76e7f6f7a6148fb924f6df6d8a16d1a8c2fd7bd41f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `docker:rc-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull docker@sha256:92b36dcb2656dc4cec09361d67312c5a6b3193fce07d90d354247d9273b96e6c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2136896440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee6dca3f5eacd0b0ee0376048144291248199b52b950ec2559aec127982a384a`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Fri, 03 Apr 2026 16:46:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:47:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:47:46 GMT
ENV DOCKER_VERSION=29.4.0-rc.1
# Fri, 03 Apr 2026 16:47:48 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.4.0-rc.1.zip
# Fri, 03 Apr 2026 16:48:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:48:12 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:48:13 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:48:13 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:48:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:48:36 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:48:36 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:48:37 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:48:48 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52c270b4855aee55fc942597e3d97a269264cc59cd8fbb9b71a492d157d326c5`  
		Last Modified: Fri, 03 Apr 2026 16:48:57 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9ec7fb0e409b846a9c5328f5e291bf3c107ad7361341cd0427652243cc0f2d`  
		Last Modified: Fri, 03 Apr 2026 16:48:57 GMT  
		Size: 393.8 KB (393836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0982f4d571b37b1d2f83f48b122348ab67800272d146f27cda771d945cb189e7`  
		Last Modified: Fri, 03 Apr 2026 16:48:56 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83362725d9d1fa249e2105bc4990a9286f9fdf370cb792af104224e3cc6544ee`  
		Last Modified: Fri, 03 Apr 2026 16:48:56 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8560c11039fb87e030bff8590677eb44ebb121d845760335e49880ba6f970c9`  
		Last Modified: Fri, 03 Apr 2026 16:48:58 GMT  
		Size: 20.2 MB (20172878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66b8241f2925f542c306f803b47dd214bfdfcd5c73db69574778c3997ea3b58a`  
		Last Modified: Fri, 03 Apr 2026 16:48:54 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdbc918e34464efbe8c9fb638df938675615b18473968b2c4e1e95b64e6ba63`  
		Last Modified: Fri, 03 Apr 2026 16:48:54 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c718950d774c4bd91e61b55cc95e47c4a90273c53d994fc535cd34f3233f4542`  
		Last Modified: Fri, 03 Apr 2026 16:48:54 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ce49c888dec05d151daee58a6ee0b8d44ced25959f2a756048e75b913d5e2ec`  
		Last Modified: Fri, 03 Apr 2026 16:48:56 GMT  
		Size: 23.5 MB (23454211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5099778bad799b4eabedbf4d318ac87310898b6d3b5f56b3cee5c31516a2bd8f`  
		Last Modified: Fri, 03 Apr 2026 16:48:53 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fbfe9b1763d1e1db1e65b321d9e0907fa79eff868d6a73b04196781d8f9f534`  
		Last Modified: Fri, 03 Apr 2026 16:48:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db953123acbac143685ed0ffc102ad13d5a4653945055de4894693455da98ef0`  
		Last Modified: Fri, 03 Apr 2026 16:48:53 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e9a9c1eca9259967503b681a4477e6fb763abece4443c27e154d727797aa42`  
		Last Modified: Fri, 03 Apr 2026 16:48:55 GMT  
		Size: 11.7 MB (11667712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:rc-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull docker@sha256:035c05fcce3198152b4157e0ad39cf52f7ababb12f0d56a4ad95c64677516744
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2038020088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99e8f28cd22d672c311b91be19969103d99bebbcbcfcb93b521abfebae661081`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Fri, 03 Apr 2026 16:44:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 03 Apr 2026 16:45:20 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Fri, 03 Apr 2026 16:45:20 GMT
ENV DOCKER_VERSION=29.4.0-rc.1
# Fri, 03 Apr 2026 16:45:22 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.4.0-rc.1.zip
# Fri, 03 Apr 2026 16:45:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:45:33 GMT
ENV DOCKER_BUILDX_VERSION=0.33.0
# Fri, 03 Apr 2026 16:45:34 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.33.0/buildx-v0.33.0.windows-amd64.exe
# Fri, 03 Apr 2026 16:45:35 GMT
ENV DOCKER_BUILDX_SHA256=832ddf42373203ee3836a7cb3b16fe5080231491e7edb32019ac0f6fe03b99ed
# Fri, 03 Apr 2026 16:45:44 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_VERSION=5.1.1
# Fri, 03 Apr 2026 16:45:45 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.1.1/docker-compose-windows-x86_64.exe
# Fri, 03 Apr 2026 16:45:46 GMT
ENV DOCKER_COMPOSE_SHA256=f7ad2f6965c88153e4902019ec86e95414f0025cba0b6440f328f935a1f8b12b
# Fri, 03 Apr 2026 16:46:05 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9da6bec9129477f95248df012e3c95af897071a17f295005157697d398f7a8a`  
		Last Modified: Fri, 03 Apr 2026 16:46:14 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:431b75303dee1a94631986a8d853d10b4954aaf33183462263298acb84c04a1a`  
		Last Modified: Fri, 03 Apr 2026 16:46:13 GMT  
		Size: 502.7 KB (502740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c254d8f2576834e1e2d179c36c3f54cd49bb79ac5e3aa4cba5b38634c57e234`  
		Last Modified: Fri, 03 Apr 2026 16:46:12 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095d0ea30e4edaf819bc0be1eda06ade8abb9ce866f352d4231d4bde13f3c960`  
		Last Modified: Fri, 03 Apr 2026 16:46:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052d68affeec4efbe4b05efc3ae1e3f71aa81b43ee481df24ca807f46cc7a0fc`  
		Last Modified: Fri, 03 Apr 2026 16:46:14 GMT  
		Size: 20.1 MB (20145774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1dc5f43325b5b602b59c5d972f49fd08c807203a494c8d48e9c502836d9e58`  
		Last Modified: Fri, 03 Apr 2026 16:46:10 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a23fc5cf9f86530c3cbacf67a16ade26b9dcd3bdf8fc5f489c2c038cb872913a`  
		Last Modified: Fri, 03 Apr 2026 16:46:10 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a46e4088c8296ddb01eb9bf19c7f7ee7bd32efa49e8d5ee2fad2366f7faaddb`  
		Last Modified: Fri, 03 Apr 2026 16:46:10 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e88dd606db010eece3badf6b6f978f4ad5587bf711e973dab82cc352869a558c`  
		Last Modified: Fri, 03 Apr 2026 16:46:23 GMT  
		Size: 23.4 MB (23434424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51bcba0754c5a5b20e37b8258d0c23e2c907bc84c5299eecac20cf862a818b91`  
		Last Modified: Fri, 03 Apr 2026 16:46:09 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9dc27b70d34bebea3433443de19bd77ff4787d228e128ff259ae16c64d6958`  
		Last Modified: Fri, 03 Apr 2026 16:46:09 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:764d925495d3487d672141eaf3ccaceaa1a407e19a6dadcb33487b426241dfe6`  
		Last Modified: Fri, 03 Apr 2026 16:46:09 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd771fd7ddb4e6a40933bfe63393c1df876459af1c746145baea179b10d7113`  
		Last Modified: Fri, 03 Apr 2026 16:46:11 GMT  
		Size: 11.6 MB (11643994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
