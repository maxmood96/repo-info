## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:37a34fdf7f6850604b9e0d4389d906e91e0413acfff5c5535614fa23c10241ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3770; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.3770; amd64

```console
$ docker pull julia@sha256:df6108b84bb7e6a1ccd2510f5f06e2a009c19c112b64b485b460d4b5b9e239e9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2935248934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aad39e7721258d80d6ba9f16a04954960530910acec4b5f878f8cc1515b88ce`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sun, 11 Dec 2022 08:04:49 GMT
RUN Install update 10.0.17763.3770
# Tue, 13 Dec 2022 22:48:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Dec 2022 03:40:56 GMT
ENV JULIA_VERSION=1.9.0-alpha1
# Wed, 14 Dec 2022 03:40:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.0-alpha1-win64.exe
# Wed, 14 Dec 2022 03:40:57 GMT
ENV JULIA_SHA256=b9cf18544d67e015fc8679e10deac29bef56758f1a88021ed485b5719bca7eae
# Wed, 14 Dec 2022 03:44:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Dec 2022 03:44:07 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:a48a3e4ae2de839d8e99bde16eb91d113fb2cf889bba472d0c4274851b5fb402`  
		Last Modified: Tue, 21 Jun 2022 18:30:17 GMT  
		Size: 1.9 GB (1924269350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f3ad73ed772f80ab7923579a55dd12fb9b6e090d1d836408d16ffd9d3dee252`  
		Last Modified: Tue, 13 Dec 2022 23:56:47 GMT  
		Size: 856.4 MB (856427878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc9debb9503ac53c2f64685982eca56ac5110ea6baf7278b27af54ab8fbc409`  
		Last Modified: Tue, 13 Dec 2022 23:54:25 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dea490b61c44af4b7ed058a6b0577efd1e54029a30afacf26c4415225169510`  
		Last Modified: Wed, 14 Dec 2022 03:56:34 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44fab40c1e715c7c644acd0538d5e0879be3ce8835d2feb65a7a1115ea87d15`  
		Last Modified: Wed, 14 Dec 2022 03:56:34 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fb4a62a51e44a7e73041b75beadfa8017dd92602f08e0e29020af833a9b4fb6`  
		Last Modified: Wed, 14 Dec 2022 03:56:34 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8879321ba0b35abb48e581ab01a078a35f0fc853910c7bb79e4ff5c181071d`  
		Last Modified: Wed, 14 Dec 2022 03:57:12 GMT  
		Size: 154.5 MB (154544606 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b05c069239144bba42a4e9c3fa369bf9090d912c6c72e02e0cf9298230896a16`  
		Last Modified: Wed, 14 Dec 2022 03:56:34 GMT  
		Size: 1.4 KB (1407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
