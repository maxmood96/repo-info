## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:b1de7133812432bcf19524043d772e56d42ea2eb3ac0ed426dcfb47d3376d2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull docker@sha256:b6488edda0acb9cf96e5dc9e958953b4957e0ac6d396b67f7d944c11b6da5e06
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2069849551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda1cf6b54984b76701e28323e5b111dc4fd83f6bcab483c95941ac8c2b41aa7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Thu, 05 Dec 2024 01:27:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 05 Dec 2024 01:28:54 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 05 Dec 2024 01:28:54 GMT
ENV DOCKER_VERSION=27.4.0-rc.4
# Thu, 05 Dec 2024 01:28:55 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-27.4.0-rc.4.zip
# Thu, 05 Dec 2024 01:29:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 05 Dec 2024 01:29:13 GMT
ENV DOCKER_BUILDX_VERSION=0.19.1
# Thu, 05 Dec 2024 01:29:14 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.19.1/buildx-v0.19.1.windows-amd64.exe
# Thu, 05 Dec 2024 01:29:15 GMT
ENV DOCKER_BUILDX_SHA256=62c0ac3c49debde197ff855dbcd752829f4f31042336a42ba4033a43ec7a7ef2
# Thu, 05 Dec 2024 01:29:26 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 05 Dec 2024 01:29:26 GMT
ENV DOCKER_COMPOSE_VERSION=2.31.0
# Thu, 05 Dec 2024 01:29:27 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.31.0/docker-compose-windows-x86_64.exe
# Thu, 05 Dec 2024 01:29:28 GMT
ENV DOCKER_COMPOSE_SHA256=93fa851954c19e0e19b753817eca37c81c9f4394b0db1853ebc66cd62230ea75
# Thu, 05 Dec 2024 01:29:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1221c39d67709c4b655fd306fe07287bd26b6cdc58323b0451524ec92897cbba`  
		Last Modified: Thu, 05 Dec 2024 01:29:49 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce8bbc473ec0fd2d0dc55379fc8c5723532e493a8623e7b58dbdf08aae7e9f2`  
		Last Modified: Thu, 05 Dec 2024 01:29:52 GMT  
		Size: 489.3 KB (489320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa040ec55e2513ca18f4d79c7fa979f3d0db3dabc1aaca394a1afaf2cabb341a`  
		Last Modified: Thu, 05 Dec 2024 01:29:58 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1379c98f8c659d791bdef99e329ee2a5508f859308df49896656d351eb412333`  
		Last Modified: Thu, 05 Dec 2024 01:29:47 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3d946188c456f35735741fc3f82847fa84ee906d85bc0abf5443732dcdca000`  
		Last Modified: Thu, 05 Dec 2024 01:29:49 GMT  
		Size: 19.0 MB (18998762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c814be54ae48fd6073d3aed258ad0e5aa3b73c7ed26282341507a04b4388f052`  
		Last Modified: Thu, 05 Dec 2024 01:29:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5008c45ef626af321ea5e6077fb39e4d5550dea08c2404f046355d13299e2ce3`  
		Last Modified: Thu, 05 Dec 2024 01:29:45 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c76ca3f286850d13b68da971ed54177fe87c1dc46505af1e2a90229328e0d121`  
		Last Modified: Thu, 05 Dec 2024 01:29:45 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1da3824ee335951bc1022346c7313eefef8b00fa78fa82911a3848d4afa80ea`  
		Last Modified: Thu, 05 Dec 2024 01:29:46 GMT  
		Size: 19.6 MB (19645451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75ac2e8f6c81dcdcc124ed1bbd7c0a7bf804d0b3845822980f197f5cb377f62c`  
		Last Modified: Thu, 05 Dec 2024 01:29:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e767c467c1a24d51e9b995373ef262dbefccc9ea634fb252125d4c3c171376`  
		Last Modified: Thu, 05 Dec 2024 01:29:43 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4822cc0251b86b3891e7ac8c7abaea207f55b114e64a0ee6fec6f49cd439a3ae`  
		Last Modified: Thu, 05 Dec 2024 01:29:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdc55493aa9835427b16c17ba1d28567715ea79a0b3f5c30e5ab320e04088f7`  
		Last Modified: Thu, 05 Dec 2024 01:29:48 GMT  
		Size: 20.1 MB (20050561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
