## `julia:1-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:c69620f4af2834775aa29ef48c8e99e594e09e6b6cfb8ce28a8eb455973267d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `julia:1-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull julia@sha256:f646c262c693923078dd1367a8892bf9f82e257360efd5d10672d0201a780f02
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3639145989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda9a693e86e998532ec21e54d9a5602e6a069083f23ba1df78fb28fd01aaeca`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Tue, 09 Dec 2025 20:35:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:35:21 GMT
ENV JULIA_VERSION=1.12.2
# Tue, 09 Dec 2025 20:35:22 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.2-win64.exe
# Tue, 09 Dec 2025 20:35:22 GMT
ENV JULIA_SHA256=b8c6ffd3f760e088820f0f208b799167a02d528df467337852ffcc599eaa8e7e
# Tue, 09 Dec 2025 20:36:59 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:37:00 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62c64c7dc565d03eb3e9f39894e67ad9fe74d54f61e84975b3f57b9f2972a79`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66fdedb62e9363240d1648636c3f97dc5c9695d52cb30e1bdff0f88d750d47e`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc37f0905d73ef1b5ac18675b08df9f750e89fa97ccf7f10ac44e6a412b2c64`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69d45161174a9487b09781f63981fefc9959ff659c2f61f30c615180c879e225`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efed2071fb98ca5345ad7ccc3118e0972f266521b883de458c2b8c1d08d98b33`  
		Last Modified: Tue, 09 Dec 2025 20:45:21 GMT  
		Size: 386.0 MB (386019029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6395f80ded2d1defcb8360787857a8b0e66c0742878fa7c61faf7b12d849cf59`  
		Last Modified: Tue, 09 Dec 2025 20:45:08 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
