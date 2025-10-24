## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:fa10c1c8c32867203dde7a7be57b7e184bda0c46e4bfd0fa4054e4abd8ca9d5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull julia@sha256:e235c339a9c3a9d01b2637b4a66fc6e3a3820adca59f44baab7a11c47e38dbc3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3605103870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a53c104d92911fdc99bed1914540bbe298fdd96b0c6a0b9b0c8a08b5281be19`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Wed, 22 Oct 2025 07:45:25 GMT
RUN Install update 10.0.26100.6905
# Fri, 24 Oct 2025 18:12:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Oct 2025 18:12:26 GMT
ENV JULIA_VERSION=1.12.1
# Fri, 24 Oct 2025 18:12:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.1-win64.exe
# Fri, 24 Oct 2025 18:12:28 GMT
ENV JULIA_SHA256=a0f8a9edf07f2904261df99d451c614bbbb98c123b36769cb774ed9ce753c993
# Fri, 24 Oct 2025 18:14:10 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 24 Oct 2025 18:14:10 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c754a6aa9f16aa1c4d70f2ffa463bbd24a85c1acd69772fb9ea2d810f69847`  
		Last Modified: Fri, 24 Oct 2025 13:36:02 GMT  
		Size: 1.0 GB (1005039853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f3190565a49c015f5e55cf7bc0bd3597dbd44b12291bf03f9f3dbf71908f4e`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7788d42ce86ecf855514e53e1fc8e0489b792b82eec2b8128a89b1fa280e109d`  
		Last Modified: Fri, 24 Oct 2025 19:07:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872531f7893569f066b270fd87043e569842b4b9c13b5a0d7bebaa118e14875b`  
		Last Modified: Fri, 24 Oct 2025 19:07:16 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0957b3bd3a3855fad61deaa833e76630ca8f8bf0703860db5f8465569c08b2af`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8980bde7d495e8fb8f029b98cc010b0d2441ee638bc17632d7ed246bd3b36bc`  
		Last Modified: Fri, 24 Oct 2025 20:04:00 GMT  
		Size: 384.8 MB (384750320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a69307ba5b6b74e2601cd11796b327fd31e2daabdce920fd18f6657f1b1128c5`  
		Last Modified: Fri, 24 Oct 2025 19:07:15 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
