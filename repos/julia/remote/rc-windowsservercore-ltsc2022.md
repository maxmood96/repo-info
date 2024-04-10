## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:34afafb4646ab0d440a76cf77422c5b90b254e88c9ea81d1cbfa5b40feddc498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull julia@sha256:c88e20d5b96948a1701b3e66c312b8a8239a07ccbec5ae116f69c57dff9ca10e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2251410968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10850422c60f90e030d20f6920b2733b80a398b2a969361eeb4a362e936ce0ab`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:59:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Apr 2024 23:59:02 GMT
ENV JULIA_VERSION=1.11.0-alpha2
# Tue, 09 Apr 2024 23:59:03 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha2-win64.exe
# Tue, 09 Apr 2024 23:59:03 GMT
ENV JULIA_SHA256=acfbe50c378e3e0d6dc967525b5886edd5ae61ef3de85130343db378dfe88b0d
# Wed, 10 Apr 2024 00:00:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:00:11 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0fb179a3d784ee6d4ee555ce2c9dbeb19de4a69c8146bd605283788491857d5`  
		Last Modified: Wed, 10 Apr 2024 00:00:20 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31699d5271eff157c95c94e14cc49b4600db1b860462c91dfcaddbfde663e4f8`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82746ae8de4daa8e3f6aa1e7f409e969875d112d4a4edccaf6c29969606ec78e`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98787512b898e7eeb7c7c7d02cd4410839cf296247a34a4e36b30874eac9ec69`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:347bb455d9d3442fec2a6415a7f32b4f3d26e4a1e6e5b694403cebc3e193e701`  
		Last Modified: Wed, 10 Apr 2024 00:00:50 GMT  
		Size: 252.0 MB (252030847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c97ea9ab392191910f516e7d972257dea92f14bfb8296499788b0181ba6a7829`  
		Last Modified: Wed, 10 Apr 2024 00:00:18 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
