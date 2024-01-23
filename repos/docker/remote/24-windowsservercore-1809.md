## `docker:24-windowsservercore-1809`

```console
$ docker pull docker@sha256:ae9c06433d434919decac2303badc19e0f6bca0e36f6658986ad34a366b03b55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5329; amd64

### `docker:24-windowsservercore-1809` - windows version 10.0.17763.5329; amd64

```console
$ docker pull docker@sha256:db0b37276d819cefa9d4585e8642fcbc7a7ce9a76e98fe3ac8b40527326d6847
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2124883472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818faeb366365c1584e222bdf48979fe0a45722629a14857a9809f33b833738`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Mon, 22 Jan 2024 22:50:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jan 2024 22:52:28 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 22 Jan 2024 22:52:29 GMT
ENV DOCKER_VERSION=24.0.7
# Mon, 22 Jan 2024 22:52:30 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-24.0.7.zip
# Mon, 22 Jan 2024 22:53:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 22 Jan 2024 22:53:04 GMT
ENV DOCKER_BUILDX_VERSION=0.12.1
# Mon, 22 Jan 2024 22:53:04 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.1/buildx-v0.12.1.windows-amd64.exe
# Mon, 22 Jan 2024 22:53:05 GMT
ENV DOCKER_BUILDX_SHA256=0ff0853a09960ff8f454d5db7253d5d935f5538856ea4985a276cbd1b28a96a5
# Mon, 22 Jan 2024 22:53:31 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 22 Jan 2024 22:53:32 GMT
ENV DOCKER_COMPOSE_VERSION=2.24.2
# Mon, 22 Jan 2024 22:53:33 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.24.2/docker-compose-windows-x86_64.exe
# Mon, 22 Jan 2024 22:53:33 GMT
ENV DOCKER_COMPOSE_SHA256=8402473653066beefdd602acb227f399cdae11a328ac3ca5feead826992c31b0
# Mon, 22 Jan 2024 22:53:59 GMT
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
	-	`sha256:0e364f3702d54a750da337509d0efd3f9aa795f703f7fb82e0d92f9469aa4c0b`  
		Last Modified: Mon, 22 Jan 2024 22:54:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d077e7c679bfcbe769ec04730da3a30707fba4b985dffdd44907addea93e089`  
		Last Modified: Mon, 22 Jan 2024 22:54:09 GMT  
		Size: 514.3 KB (514270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46062bed3afad84e4431af7fbba381bca8b99c27b8dbc1e86eb0680ba437c028`  
		Last Modified: Mon, 22 Jan 2024 22:54:08 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d166100aea4845d42ce459d418763bba6b51128758f15801c968829f5630e9`  
		Last Modified: Mon, 22 Jan 2024 22:54:07 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c7d21e198ab40168a54bcf4451bcc326279c2d2553b4c4d67b2f752d8b12d1e`  
		Last Modified: Mon, 22 Jan 2024 22:54:09 GMT  
		Size: 17.6 MB (17550515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b55513ff0de477c7f0549b69aee93796a29cfa292300ddfde7efedaa447b40e`  
		Last Modified: Mon, 22 Jan 2024 22:54:05 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd675d8301d4b7e883ac4c3564619ac7567ac057aefaf2825e34bae607a8770`  
		Last Modified: Mon, 22 Jan 2024 22:54:05 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1358df094bd87b4677963c69fa1a5808de9942fac16e5ebdd1c5bf4ac6dc59`  
		Last Modified: Mon, 22 Jan 2024 22:54:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae8970af9e67ee55dfca50a6c52aefec05fa3533672c1e8fd73214bdc7ff1975`  
		Last Modified: Mon, 22 Jan 2024 22:54:06 GMT  
		Size: 18.0 MB (18039218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b053e2fe50713ebed2853d19b81dc5c485c8607f94134c0746b28e438c4633`  
		Last Modified: Mon, 22 Jan 2024 22:54:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb31b6354e21cd95b1a6f4080215f4198cb6bdbee40e7f64ac66bdeac245a53b`  
		Last Modified: Mon, 22 Jan 2024 22:54:03 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28dc05664c43363134e86e0bba8d157390d9740543a702c1690a82fdc2ddd63`  
		Last Modified: Mon, 22 Jan 2024 22:54:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d59032a95d6221f98622b7fdde4bd15d291592acb5478cdf0a666ef030839e`  
		Last Modified: Mon, 22 Jan 2024 22:54:06 GMT  
		Size: 19.0 MB (19045296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
