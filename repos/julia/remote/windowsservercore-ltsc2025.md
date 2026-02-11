## `julia:windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:9aee6820dd68dc70a8eaecb88501170ed4a78ee9dd5a1d905c0d20dd9898f8b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `julia:windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull julia@sha256:c7699b36a57db797c74e7459d068e62fa62e11562768b3e204db9cd6c71ab396
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2352108932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3876915edf35719373868dbfe147397f129c460c70e8ef0d3b8939ca9c0f068b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:52:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:52:55 GMT
ENV JULIA_VERSION=1.12.4
# Tue, 10 Feb 2026 22:52:55 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.4-win64.exe
# Tue, 10 Feb 2026 22:52:56 GMT
ENV JULIA_SHA256=6b0e030497bd1abc0c12054105e70f0c5600f312be1dadd728d9b6624f9f8940
# Tue, 10 Feb 2026 22:54:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:54:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c9a7b1ea2d51cf301948e0c8a3e4ba1f32df5bd596839458d89680e01fb3546`  
		Last Modified: Tue, 10 Feb 2026 22:54:47 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1136e38a282d294c9e78411cee3ec23ea6e7517d37094546b029b36b92dcb8da`  
		Last Modified: Tue, 10 Feb 2026 22:54:46 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed052be7357ce6eda29f336057f1f7f6cb1bdea8ed2d9333248f98c0d7d33527`  
		Last Modified: Tue, 10 Feb 2026 22:54:46 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf1259783e1bdf64e85bc35f85ddde7fcff8a3fbfc59d6ac915885ccb683ba9`  
		Last Modified: Tue, 10 Feb 2026 22:54:46 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ba90b86e1058738f0054043999035a117ae0e53fd154a0cce4e3f534385976`  
		Last Modified: Tue, 10 Feb 2026 22:55:44 GMT  
		Size: 387.3 MB (387342521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28899097a237bd71c20cdca58554f9d614c4a184a3f2eeb6328959bb5378d350`  
		Last Modified: Tue, 10 Feb 2026 22:54:46 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
