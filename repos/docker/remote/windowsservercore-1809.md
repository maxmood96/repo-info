## `docker:windowsservercore-1809`

```console
$ docker pull docker@sha256:288edc0140614db3e9f4b69aabb72919f88310fbe74972c612d3db9821df2759
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6893; amd64

### `docker:windowsservercore-1809` - windows version 10.0.17763.6893; amd64

```console
$ docker pull docker@sha256:dcf28587862b66f11c9152f0f07aba6549e6fc69ae5692187d8b81fd9632e2ae
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2199331794 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abaa563d895b666255230f87f1e8fe38b9731565871f357c861f66dbf2417f81`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 07 Feb 2025 18:15:33 GMT
RUN Install update 10.0.17763.6893
# Thu, 13 Feb 2025 00:30:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Feb 2025 00:30:32 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Thu, 13 Feb 2025 00:30:33 GMT
ENV DOCKER_VERSION=27.5.1
# Thu, 13 Feb 2025 00:30:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.5.1.zip
# Thu, 13 Feb 2025 00:30:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:30:43 GMT
ENV DOCKER_BUILDX_VERSION=0.20.1
# Thu, 13 Feb 2025 00:30:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.20.1/buildx-v0.20.1.windows-amd64.exe
# Thu, 13 Feb 2025 00:30:44 GMT
ENV DOCKER_BUILDX_SHA256=39f53ec70c6ce37beca6898809e8eb89a77a1651be35ea50b51629c7a5d3b1f2
# Thu, 13 Feb 2025 00:30:53 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Thu, 13 Feb 2025 00:30:54 GMT
ENV DOCKER_COMPOSE_VERSION=2.33.0
# Thu, 13 Feb 2025 00:30:55 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.33.0/docker-compose-windows-x86_64.exe
# Thu, 13 Feb 2025 00:30:55 GMT
ENV DOCKER_COMPOSE_SHA256=1324e382e1a79efaee4be288aae847f8a2862acf270d5621c17dff3a10d5ee83
# Thu, 13 Feb 2025 00:31:04 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3af2bd0a1965eaed07372d9df47eb5ee783273fad4e91a30412cdd07c198cc7`  
		Last Modified: Tue, 11 Feb 2025 22:29:28 GMT  
		Size: 416.6 MB (416640430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ddec09ce130898b858d868d863c38d0a59ad02d30317040c713bbcad470d7b`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5b18610111d087a831e8f8ee56836d6b68057470111cd634df6fbd5f7eefe8`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 333.7 KB (333660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b3085b676e07491e9c1eea56a888e0405ddf3aff207f0f8eee75b2201937c22`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e439965d4bb61c02ec64eb94d7cfe644ef8c059133cbcf266573b59d5ddfe7`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6714307851c701c6dbe14d976b4ed71dfa150ca4c45c6e0c9a64854f7d76ba86`  
		Last Modified: Thu, 13 Feb 2025 03:08:36 GMT  
		Size: 19.1 MB (19148895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e81914763a0ae26bccf9728612de0fc76384393d1a179879e256af8cce9b09`  
		Last Modified: Thu, 13 Feb 2025 03:08:28 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a65c219e06bfe9ca604cbde640314b8068a4d0feeaccbafd5f1857f31f72fa57`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bcc26bb2920298fb60914141b02f623bd84c3d2e8e5f800678259f8f46ada5e`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622ffa3a23b3c72d93e7700d2d2a621f73d09b371913c49a4b6bb7a03836df1b`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 21.1 MB (21125839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda2cb85d7567448d09f5063d50876774b50476e783a6228538b975f31a4c2d9`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2a862ff7c9cef485f0c7554c1dea61fe84ec9cd43825c10ee846c057f7e319`  
		Last Modified: Thu, 13 Feb 2025 03:08:29 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a00d05b58e6f9ed3e53e37132919f43c22ee3a79989ef8ca2be0428296cf49`  
		Last Modified: Thu, 13 Feb 2025 03:08:30 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50ddba2f9c71876169789e635349f235b35dfaf2447e05d22566cc343498165`  
		Last Modified: Thu, 13 Feb 2025 03:08:32 GMT  
		Size: 21.8 MB (21802955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
