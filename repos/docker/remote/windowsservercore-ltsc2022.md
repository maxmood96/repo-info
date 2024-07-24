## `docker:windowsservercore-ltsc2022`

```console
$ docker pull docker@sha256:d97163db065c98e9c2f5892e2e8515a608c20db99f5dd3d269a3e9fb31be0e0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `docker:windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull docker@sha256:eac31321c5758e4659e54c8fea3ad8a13e5039f3ec93f0f5663e4cea321017d7
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2198106481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d08ea0bf426754030d643b1b8e1387bcc0c5e760582d61b3edbe778a9e6fd5e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Wed, 24 Jul 2024 01:08:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Jul 2024 01:09:53 GMT
RUN $newPath = ('{0}\docker;{1}' -f $env:ProgramFiles, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine);
# Wed, 24 Jul 2024 01:09:54 GMT
ENV DOCKER_VERSION=27.1.1
# Wed, 24 Jul 2024 01:09:54 GMT
ENV DOCKER_URL=https://download.docker.com/win/static/stable/x86_64/docker-27.1.1.zip
# Wed, 24 Jul 2024 01:10:11 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:DOCKER_URL); 	Invoke-WebRequest -Uri $env:DOCKER_URL -OutFile 'docker.zip'; 		Write-Host 'Expanding ...'; 	Expand-Archive docker.zip -DestinationPath $env:ProgramFiles; 		Write-Host 'Removing ...'; 	Remove-Item @( 			'docker.zip', 			('{0}\docker\dockerd.exe' -f $env:ProgramFiles) 		) -Force; 		Write-Host 'Verifying install ("docker --version") ...'; 	docker --version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:10:12 GMT
ENV DOCKER_BUILDX_VERSION=0.16.1
# Wed, 24 Jul 2024 01:10:12 GMT
ENV DOCKER_BUILDX_URL=https://github.com/docker/buildx/releases/download/v0.16.1/buildx-v0.16.1.windows-amd64.exe
# Wed, 24 Jul 2024 01:10:13 GMT
ENV DOCKER_BUILDX_SHA256=34b8bd302364e9df99ebcd86658eae6ade175baf8baf6e74123ae04fcb2675c3
# Wed, 24 Jul 2024 01:10:20 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-buildx.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_BUILDX_URL); 	Invoke-WebRequest -Uri $env:DOCKER_BUILDX_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_BUILDX_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_BUILDX_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker buildx version") ...'; 	docker buildx version; 		Write-Host 'Complete.';
# Wed, 24 Jul 2024 01:10:21 GMT
ENV DOCKER_COMPOSE_VERSION=2.29.1
# Wed, 24 Jul 2024 01:10:22 GMT
ENV DOCKER_COMPOSE_URL=https://github.com/docker/compose/releases/download/v2.29.1/docker-compose-windows-x86_64.exe
# Wed, 24 Jul 2024 01:10:22 GMT
ENV DOCKER_COMPOSE_SHA256=c80155bfd2669bcdc7482ae7ccf7ccaf6b5da2149b690d806c7a4d9200abc54e
# Wed, 24 Jul 2024 01:10:35 GMT
RUN $dir = ('{0}\docker\cli-plugins' -f $env:ProgramFiles); 	Write-Host ('Creating {0} ...' -f $dir); 	New-Item -ItemType Directory $dir -Force; 		$plugin = ('{0}\docker-compose.exe' -f $dir); 	Write-Host ('Downloading {0} ...' -f $env:DOCKER_COMPOSE_URL); 	Invoke-WebRequest -Uri $env:DOCKER_COMPOSE_URL -OutFile $plugin; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:DOCKER_COMPOSE_SHA256); 	if ((Get-FileHash $plugin -Algorithm sha256).Hash -ne $env:DOCKER_COMPOSE_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Verifying install ("docker compose version") ...'; 	docker compose version; 		$link = ('{0}\docker\docker-compose.exe' -f $env:ProgramFiles); 	Write-Host ('Linking {0} to {1} ...' -f $plugin, $link); 	New-Item -ItemType SymbolicLink -Path $link -Target $plugin; 		Write-Host 'Verifying install ("docker-compose --version") ...'; 	docker-compose --version; 		Write-Host 'Complete.';
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0340d8cecbfa7e015c70df007e94bc2ba065cf3f1932d0dd809322d719d1b35`  
		Last Modified: Wed, 24 Jul 2024 01:10:40 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54bcba1252e4cf2dfc44349442124994d7bff3e5f78424bb3fa2e58d394ba917`  
		Last Modified: Wed, 24 Jul 2024 01:10:40 GMT  
		Size: 358.8 KB (358758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a10e500ae735dfffac82749f41c9415b2a141d7a22cda61bf97fad7a493eaa1`  
		Last Modified: Wed, 24 Jul 2024 01:10:39 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f41521061a07dbe3183bac911d398e59246660fc11b97564b7496eec80cbe57`  
		Last Modified: Wed, 24 Jul 2024 01:10:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3262badd61f25c0ddd8202464dac219238a102272da1cbcece79d4c13d60cfeb`  
		Last Modified: Wed, 24 Jul 2024 01:10:40 GMT  
		Size: 19.3 MB (19251997 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dac15df8b493dd2fa9ff23051d2eec14ad68e0d655ac2801fe5e28767bd1870`  
		Last Modified: Wed, 24 Jul 2024 01:10:38 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5499bfb74c883f8373ea29ec8512a138af68b05576bafcf7948de807837c8c61`  
		Last Modified: Wed, 24 Jul 2024 01:10:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7fa4dc1eb28535ed4d3ce6495c236a0734aa49c956bbc4156d4ccb63df1f51`  
		Last Modified: Wed, 24 Jul 2024 01:10:38 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a0527915ec215f85e98c83b5725af36881145471716d1aa3befc2d82f948b03`  
		Last Modified: Wed, 24 Jul 2024 01:10:40 GMT  
		Size: 19.2 MB (19223909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99ddc31f46225dbb008a08598570e59c6929c6f11caaa6a67d3837a13c0bb72`  
		Last Modified: Wed, 24 Jul 2024 01:10:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4f6a7ed44e827856e618ad1c6e5a5a29452fb3e55ec2676e479902515100a3`  
		Last Modified: Wed, 24 Jul 2024 01:10:37 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3c97e0e2b9abaf3b8e72094403bd26fce2c38e76486825ae83988cd32fca3a`  
		Last Modified: Wed, 24 Jul 2024 01:10:37 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394bd02b128ee16d843083c80bcaa205f74d78e009623eca104f0df365601843`  
		Last Modified: Wed, 24 Jul 2024 01:10:40 GMT  
		Size: 19.7 MB (19659944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
