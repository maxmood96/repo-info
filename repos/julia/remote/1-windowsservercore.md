## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:5ba56e049b8e09c7a05d0620b12a3121e98ce39ac100b6df6b14e151dde32fd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1129; amd64
	-	windows version 10.0.17763.3532; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.1129; amd64

```console
$ docker pull julia@sha256:842af2050b524ff0617af7ee25afd39c2d700cbe70b0e7245c6de1ea0a6f4e1c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2574828626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5715da4b05a763b7634e93b864f70c2b00d06e3e850422006ba0bfe7bcb73028`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Fri, 07 Oct 2022 22:13:48 GMT
RUN Install update 10.0.20348.1129
# Tue, 11 Oct 2022 20:20:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:02:32 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:02:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:02:34 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:04:02 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:04:03 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ab91661ce2a2a2c14684a2ba0f543a81d7896773f88200b31be0e37c589de38`  
		Size: 979.4 MB (979359717 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:15e15cecc9c7498ee7335091ed603347777bb2f7810e8b701327779faaae1712`  
		Last Modified: Tue, 11 Oct 2022 20:34:44 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7221a25f4e4cc5717362c07d9bbd208a47cf06481aba440f2f80e1a890d279c8`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c5343334074f75755c9d117ee7db9143f963f6e2a1c7b56784d14f03ab25800`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe5a8ffb3874e523fcef6e6030c1661a7b188f4a60823d7637633b6c40cdd09`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a132b821df963f4235db2aa9b1696fe6bd79448c2d3a5b79fdeb7621d2c1c4f`  
		Last Modified: Wed, 12 Oct 2022 15:11:26 GMT  
		Size: 158.6 MB (158598180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc097456b7d16fe526e62620c12338567d8847eac97a6c76a72107b1c210593d`  
		Last Modified: Wed, 12 Oct 2022 15:10:53 GMT  
		Size: 1.4 KB (1438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.3532; amd64

```console
$ docker pull julia@sha256:dad6fc6ed11d150fe2395b5f52e2c09fc10268f6e7b54199caf7d6d7bd154039
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2869514021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f2d8b8e8fb2ef7755de2816e1c35d666aa3bbdf48c77d1091d1b363bdfc0989`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:04:14 GMT
ENV JULIA_VERSION=1.8.2
# Wed, 12 Oct 2022 15:04:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.2-win64.exe
# Wed, 12 Oct 2022 15:04:16 GMT
ENV JULIA_SHA256=248af521126dcf25364abe9e6bb875df836da232b9408e49dcdbfe8105054557
# Wed, 12 Oct 2022 15:06:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 12 Oct 2022 15:06:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67379414393984276933f1494d7d41aeda14519f9aa8d6d5023637609aaacac5`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0396669edefa15e6b365767408e0dc26922be8d55973e231cf0d966aadb67092`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cace966b134b3e9c756a96411f52eaf49e1d414b004ae48632b8b7da0ec16165`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9783bbd1f10b0d919fa1c4ef10e0f5d7d080f166b8d941447d772c3ea8b0d0`  
		Last Modified: Wed, 12 Oct 2022 15:12:13 GMT  
		Size: 158.3 MB (158342967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf4bfdf269aea874d95cecf9039053143ee16fb6ac63f983abb6e6bc452e3af7`  
		Last Modified: Wed, 12 Oct 2022 15:11:41 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
