## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:abaeaa13d6e4a1dc3e6c6fc8daf40f6277234856a531dfb642a7cb7e62c9cd52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6414; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6414; amd64

```console
$ docker pull docker@sha256:0a1d2647328a5d7345d5629270770b989f2c7768181c83325942cd89e067aea9
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1960588156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3af4d7092f9d6273e29e855460990c60c96df5efb01eba5b94c474f495baf2e6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Mon, 04 Nov 2024 22:04:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:06:09 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:06:09 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:06:10 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:06:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:38 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:06:39 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:06:58 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:06:58 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:06:59 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:07:00 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:07:11 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9180539f0878e6e9a22347c0c53933007658d4098666dea7656c5c94fdab13f`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b3f4c14fe4ae112eea0e12a8d914b20e740b50daa01c1ded89b3090ccc17d6`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 486.1 KB (486133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3352ba51ca22547049bc53b6260b2bf1bdd0e6e8c18beca1396faf8604a56fb`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66da5a3e191fa08f89aa0d45f503068ecbffd1d5256172a4be411a3b60652e4`  
		Last Modified: Mon, 04 Nov 2024 22:07:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:008892b68904102745a26d0ea805b6e5f65aefb5e86902c439cafb7f208e9553`  
		Last Modified: Mon, 04 Nov 2024 22:07:17 GMT  
		Size: 18.9 MB (18883136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45390ca0b1420a5bed894f140737685becc355e971a102d7c7710afa76c3adeb`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3eb4d33e81e187c21e2ed7ff812dc398e941c1698f3269261fa0a9de4a20b`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21368c2d17f4914b1f07e4932c557acbab2f0c47ffb2d432f5415d140d9e882d`  
		Last Modified: Mon, 04 Nov 2024 22:07:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9b340f151c54bc2044a44bbdb991189dc58a7c9a88cc16e9ad2473f99bde5c5`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 19.4 MB (19403987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e1e7e4b67806f9bc8f5ed9222bb97bb3d3c352a3f0df91a4cbc39b32df7764`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ffe9dd5fd1ca6794334ca733716595a715d56dbcf45241a409377ff826f8f2`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9c57e4ddd42379cb676060924ff571236b382e6e67a1b8038aefa2740849d03`  
		Last Modified: Mon, 04 Nov 2024 22:07:13 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7032051664667397bdbb39f6c19703d98e185b07cc753c33eafabb09557981b1`  
		Last Modified: Mon, 04 Nov 2024 22:07:16 GMT  
		Size: 20.0 MB (19977973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
