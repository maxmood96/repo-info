## `docker:27-windowsservercore`

```console
$ docker pull docker@sha256:9920491f2ef7ea58eb44b9081c71f6b0b377e156429480e162d2da1a35709c9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `docker:27-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull docker@sha256:c8aa4fe546c608c397c121187d89bc56ea3d9737443405876c1ef9d2acb4b05b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1858142020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4411154f7c2d251f560e0da541ddab796f6fee7a12d0eee01c6bf7bbf3edc6`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Mon, 04 Nov 2024 22:03:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 04 Nov 2024 22:04:14 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_VERSION=27.3.1
# Mon, 04 Nov 2024 22:04:15 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.3.1.zip
# Mon, 04 Nov 2024 22:04:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:28 GMT
ENV DOCKER_BUILDX_VERSION=0.18.0
# Mon, 04 Nov 2024 22:04:29 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.18.0/buildx-v0.18.0.windows-amd64.exe
# Mon, 04 Nov 2024 22:04:30 GMT
ENV DOCKER_BUILDX_SHA256=85f9218497427f8a1d4e09fa73b7133b555f8017cffc24c4ffc9640668b61dca
# Mon, 04 Nov 2024 22:04:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Mon, 04 Nov 2024 22:04:40 GMT
ENV DOCKER_COMPOSE_VERSION=2.30.1
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.30.1/docker-compose-windows-x86_64.exe
# Mon, 04 Nov 2024 22:04:41 GMT
ENV DOCKER_COMPOSE_SHA256=bf29dcf1b35cf226ca0fe337d0de903060ec50855eea5c0eb54739e3c3c3fa5a
# Mon, 04 Nov 2024 22:04:51 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ee01e199a2f24e8b6b493c7367a13ddfae6bba887e466c01ad020d2524bc5a`  
		Last Modified: Mon, 04 Nov 2024 22:05:01 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2bbb9fdbcc87bfb4b93de3c0cdae83c335e9f7dbc06d098d192e52bafabe50`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 492.1 KB (492079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ebbb20ded945183fd4c14656b19cda045f5b7e97bb07f22b9843e50895f43f`  
		Last Modified: Mon, 04 Nov 2024 22:04:59 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f968ccc0dac3674bd61466b0204370379096fb7357ab18f5657b0bd96f2cc72`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db93b3cff5d285cbe387f545603057efda45b74dd0b03b2994f021ce6e5c871`  
		Last Modified: Mon, 04 Nov 2024 22:05:00 GMT  
		Size: 18.9 MB (18889070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43876228572fd4804ce70ac9c566ac1d193206a3ea2d121a1e830f9d0c0fa73c`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:602105bafc75282867b0569c543c716118673ba5e5ca0f4e52fd6cfd5d55bd33`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.4 KB (1350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a078c599f2a3701b122a8fd2b8924fbeabf9b5dd4ceeee5247bc4eae9b988d6`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:864c90fc0fd7fe7cc190db57aee11560a7f3148518ae59c477b9500175aaa116`  
		Last Modified: Mon, 04 Nov 2024 22:04:57 GMT  
		Size: 19.4 MB (19413058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e5f8dea2b99b1a1c06346aa7d434e05c39e531fc9a0771a1a42eb7d5b300741`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86fa469fc9ccf873529283ea129bc855ebff8a8fc727cc1a97da3dc40791299d`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65181de9a5a0c56771fd37894a1db0360670b93d58280e39fe9a08e7a9288114`  
		Last Modified: Mon, 04 Nov 2024 22:04:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4d4dd212468a9d7f2c6ace60eab51374804cdcd5337f5de1fabf7a928190b55`  
		Last Modified: Mon, 04 Nov 2024 22:04:58 GMT  
		Size: 20.0 MB (19994513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:27-windowsservercore` - windows version 10.0.17763.6414; amd64

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
