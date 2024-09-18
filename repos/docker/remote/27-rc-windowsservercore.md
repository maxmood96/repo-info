## `docker:27-rc-windowsservercore`

```console
$ docker pull docker@sha256:e22edb4fb88479e1b807a3dba6fffc0ffb01956f3857e2e4e031deddc2bbd22c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27-rc-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:e7e0c99cbc5dc49f357c6bc7cd1324d7592199146d43d748ae9002c3163ef145
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520627238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:001f16c71a1337580b8596ef9d168b3bdf9acf315200576bf9874272b31744f7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Tue, 17 Sep 2024 22:58:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Sep 2024 22:58:34 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 17 Sep 2024 22:58:34 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Tue, 17 Sep 2024 22:58:35 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.1.zip
# Tue, 17 Sep 2024 22:58:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 17 Sep 2024 22:58:47 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 22:58:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 17 Sep 2024 22:58:48 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 17 Sep 2024 22:58:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 17 Sep 2024 22:58:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 22:58:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-windows-x86_64.exe
# Tue, 17 Sep 2024 22:58:58 GMT
ENV DOCKER_COMPOSE_SHA256=4eda107dc1f83a57116c57595d39e6a0ff63e696a52230ea277bd7fa7977c8d7
# Tue, 17 Sep 2024 22:59:06 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:874cdb146cc29a2eff048bf3d44d3bb0f97f5f35ba02e9f96cc348e2ca90ef9b`  
		Last Modified: Tue, 17 Sep 2024 22:59:15 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3a1880b6efa86bb0fdec5b86fc63230980aa641b282a8a197b1a46799be3abf`  
		Last Modified: Tue, 17 Sep 2024 22:59:16 GMT  
		Size: 355.1 KB (355148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ca837f5174e24f11812016649f38fc0933a606c16636ba50860a3021b07c42`  
		Last Modified: Tue, 17 Sep 2024 22:59:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0cb8a6f18c6600e72228bb5fadffcf265d66c7063a3323a9ffae68b11b6ddf`  
		Last Modified: Tue, 17 Sep 2024 22:59:14 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7c07cd5fe4ad420b88176068b8474103d6968dcfe41baefcd493db5e5e81258`  
		Last Modified: Tue, 17 Sep 2024 22:59:16 GMT  
		Size: 18.9 MB (18884453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe663549859818215d2ac82454de3410479587882f96413d77d5b4e2292e710e`  
		Last Modified: Tue, 17 Sep 2024 22:59:12 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2112dc1a54405a4a7bbee24546499d0bec8b456f132c0475a671a228005dc719`  
		Last Modified: Tue, 17 Sep 2024 22:59:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017b45902ad0a38f56d501402f7bcf18f3c6bfc22cc558937d8bf1b177a27a8f`  
		Last Modified: Tue, 17 Sep 2024 22:59:12 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee5a7385741136ce7112a62a92f92864a792495712c1fef553989146d3c0374`  
		Last Modified: Tue, 17 Sep 2024 22:59:13 GMT  
		Size: 19.3 MB (19275981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4353e390e1d6ff2ad3e85dfc3130e160ee41ece8840042cfccd241e4c7e68f2a`  
		Last Modified: Tue, 17 Sep 2024 22:59:10 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9075c23e647e1f9d8d8beeab7cd9db924a7c031864bf1012d313c701ed9b2c2`  
		Last Modified: Tue, 17 Sep 2024 22:59:10 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0593abea47e5d7bcabd51c5d79345c97f520ddab9a1c52d4d400270115440a75`  
		Last Modified: Tue, 17 Sep 2024 22:59:10 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc86eda8bf257df3dd9eaa5a6d3bd4af293ef8d343e4f4795523b795f1b560a8`  
		Last Modified: Tue, 17 Sep 2024 22:59:13 GMT  
		Size: 19.9 MB (19907691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-rc-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:b815f9d53f9b439a9066c3b3e837d0b3313975710150476c77b72c3ec23c98a3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778688897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856400659c312b95c9a1114378b13e3bd955404754827e9d75271470668dd090`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 17 Sep 2024 23:03:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Sep 2024 23:03:35 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Tue, 17 Sep 2024 23:03:36 GMT
ENV DOCKER_VERSION=27.3.0-rc.1
# Tue, 17 Sep 2024 23:03:36 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.3.0-rc.1.zip
# Tue, 17 Sep 2024 23:03:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Tue, 17 Sep 2024 23:03:52 GMT
ENV DOCKER_BUILDX_VERSION=0.17.1
# Tue, 17 Sep 2024 23:03:52 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.1/buildx-v0.17.1.windows-amd64.exe
# Tue, 17 Sep 2024 23:03:53 GMT
ENV DOCKER_BUILDX_SHA256=8751c926b953edf6dd9c7db0b01e567033c407e85bb5f21d559199e2553a07cc
# Tue, 17 Sep 2024 23:04:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Tue, 17 Sep 2024 23:04:11 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.5
# Tue, 17 Sep 2024 23:04:11 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.5/docker-compose-windows-x86_64.exe
# Tue, 17 Sep 2024 23:04:12 GMT
ENV DOCKER_COMPOSE_SHA256=4eda107dc1f83a57116c57595d39e6a0ff63e696a52230ea277bd7fa7977c8d7
# Tue, 17 Sep 2024 23:04:33 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc57543c54b658cb7045bf462d4009ac0421eed94b9e0287719767a286deac4`  
		Last Modified: Tue, 17 Sep 2024 23:04:41 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec15f36b37bee7ad11ba4fd2539527ac4170d450ec6c5a32a6f14bd7d875218`  
		Last Modified: Tue, 17 Sep 2024 23:04:41 GMT  
		Size: 340.3 KB (340281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50bc20c8bbd37453563ca40f2a0357770fc4befb075a045b3cec15d5c7a1d227`  
		Last Modified: Tue, 17 Sep 2024 23:04:40 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3cc1cc5dfd529aa58c7bd8e092620a42caf2bb870507609230ea18f2ee7347c`  
		Last Modified: Tue, 17 Sep 2024 23:04:40 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff71b07ac624e67fee061cc55eb7408bbc073439b22928a7bfcdffdbf336fd0b`  
		Last Modified: Tue, 17 Sep 2024 23:04:41 GMT  
		Size: 18.9 MB (18885686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8cbc70e85a5939bcba4e234e2e0fa8a66382f02fee02de276c832921e5e6c8`  
		Last Modified: Tue, 17 Sep 2024 23:04:38 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5d7b971f0f0ef852c4bd70318b693e52882fe680f49671a2691907c6c70ab4`  
		Last Modified: Tue, 17 Sep 2024 23:04:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440163b90688c11131e903254536f6c94e863d54476509ebab9b6f2948a70f7e`  
		Last Modified: Tue, 17 Sep 2024 23:04:38 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01140b6cbf792ca3bd3398bbeda5855c83c8250e43ec8533f8bc26b1a557c4c5`  
		Last Modified: Tue, 17 Sep 2024 23:04:39 GMT  
		Size: 19.3 MB (19278262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aca7d79e081c9614739aa541f01884179a27adc1740da9a4a813e7fc33eca3`  
		Last Modified: Tue, 17 Sep 2024 23:04:36 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:596c89f5d18bfea5b83ba2e14a7124bac5b432d6af0b574cfe18ef4e30fcf0d2`  
		Last Modified: Tue, 17 Sep 2024 23:04:36 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe0fccbd360bb96083e026dd492f90ba8b81b4ef648027883b0ed299cb96c397`  
		Last Modified: Tue, 17 Sep 2024 23:04:36 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3915161b20e5d9417e376ff41f645931ec8aea303b95333866d4f462b55a1535`  
		Last Modified: Tue, 17 Sep 2024 23:04:39 GMT  
		Size: 19.9 MB (19904666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
