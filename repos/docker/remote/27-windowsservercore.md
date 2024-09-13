## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:93c29cefdb122b1aaa0617c478f08c4db595809f1209ed61963cfc1afe5c0f81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull docker@sha256:405e693bc29383dfaf6e973687bf5f939b5973b89f78117284d3dce8b1cfe8fe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1520629697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa8de568273b2d55aa406e8e3df3e87e953b908d111d1585d0f1074cd395601f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 12 Sep 2024 23:06:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 23:06:46 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Sep 2024 23:06:46 GMT
ENV DOCKER_VERSION=27.2.1
# Thu, 12 Sep 2024 23:06:47 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Thu, 12 Sep 2024 23:07:01 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Sep 2024 23:07:01 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Thu, 12 Sep 2024 23:07:02 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Thu, 12 Sep 2024 23:07:03 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Thu, 12 Sep 2024 23:07:18 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Sep 2024 23:07:18 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Thu, 12 Sep 2024 23:07:19 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-windows-x86_64.exe
# Thu, 12 Sep 2024 23:07:19 GMT
ENV DOCKER_COMPOSE_SHA256=8603f4e6936e752793f7edf3f45ed67cb1b8ed8c7b1dabc5721384299bfebd7f
# Thu, 12 Sep 2024 23:07:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d2b76973ba80014c7e4c1d928a1a48b8a9eb70d4d0be30e3ec940c03d99be3a`  
		Last Modified: Thu, 12 Sep 2024 23:07:37 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c52885658aa962688b752d11811d45d43bef445e75e57fc5a14064558ded0f5`  
		Last Modified: Thu, 12 Sep 2024 23:07:37 GMT  
		Size: 341.9 KB (341899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead9e67a940a471a586a4516a804edc4d3cf82949e805c8b25d5ee6818058921`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ad2af61af8b64812005cebcb0773a9ea01a7e309030ece195e82976fa233d73`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9415c1343cdbd788dd09414664ecfc4610eceb380cd195e9d1307b2f2b356742`  
		Last Modified: Thu, 12 Sep 2024 23:07:37 GMT  
		Size: 18.9 MB (18913517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd41bc0b9bfd5008aef5f2a2b352f03fd981a96074fc38e8b6834015359dc74a`  
		Last Modified: Thu, 12 Sep 2024 23:07:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139be8568ce6e33024c303ff04a8e5df2cf8f66d875c3769e951f159df929df2`  
		Last Modified: Thu, 12 Sep 2024 23:07:35 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792668dc6d874e1bb541d77edfd6c8d9129743ed28028598747d3120c9aca0f7`  
		Last Modified: Thu, 12 Sep 2024 23:07:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d61431112e35dd7bb61efb83c7c2ec2c03e3160c8bc0643390cd0a221864427`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 19.3 MB (19269180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff28526aa2b8e567eb9d2601ade782df3d2e461c57a22bb4c5b3914c61d4b29`  
		Last Modified: Thu, 12 Sep 2024 23:07:34 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0a400e047f39e5033ae2833ffd362aa3b77cdec0662edbb526c04ffa428fbc`  
		Last Modified: Thu, 12 Sep 2024 23:07:33 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d07564c0fbdea5d9bcf44bd7c7519c83b87d1b9f57fa92afa064b86f5a7cd7`  
		Last Modified: Thu, 12 Sep 2024 23:07:33 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84e4c4be24a83623531a3ca568bd7bad0fdc2b750d4c5d072ba9fa01cb0d9712`  
		Last Modified: Thu, 12 Sep 2024 23:07:36 GMT  
		Size: 19.9 MB (19901121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull docker@sha256:8fde9ff47646452ff2e27068f3b4cb4f9476a7ded1f9113961adef14f3c3e5f3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1778671057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ce0b43adbb67d7798db5e039e5d9bcad7f001ae98db7f523c04c4975b46645f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 12 Sep 2024 23:08:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 12 Sep 2024 23:08:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 12 Sep 2024 23:08:15 GMT
ENV DOCKER_VERSION=27.2.1
# Thu, 12 Sep 2024 23:08:16 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.2.1.zip
# Thu, 12 Sep 2024 23:08:29 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 12 Sep 2024 23:08:29 GMT
ENV DOCKER_BUILDX_VERSION=0.17.0
# Thu, 12 Sep 2024 23:08:30 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.17.0/buildx-v0.17.0.windows-amd64.exe
# Thu, 12 Sep 2024 23:08:31 GMT
ENV DOCKER_BUILDX_SHA256=2bee3541fd1ed077d5f59141085f59345d0d0380d5749724e7088a3f02a113ca
# Thu, 12 Sep 2024 23:08:49 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 12 Sep 2024 23:08:49 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.3
# Thu, 12 Sep 2024 23:08:50 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.3/docker-compose-windows-x86_64.exe
# Thu, 12 Sep 2024 23:08:50 GMT
ENV DOCKER_COMPOSE_SHA256=8603f4e6936e752793f7edf3f45ed67cb1b8ed8c7b1dabc5721384299bfebd7f
# Thu, 12 Sep 2024 23:09:10 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33eeb48469b8cb8fbcc25d58396d3bfcb648410b816b25028d822836be6436c2`  
		Last Modified: Thu, 12 Sep 2024 23:09:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf735aff1ca4cd273b8e91688d4a4982c8dbf01cca8f085b50b4169623ac882`  
		Last Modified: Thu, 12 Sep 2024 23:09:16 GMT  
		Size: 329.7 KB (329714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41b1428dcbd9cfb9bdd6ebcbd6cce242eda98932c00705b3c179585ecb228474`  
		Last Modified: Thu, 12 Sep 2024 23:09:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c57e89724f6a93752272709ffcf477f494b1807d62e36fbc10885e33f2cf7387`  
		Last Modified: Thu, 12 Sep 2024 23:09:14 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aae2dcad4011783d673ce7f81757d43898af3e585090c19c5f59ee35576cf29`  
		Last Modified: Thu, 12 Sep 2024 23:09:16 GMT  
		Size: 18.9 MB (18909686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b1031d3e3cc797515353dba3df2e6962ce58edf83c1adcedd3520df93ec5abd`  
		Last Modified: Thu, 12 Sep 2024 23:09:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0094bc2ef1f0f8b18237edafa452de0a2f8847c3437d49d3e6a769aee9676155`  
		Last Modified: Thu, 12 Sep 2024 23:09:13 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86753ec4a2ceb01ee37a9f2203921291d31c0f8a6d2ed3832a3db8a16575e24c`  
		Last Modified: Thu, 12 Sep 2024 23:09:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693bd41830e9acf36f3d81eae4537d3dc7ca079f2517c98dcbb0dffdd6962f52`  
		Last Modified: Thu, 12 Sep 2024 23:09:15 GMT  
		Size: 19.3 MB (19262621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a8b53a848ffcc09f9265f19ba5ec3b505569ad34bb09a9075be6bcecebc69f`  
		Last Modified: Thu, 12 Sep 2024 23:09:13 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c160ba098736b1836c6325df752a2c0a3415dc3a6412e265865b15236fb0a73a`  
		Last Modified: Thu, 12 Sep 2024 23:09:12 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe78231e5b9a3ab05b45d8c495e9b0701fe711e2d04070606fd9591d1f8ce16`  
		Last Modified: Thu, 12 Sep 2024 23:09:12 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea16651884e8156914519a7179a9602c0098b2ab4b1dc645777f421e81e94a3`  
		Last Modified: Thu, 12 Sep 2024 23:09:15 GMT  
		Size: 19.9 MB (19888980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
