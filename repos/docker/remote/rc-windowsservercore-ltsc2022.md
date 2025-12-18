## `docker:rc-windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:96494b4483a012788da8d10009693dbd0f8338a7533d82b2f0adf1b414e9a967
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `docker:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull docker@sha256:05c368ec69feeedf5610aff9823ed8b949de198b2238ccfcccde7286c84f3c12
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1835177316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40f3c1a0dcf2c62f39622051c3bb735b4db16d145343c677ec1b3b259d5ce84b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Wed, 17 Dec 2025 22:21:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Dec 2025 22:21:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 17 Dec 2025 22:21:53 GMT
ENV DOCKER_VERSION=29.2.0-rc.1
# Wed, 17 Dec 2025 22:21:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/test/x86_64/docker-29.2.0-rc.1.zip
# Wed, 17 Dec 2025 22:22:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 17 Dec 2025 22:22:15 GMT
ENV DOCKER_BUILDX_VERSION=0.30.1
# Wed, 17 Dec 2025 22:22:16 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.30.1/buildx-v0.30.1.windows-amd64.exe
# Wed, 17 Dec 2025 22:22:17 GMT
ENV DOCKER_BUILDX_SHA256=3c48e2da717c55518cf22a5b372f48f54cf3a58c9fae675b818a3311775e1b71
# Wed, 17 Dec 2025 22:22:39 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 17 Dec 2025 22:22:40 GMT
ENV DOCKER_COMPOSE_VERSION=5.0.0
# Wed, 17 Dec 2025 22:22:40 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v5.0.0/docker-compose-windows-x86_64.exe
# Wed, 17 Dec 2025 22:22:41 GMT
ENV DOCKER_COMPOSE_SHA256=e8a5338e20bc6d30ae38db5533ce63ebf3c229801c20a74051fd06a650e5a8f9
# Wed, 17 Dec 2025 22:22:55 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15fbd97b1db2c11c6a83d2abe864c71bdad436420fa4b87cdddbc318940dfa6`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3daa6982734debb16d777f0da00327753680f264ec092909201f052ac9033925`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 501.2 KB (501175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:247517d9f44cc165729060fa0cb1c1e58af3c5c7801b6c9beb748880a74ce6f2`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e739d6e53c0deb5627b909a779ac38268365ff94202f3be105f7a04e592b92bc`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd15f4b120ad5f0164308ccae0f9761aa223b55fd4d567c3922b3e3aa7a643da`  
		Last Modified: Wed, 17 Dec 2025 22:32:40 GMT  
		Size: 19.4 MB (19426495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7da1f83517d9049bc971f329acafc5bec0dc92b59ab53fc4725288b139a11ffe`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f09773bfc442cc918e2e101e09d2a8b76fec46dc31e8a906e925dc0d13b14db`  
		Last Modified: Wed, 17 Dec 2025 22:32:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687912b954660a73d7eeddc2f2e559a6966e5f9af5101bbcc488a29211124e78`  
		Last Modified: Wed, 17 Dec 2025 22:32:38 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe20f5149441870cada28db557d2169cc1411984ad07ca19a4798e02342e8e6`  
		Last Modified: Wed, 17 Dec 2025 22:32:40 GMT  
		Size: 23.9 MB (23922490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50eaa937965704e12a2a2b56d356c10e29f32af2fff592387bcf405a5adc0033`  
		Last Modified: Wed, 17 Dec 2025 22:32:38 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501f5457d14a019dcd42840f47504e3dd6256197ca8c1f9bd157594d07b53bee`  
		Last Modified: Wed, 17 Dec 2025 22:32:36 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6c2a8e2d14fb9bc14690ee763365fc182c25cb621501556835269ed5c207e02`  
		Last Modified: Wed, 17 Dec 2025 22:32:36 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b684e33096cbec38221da883b0af0fcfc09ecac83a8cb6a657ce0b1f1a26701d`  
		Last Modified: Wed, 17 Dec 2025 22:32:37 GMT  
		Size: 11.4 MB (11436104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
