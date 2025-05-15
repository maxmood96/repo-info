## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:d7f007281ff122310f225c4ce859044e19559e33e870f15a5b0ff23967759fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull julia@sha256:41adc4eb1742d8c329b90920d988a19e5c718c788911d900e0f41943f5621afb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3716298354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:231971b8f3529dbec2a2df6f3a235f6eab07cf24850732a15738e0214599e1c7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 20:54:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:54:59 GMT
ENV JULIA_VERSION=1.11.5
# Wed, 14 May 2025 20:55:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Wed, 14 May 2025 20:55:01 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Wed, 14 May 2025 20:56:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 20:56:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:394acb6e6be3193b6b2a574a196451b348ac5cc42e27d53df835538a8b733416`  
		Last Modified: Wed, 14 May 2025 20:56:14 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50b22d881bdf539d03aa0eeb5e798eb6aa50c2a15eb50f7866b2165a3e9e749`  
		Last Modified: Wed, 14 May 2025 20:56:13 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3004fb68859327c588d416b46979e1b93b0f8e07740ae76229cbd8635b5fc1cd`  
		Last Modified: Wed, 14 May 2025 20:56:13 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba76f9867c3075aabc59cc9ba153184321ab6e907c71fd021bde82ad44bc108c`  
		Last Modified: Wed, 14 May 2025 20:56:13 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c18907759e96fb77fcd7744515f2fc56dfafbe638300f73b77d3aae1a00d2b2`  
		Last Modified: Wed, 14 May 2025 20:56:55 GMT  
		Size: 285.5 MB (285526036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d396b2d2562da806ab45a73419fc5e84fe6fdef83d88bff6bd16f634db4cfd3e`  
		Last Modified: Wed, 14 May 2025 20:56:13 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
