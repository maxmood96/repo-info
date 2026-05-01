## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:5cdb5683e1301ab6717fa1959bb5d40cb7447055debe3a78647b36199ce176c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `julia:rc-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull julia@sha256:c590f899ed104cf6158eddf2eb78da0f3e5c102a9dff2dec786895065e804ff1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2442240085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5a9647855291ede84e16b8477842e75bf302cbf01b616283dcb92914f444ea0`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Fri, 01 May 2026 06:37:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 01 May 2026 06:37:01 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 01 May 2026 06:37:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Fri, 01 May 2026 06:37:03 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Fri, 01 May 2026 06:38:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 01 May 2026 06:38:51 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5a4a841b47f6d4734f84a9ffed102b568d8e2d220d024bfa81dc5aeda8a49d`  
		Last Modified: Fri, 01 May 2026 06:38:56 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be7c1fd979f6a35077064e62b96d99e70f140889855c4e8fb52b422ef12b1ec6`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0461eb154063a8ac7ab115f219831ed1a35a12e51977adf3ed4930f6456afa`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4ba19f31709312a8d90f582bbb24fc6fa4cd2936efd015c04b48f7f2c7f86a`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfdf0d7e5784d994cd1084d5c6c9985054706b4d75fcbc53f3f78d3cc0fd1717`  
		Last Modified: Fri, 01 May 2026 06:39:41 GMT  
		Size: 312.2 MB (312247516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:876c564356126a71e10b62ce8ff07af5cd2d6b6b80c97c4f51b36ac033003971`  
		Last Modified: Fri, 01 May 2026 06:38:55 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull julia@sha256:401ad7585973d604032c1b9799a9a1fb852ed7811ab8526b4f38bcac9284c4ab
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2382523826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd18ce4a7e34a140a51c9b47b6d839f2eceaa1977ef7d0322f4d02a12204d02`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Fri, 01 May 2026 06:34:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 01 May 2026 06:34:35 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Fri, 01 May 2026 06:34:36 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Fri, 01 May 2026 06:34:36 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Fri, 01 May 2026 06:35:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 01 May 2026 06:35:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77be2f9c243b0e263c88ca2d726022040687be630dcf57393cc6b22b4185dbf`  
		Last Modified: Fri, 01 May 2026 06:36:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e932476babec9ee83f5a230f626301da45f76fac5cf900af2c2648cbfc2b5a`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e7a7358644a33dd8cff75bc9310d43243c6391a7112dcf15fd1ef85c3047e72`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c14313f3dab02546408316191117d691fb0555f1bd46b60e37b44f496717d5`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383535af7e630d3f2db2832c2c8e141e0298958ab5dba981083f1c8091e4fe7d`  
		Last Modified: Fri, 01 May 2026 06:36:42 GMT  
		Size: 312.3 MB (312306104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3752c15d2e0e0040ccb2d4d90be4c5a921452d943fc6793c3f1336a82bc4f90`  
		Last Modified: Fri, 01 May 2026 06:35:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
