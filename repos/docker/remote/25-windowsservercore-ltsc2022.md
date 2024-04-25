## `docker:25-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:c9ca4afcfd49eeaf0c6af3c19e4272a1a3da4b6b3ac2731a8839dace4748c881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `docker:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull docker@sha256:92ba4d13afa1ea420d3a459c01032800906b4cbe70c31b5d210b61900084a3cd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2056531694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e159876ee84bc2477e06ca249179171c5fd36f4de40239278d2fb30c5eca6658`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Thu, 25 Apr 2024 18:53:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Apr 2024 18:54:01 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 25 Apr 2024 18:54:01 GMT
ENV DOCKER_VERSION=25.0.5
# Thu, 25 Apr 2024 18:54:02 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-25.0.5.zip
# Thu, 25 Apr 2024 18:54:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 25 Apr 2024 18:54:15 GMT
ENV DOCKER_BUILDX_VERSION=0.14.0
# Thu, 25 Apr 2024 18:54:15 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.14.0/buildx-v0.14.0.windows-amd64.exe
# Thu, 25 Apr 2024 18:54:16 GMT
ENV DOCKER_BUILDX_SHA256=d43f5008431fb4ffd438d14ea686ed0f9c7ef101f2dfd1f84a5670979aeb39a8
# Thu, 25 Apr 2024 18:54:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 25 Apr 2024 18:54:25 GMT
ENV DOCKER_COMPOSE_VERSION=2.27.0
# Thu, 25 Apr 2024 18:54:26 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.27.0/docker-compose-windows-x86_64.exe
# Thu, 25 Apr 2024 18:54:27 GMT
ENV DOCKER_COMPOSE_SHA256=2e5ae01bbec3bd6ed3a5a267df7edee3c8c5fc59101a0aad0241ed4ed46c70ac
# Thu, 25 Apr 2024 18:54:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03047e1dd7dcc90daa0818ac9df009ac038bca0658cbbc9f7bc54915f888be0`  
		Last Modified: Thu, 25 Apr 2024 18:54:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f321beba22de9330c91356537349aae077894c8fe0cf9feb40eb879406940ea9`  
		Last Modified: Thu, 25 Apr 2024 18:54:45 GMT  
		Size: 499.2 KB (499219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7933ef5e192a4d97d74bbb894be820ee873d9a9dfee504d50adc24e47c0df15d`  
		Last Modified: Thu, 25 Apr 2024 18:54:43 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb15fd46b334e3e82ab9e006cbf656ba92c208c0430dd5a20601e3bad5c30300`  
		Last Modified: Thu, 25 Apr 2024 18:54:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8135b2c507eb01b6283d2ca5146956152c192582253ceeec31fd40724274b113`  
		Last Modified: Thu, 25 Apr 2024 18:54:45 GMT  
		Size: 18.1 MB (18079854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9750d30f8cb1b4202b5e4ee7666ee1409b53a9c523172a9c83f44625bfb91e6d`  
		Last Modified: Thu, 25 Apr 2024 18:54:41 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcd0d813b088f1e3ade3923fba1f08a32e089ac896a3c472965454dcee7ff0e4`  
		Last Modified: Thu, 25 Apr 2024 18:54:41 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b8d175ff8e7c05d78a7bbc2e89cdf236a8ebaa93e01f457967841f52afbba6f`  
		Last Modified: Thu, 25 Apr 2024 18:54:41 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ffe767adf2c5d2e5df0793567672e43428ccbd72150a64230133c859f3e136d`  
		Last Modified: Thu, 25 Apr 2024 18:54:42 GMT  
		Size: 18.9 MB (18927732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e020dc3e3bc158695c86ff9fcdfbf8b6a69ec57e991a081f518f6029528ab692`  
		Last Modified: Thu, 25 Apr 2024 18:54:39 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c33f8ae4e5ab614b8f361f286b83290fa8df8d40b29bb2306915b8033b7e8e`  
		Last Modified: Thu, 25 Apr 2024 18:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a025ef59d9dfc849ed13562ccf5af01da8d1f1eac374eca24ecf3cf15de3ff3`  
		Last Modified: Thu, 25 Apr 2024 18:54:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe102e240c33e34bcee4cd97969ecf86f3a4845e4a64ef0ba8e10b4a51f9e9ea`  
		Last Modified: Thu, 25 Apr 2024 18:54:46 GMT  
		Size: 19.6 MB (19639613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
