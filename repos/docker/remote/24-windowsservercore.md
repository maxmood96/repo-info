## `docker:24-windowsservercore`

```console
$ docker pull docker@sha256:2fc8d3dfee8968e870ad113ce6b6c32dbfb82de6002cbf89e688d84441d6d1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2461; amd64
	-	windows version 10.0.17763.5820; amd64

### `docker:24-windowsservercore` - windows version 10.0.20348.2461; amd64

```console
$ docker pull docker@sha256:f64d8cf61eb0861cd27dc9fbb7d68245fb4dbd31be8c97285dd795117623e0a0
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2169092039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9003bf795b91cc17bb2e644efd7f693777d4e931fd57766b7cd5870401f01e47`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 10 May 2024 20:40:01 GMT
RUN Install update 10.0.20348.2461
# Wed, 22 May 2024 22:55:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 May 2024 22:55:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 May 2024 22:55:33 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 22 May 2024 22:55:34 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 22 May 2024 22:55:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:55:46 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 22:55:47 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 22 May 2024 22:55:47 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 22 May 2024 22:55:56 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:55:57 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 22:55:57 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Wed, 22 May 2024 22:55:58 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Wed, 22 May 2024 22:56:07 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba03114511317f14392dd2ac806678d1f79c73a8a7e0bc64013540e54c22020f`  
		Last Modified: Tue, 14 May 2024 18:09:07 GMT  
		Size: 724.1 MB (724072575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b998151686eefb94d03cef13a6bd47c3b829c6cd02b5898c5763ef8172b21aa`  
		Last Modified: Wed, 22 May 2024 22:56:17 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eef5a26f249591f9361e4ab6d1d4dddb9046b17d6dc22caf75d4d3febba4c8c5`  
		Last Modified: Wed, 22 May 2024 22:56:17 GMT  
		Size: 347.7 KB (347745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:356d1e858be19b37a07fc5c4410e9b96a6fbde28473e524aaf1deced389b4cda`  
		Last Modified: Wed, 22 May 2024 22:56:15 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d62238c3dafa754d614d8ffb607289c12b3e20eab9b7192963802c995f45540`  
		Last Modified: Wed, 22 May 2024 22:56:15 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e86ccd96c7882e028c701d251bebc45dd19ed0cbe5a517d12dec3d2696fe85`  
		Last Modified: Wed, 22 May 2024 22:56:17 GMT  
		Size: 17.5 MB (17521247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3da0d675278e5a34804290aa783e5dfa3bd632ae71831e90d51992a8db58381`  
		Last Modified: Wed, 22 May 2024 22:56:13 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2476015d7ba84d414b824b0a3a6c615b0da5a29bb5ee28202061ced5148e4d2b`  
		Last Modified: Wed, 22 May 2024 22:56:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46dea17365a061f2cc92f0414bf29dba55707b4bffb15cfa0eed8c31e5a220b1`  
		Last Modified: Wed, 22 May 2024 22:56:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02bbc39042afda5832b8b8f0c22281a0d41c5744eab1bf0df1a92ba76bc16c3`  
		Last Modified: Wed, 22 May 2024 22:56:14 GMT  
		Size: 18.9 MB (18919233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84e30d66a3d1486f44c6b3b00b90cdcd0c8f576b8685c21bf7c2ef2706f6d9b`  
		Last Modified: Wed, 22 May 2024 22:56:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d6cca4f2d86d9766daf7300cfa9dba7b708368a59fb5ddf2c121db3131356a`  
		Last Modified: Wed, 22 May 2024 22:56:11 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b47e3485cef56a78e0ed73008d079278bc10133c2e1948a47e776ffc452e7a`  
		Last Modified: Wed, 22 May 2024 22:56:11 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e248e5ed21f036eb826b1e406ed29e4663258af85d2d7a90487fbdbbe615c68`  
		Last Modified: Wed, 22 May 2024 22:56:14 GMT  
		Size: 19.6 MB (19620763 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:24-windowsservercore` - windows version 10.0.17763.5820; amd64

```console
$ docker pull docker@sha256:e3cac9ac54534216b4ca25f70e64239acc34767385486eb443bf584bfc384154
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2236409712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d06a5e526e050fc33276c1ec21f2c655de85f7bbd1f7f4bd19f895cc8d7b134`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 22 May 2024 22:54:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 May 2024 22:55:43 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 22 May 2024 22:55:44 GMT
ENV DOCKER_VERSION=24.0.9
# Wed, 22 May 2024 22:55:45 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.9.zip
# Wed, 22 May 2024 22:56:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:56:16 GMT
ENV DOCKER_BUILDX_VERSION=0.14.1
# Wed, 22 May 2024 22:56:17 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.1/buildx-v0.14.1.windows-amd64.exe
# Wed, 22 May 2024 22:56:17 GMT
ENV DOCKER_BUILDX_SHA256=21830c62d2a43ef2568ad325c338e892f7d534e656795e1fa49f68a679ac5928
# Wed, 22 May 2024 22:56:47 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 22 May 2024 22:56:48 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Wed, 22 May 2024 22:56:49 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Wed, 22 May 2024 22:56:50 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Wed, 22 May 2024 22:57:17 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56701875d16553e79817f1dec0e35e190c1f1bc105e779b7c375c46e977270a6`  
		Last Modified: Wed, 22 May 2024 22:57:26 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe85da59b7201c3a4761ef1dc83a49057961e8002484289893b5c2a821dada39`  
		Last Modified: Wed, 22 May 2024 22:57:26 GMT  
		Size: 510.7 KB (510734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8d25ecb09b1152719f4fcfe1f3b9ec7f72539e1cd7458d24fb8d7d0d4faff0`  
		Last Modified: Wed, 22 May 2024 22:57:25 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ec082f51b2c03783d4d40c0d26368681ff02953e3d34a5ea8229ca0c7cdd0f4`  
		Last Modified: Wed, 22 May 2024 22:57:25 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6fa4715a75be9a559627ce1f6cc94118b3786ba6dac8c2f63c0123d933dabd`  
		Last Modified: Wed, 22 May 2024 22:57:27 GMT  
		Size: 17.6 MB (17564822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc920e4c99c4903ab19fa513b65263eff7ca6fef3c9adf475103c51c96d78340`  
		Last Modified: Wed, 22 May 2024 22:57:23 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccee69634280e96bfb9054f6fc9f02af7f246c96d3ec3b0a3a0b7f60c07444ad`  
		Last Modified: Wed, 22 May 2024 22:57:23 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280fb5dfbebdaee9c20e447e483581c8b506681e13b674b56591effa74a9ddfc`  
		Last Modified: Wed, 22 May 2024 22:57:23 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e271d2b4866fca6e11f3b98baf26f11294076ca34ade376b64421138e04acf3`  
		Last Modified: Wed, 22 May 2024 22:57:24 GMT  
		Size: 19.0 MB (18956378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26ec1052aefdc84bc29786a723e2b3ef9060ea05079a25e0a49843b32867e9d`  
		Last Modified: Wed, 22 May 2024 22:57:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eef517dd01ccb2dfd2e957d3ba7c8601f338f392dc09a0b88902e395c2b352c`  
		Last Modified: Wed, 22 May 2024 22:57:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f6182e165baabf4b0dfabe950bc80b70d14b3d43794aad8cd23c5a63f133c79`  
		Last Modified: Wed, 22 May 2024 22:57:21 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f939f72e8fd71cc24d25011119becd8ab6b60cd192ef681bb55575da262ea61a`  
		Last Modified: Wed, 22 May 2024 22:57:24 GMT  
		Size: 19.7 MB (19654642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
