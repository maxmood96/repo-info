## `docker:rc-windowsservercore-1809`

```console
$ docker pull docker@sha256:897056f86fcfaa539389fe49085088e972bbaf926026ae074df39dbfd059ae18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `docker:rc-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull docker@sha256:80b5460ce7c073a352022d4779e463c7ce6c7135ebcbfdb0357341415d6624b2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2248999838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5287560491ecdba0147705c8eab70e27fa4da959c2acc8f307e35b97fcab36`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 21 May 2025 18:52:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 21 May 2025 18:52:50 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 21 May 2025 18:52:51 GMT
ENV DOCKER_VERSION=28.2.0-rc.1
# Wed, 21 May 2025 18:52:52 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-28.2.0-rc.1.zip
# Wed, 21 May 2025 18:53:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:53:03 GMT
ENV DOCKER_BUILDX_VERSION=0.24.0
# Wed, 21 May 2025 18:53:03 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.24.0/buildx-v0.24.0.windows-amd64.exe
# Wed, 21 May 2025 18:53:04 GMT
ENV DOCKER_BUILDX_SHA256=8dec102c8eb14f434707cc05a8f0e366c090ded6ad74d9c5f8a64a9c0b766140
# Wed, 21 May 2025 18:53:13 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 21 May 2025 18:53:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.36.1
# Wed, 21 May 2025 18:53:14 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.36.1/docker-compose-windows-x86_64.exe
# Wed, 21 May 2025 18:53:15 GMT
ENV DOCKER_COMPOSE_SHA256=0291c2f108655128dc36005d0c703869d9d98a1d403ed9bb8719356b9e5f2704
# Wed, 21 May 2025 18:53:24 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02cd9ecb4783184f0f8066184b845d7ccd229b4697c49aefb4c5b00bf274f85e`  
		Last Modified: Wed, 21 May 2025 18:53:33 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e80f1a52b0526972b316a694465248fbc1b764f31c742a66ab9c496d6712e936`  
		Last Modified: Wed, 21 May 2025 18:53:33 GMT  
		Size: 374.6 KB (374645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0422ba1599a2f60608e4b8ebd8278976fd9f9b0ec072c7976724bea9b358448a`  
		Last Modified: Wed, 21 May 2025 18:53:32 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8ba00207166380abadd97d6959a79a383711ae45c9dea93011cadbf476fa529`  
		Last Modified: Wed, 21 May 2025 18:53:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84b9f27689919945411185e2fca547cbc225ec5d566be37c2173f69be1200f02`  
		Last Modified: Wed, 21 May 2025 18:53:33 GMT  
		Size: 20.5 MB (20470381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f368b28356aac5ae2cf16508aecbfe75be440e793a5d3c255055da4ec06d119`  
		Last Modified: Wed, 21 May 2025 18:53:30 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d90eacfd946d5a5206606ed1cabde824a17eeae64b8ac68049cae679bfccded2`  
		Last Modified: Wed, 21 May 2025 18:53:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28304dfe649d9f377cde9902b25127b7e60836606ad6dff33b87d2a0e6acf02f`  
		Last Modified: Wed, 21 May 2025 18:53:30 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4114fa6594030822b65aba522697ce0a30c73ab4778ae86b9384f0708d5424ab`  
		Last Modified: Wed, 21 May 2025 18:53:31 GMT  
		Size: 22.3 MB (22277593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc6a91474d8aad759566c70185d03b4fb70bd06dc6b61b1581226843533e8a3`  
		Last Modified: Wed, 21 May 2025 18:53:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19947b9ecd02212141da9e653fa1af8d58e22ff286c35369268f50c77c8bb00d`  
		Last Modified: Wed, 21 May 2025 18:53:28 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26646e154e6f57595e08f1dcd971a1d42274ecdc6f57a73d7a60fa8bce81541a`  
		Last Modified: Wed, 21 May 2025 18:53:28 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1931e55347cef22880403f1757ee98c01ca0620c3bda8993f6259fa5bd2ff396`  
		Last Modified: Wed, 21 May 2025 18:53:31 GMT  
		Size: 22.1 MB (22148142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
