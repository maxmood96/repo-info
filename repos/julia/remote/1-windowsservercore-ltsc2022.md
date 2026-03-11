## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ee0fd29ddd42ffa9d5674d615f5a97654183e73a98c3d192efb276be8b059853
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull julia@sha256:2523df2fefc3cdac6b1ca4d80d4a3eb4006b94691b8ecb3ffa086db506389ae0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2268662971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddfd09b82167aae284fb3e985932aac5b91ea9bb088012ffb40532090629e44`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:57:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 21:57:06 GMT
ENV JULIA_VERSION=1.12.5
# Tue, 10 Mar 2026 21:57:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.5-win64.exe
# Tue, 10 Mar 2026 21:57:09 GMT
ENV JULIA_SHA256=97c0cff9770baa823d40eb6f4f47fdfdcc3c48c609882354c01734f8abcd14f8
# Tue, 10 Mar 2026 22:00:19 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:00:20 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f982b44695c6c1cca851e9238aa8eceda2f7522e65a6a1df319239f66b3610fe`  
		Last Modified: Tue, 10 Mar 2026 22:00:31 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9871a58174f1cd722a0ec3647de218209df0947a187d6981d8979ea2155a0739`  
		Last Modified: Tue, 10 Mar 2026 22:00:29 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625ae8df47e2d602a7ef9b4204dbc089bee63d98012a5b175118a86bfbf5df1b`  
		Last Modified: Tue, 10 Mar 2026 22:00:31 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43687756026c65610073c0c5750d7c835e0da7feceb97d8600ca91a0924fe8b0`  
		Last Modified: Tue, 10 Mar 2026 22:00:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c591e4c452dfe9f092314df1a9546c6c03bcdaa65289fdf7a39ccc2bdc4bfa9d`  
		Last Modified: Tue, 10 Mar 2026 22:01:13 GMT  
		Size: 286.4 MB (286375022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278d1a6b9d0f22664afcf8ee0b517b7953e96f3fb7cf062854e64343e97d5e47`  
		Last Modified: Tue, 10 Mar 2026 22:00:30 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
