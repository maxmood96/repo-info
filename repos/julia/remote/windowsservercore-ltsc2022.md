## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:2b2995ed38b982712f74f153474777c3a75fca2c0e1108e5668e92084c453b22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull julia@sha256:59930ae7595b5fdc16c9a293f0abc122d8fc364e7d8ce3e5c2a5f7e6756cc1b5
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2186661998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a13e44a2fb7920601877a5f2970aba1300712c4c313e9758624323a0d3ada1b8`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 30 Apr 2024 21:49:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 30 Apr 2024 21:49:51 GMT
ENV JULIA_VERSION=1.10.3
# Tue, 30 Apr 2024 21:49:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.3-win64.exe
# Tue, 30 Apr 2024 21:49:52 GMT
ENV JULIA_SHA256=688e746f3d8700ba44a6cbc9ce04ccead4cd921f093af80259e10d0b0c5448c8
# Tue, 30 Apr 2024 21:51:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 30 Apr 2024 21:51:27 GMT
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
	-	`sha256:5a0162462ac8e21912c4dc6bc583bc0aa396ff310924c75020c1dd5d84b9444a`  
		Last Modified: Tue, 30 Apr 2024 21:51:34 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a01808be12ea6d8e666ac4e0ba27b4ed29bc28a6d6b79db67a1334deed40c4d`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727834c38ea41d07307df22346e629e1225460d20dc9c0644572832e69a5146b`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbea072db9d21283d89d47d81f570013db417eeb9bc2fb2b7c70b901b43eeb4a`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc8af169f1f4f0df080fe9e7c20110e16b37fc0e9e41064126570dd27140799`  
		Last Modified: Tue, 30 Apr 2024 21:51:55 GMT  
		Size: 187.3 MB (187281919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e494cdbacd2fb13126efb6e606c12c63a3c4c9995b6808dae3ecb156fc7715`  
		Last Modified: Tue, 30 Apr 2024 21:51:32 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
