## `docker:25-rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:4568e11d94466b937a88a60078b0fac7e7e1ceb28ffa61f5229807fcef9d1a6f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2159; amd64

### `docker:25-rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2159; amd64

```console
$ docker pull docker@sha256:45967101ed2cc33b107836380c407351436eda093b296bb8c62c29533eb3874d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1944605767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57a451c119659a11b7460b2964e26bf3d9f7b1ae7d8a9c37bf21d313e02f54be`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 02 Dec 2023 12:42:56 GMT
RUN Install update 10.0.20348.2159
# Wed, 13 Dec 2023 01:00:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Dec 2023 01:00:31 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 13 Dec 2023 01:00:32 GMT
ENV DOCKER_VERSION=25.0.0-beta.2
# Wed, 13 Dec 2023 01:00:33 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-25.0.0-beta.2.zip
# Wed, 13 Dec 2023 01:00:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:00:43 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Wed, 13 Dec 2023 01:00:44 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.windows-amd64.exe
# Wed, 13 Dec 2023 01:00:45 GMT
ENV DOCKER_BUILDX_SHA256=dcf01329368381fae8c24b494186a30d2f1c4adb4bef7a0410b4803e5bb1c352
# Wed, 13 Dec 2023 01:00:52 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 13 Dec 2023 01:00:53 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Wed, 13 Dec 2023 01:00:53 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-windows-x86_64.exe
# Wed, 13 Dec 2023 01:00:54 GMT
ENV DOCKER_COMPOSE_SHA256=7d3f56cc84838ca54c5f0e9c8a3645dd96030482d838663c367d93bc6c38dc05
# Wed, 13 Dec 2023 01:01:03 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7839fc47f6e056f9e09a214230f8b7115e69419dbc74acbbb1ad6bc0caa28862`  
		Last Modified: Tue, 12 Dec 2023 18:27:40 GMT  
		Size: 500.7 MB (500674814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1c8ef6e12dd57b8e5d68a53f215475baea4cb5f85d0f768d692ceb0e1bfd6c`  
		Last Modified: Wed, 13 Dec 2023 01:01:13 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201b2035a6f95d7f7f5390df457e2da0dde591a2d3e3004938ab5f22ddbc2fd7`  
		Last Modified: Wed, 13 Dec 2023 01:01:12 GMT  
		Size: 504.7 KB (504663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0856cce243a7b2e0747a6035ec36a55609e62fe46436f2a28e9665d6da899d38`  
		Last Modified: Wed, 13 Dec 2023 01:01:12 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1650aeff58afc263affeaeb8b35b6ff2a8c3b228328cf4f310adad4638247f2`  
		Last Modified: Wed, 13 Dec 2023 01:01:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f5425878edc5f149aff19abebc085ec79f14b89e1336ed3fb6fc921e9e4255b`  
		Last Modified: Wed, 13 Dec 2023 01:01:13 GMT  
		Size: 18.1 MB (18071030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:013571ecf03e325577cb89a7aea8bc0e7f9cf1269a820ef5f208499d3be949e7`  
		Last Modified: Wed, 13 Dec 2023 01:01:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cf3a535c02f1243e4fa9b6e185ddf1ddf161c34190ae8b039c766f133cb6be`  
		Last Modified: Wed, 13 Dec 2023 01:01:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e8317fb0b2cfaebeed1c2b592b50798ce9cd1d2a2e8f8f7fa343205f3e747e`  
		Last Modified: Wed, 13 Dec 2023 01:01:09 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68f4904c9e0c2ae4cfc9e56dd3dae66a87d6793b864439e2b2b2769e3a71d417`  
		Last Modified: Wed, 13 Dec 2023 01:01:09 GMT  
		Size: 18.0 MB (18029963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c371011bee429fc4dba87ff0a49fb7f42da5a1a87be53feeb8898f14d169f76a`  
		Last Modified: Wed, 13 Dec 2023 01:01:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429cbe09b45d612ec0dc7dd7d6c458943f7b4cc567c6bc50f5a33c83e6cbbfd8`  
		Last Modified: Wed, 13 Dec 2023 01:01:07 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eca4b20a5d4c573f7479e70087e8988bb018800fc9bac5118d361b063bb96e49`  
		Last Modified: Wed, 13 Dec 2023 01:01:07 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:612ef2d446e97cb93363c46dfb0d2e226830c89f5db445ae4220b938e060f605`  
		Last Modified: Wed, 13 Dec 2023 01:01:10 GMT  
		Size: 18.7 MB (18714877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
