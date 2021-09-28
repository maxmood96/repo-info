## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:e7778348c44df852f65ca02a9436caa8ab3483eb5951087631c8cdbf51b94a99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.230; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.230; amd64

```console
$ docker pull julia@sha256:446379706a11e60dd6bc46a72ce63925920caee9a341a1a7e33bfd29ffbbd852
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2259208413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984a68f2eef42b09aaf0a118ec11ac89ac5c2d12e0ce0e24c330363813431332`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 08 May 2021 09:40:24 GMT
RUN Apply image 2022-RTM-amd64
# Mon, 13 Sep 2021 07:01:40 GMT
RUN Install update ltsc2022-amd64
# Wed, 15 Sep 2021 12:20:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Sep 2021 02:14:32 GMT
ENV JULIA_VERSION=1.6.3
# Tue, 28 Sep 2021 02:14:33 GMT
ENV JULIA_SHA256=bc43b8729dd2d95d9d148ada989c8582a66e99af89fcc91d8ed41ee2f13a9985
# Tue, 28 Sep 2021 02:16:04 GMT
RUN $url = ('https://julialang-s3.julialang.org/bin/winnt/x64/{1}/julia-{0}-win64.exe' -f $env:JULIA_VERSION, ($env:JULIA_VERSION.Split('.')[0..1] -Join '.')); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Complete.'
# Tue, 28 Sep 2021 02:16:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:8f616e6e9eec767c425fd9346648807d1b658d20ff6097be1d955aac69c26642`  
		Size: 1.3 GB (1251699055 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:48a76b150a3a1ee8efbc87797c38de66d24a71421fce2754695fed8227d4cc3f`  
		Size: 873.2 MB (873175411 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3fda9a0667b0cb96fa50df6568908c70087df9372ac60c91c1ba417787ee1faf`  
		Last Modified: Wed, 15 Sep 2021 12:59:54 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cc9e5871cdea85a363bf71d5da6f1b3f64f466f6e0fd6059b1dcb48b2bafb73`  
		Last Modified: Tue, 28 Sep 2021 02:22:26 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:408b6c842cdfa2e86202d5012854850f4bfcb9fe38f3ddefde354cde85f3c1c5`  
		Last Modified: Tue, 28 Sep 2021 02:22:26 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11956d4e120e73f24d9f46be0654f612dbb70668c25d951d74c9058ade56402a`  
		Last Modified: Tue, 28 Sep 2021 02:22:56 GMT  
		Size: 134.3 MB (134328247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbab9a73bb683567b45239dc3e1d63ac2035f4a7124e13a74614b095ea715748`  
		Last Modified: Tue, 28 Sep 2021 02:22:26 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
