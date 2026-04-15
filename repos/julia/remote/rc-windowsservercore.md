## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:a45c6d14f95ef7e6ed15f1f575ff713d7662a92013ba317bda79e8492b7eb57a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `julia:rc-windowsservercore` - windows version 10.0.26100.32690; amd64

```console
$ docker pull julia@sha256:cd356f3bd4adae0b2f20e7a8074d195ef78fc5c148dfff3f009dc00c331c7bd0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2441261125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a47e53127fccc136081551dc652ec5576c0546a575e19e86e4bafee349892bd`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:02:12 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 14 Apr 2026 21:02:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta3-win64.exe
# Tue, 14 Apr 2026 21:02:14 GMT
ENV JULIA_SHA256=3ac4b3824830783ec9661cdbcca93875faea1c2ffb33568aeba1924e26466cb2
# Tue, 14 Apr 2026 21:03:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:03:43 GMT
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
	-	`sha256:8132c872e75f25bfa323300a3940e534262afa9775f557483dcc1c0951ee5277`  
		Last Modified: Tue, 14 Apr 2026 21:03:51 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58ce03cff593f5ffdfe78a631828f585b37926da1d15a573ec326da6d3ce4cc`  
		Last Modified: Tue, 14 Apr 2026 21:03:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:211839a564eaa7d69899f7c6d03e5269dc03e069cf77a42d388feefe5244397a`  
		Last Modified: Tue, 14 Apr 2026 21:03:49 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4e4280da3c754de6894e8584577c16094060c59e6ccdc519f1c1b85ee2a25e`  
		Last Modified: Tue, 14 Apr 2026 21:03:49 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e012fe490095d062ef94fb6652501b16419088fa2c7bbaac424a662180d1c021`  
		Last Modified: Tue, 14 Apr 2026 21:04:32 GMT  
		Size: 311.3 MB (311268542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:419896aa0cf70a9ade8b92e56843d37362cd76d5c2369850bfa918598c46830d`  
		Last Modified: Tue, 14 Apr 2026 21:03:49 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull julia@sha256:240861a3fe018dcda4c258507796f45d0832263c9f3d0df3aa0622fd6f0ce7b6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2381606189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8c415061582093a63f2eecd02ca84ee03368b9f79760aacdfb880e81cc077a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 20:56:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:01:23 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 14 Apr 2026 21:01:24 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta3-win64.exe
# Tue, 14 Apr 2026 21:01:25 GMT
ENV JULIA_SHA256=3ac4b3824830783ec9661cdbcca93875faea1c2ffb33568aeba1924e26466cb2
# Tue, 14 Apr 2026 21:05:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:05:15 GMT
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
	-	`sha256:4911c7412282b7f1d93fad64ba92d82b42d1ac47c62c4ff886b516f02ea28a55`  
		Last Modified: Tue, 14 Apr 2026 20:57:50 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e7762b8cf3daccc32da0cd659390e53f10dafbc133b9c8211dc0c6c9f7ce23`  
		Last Modified: Tue, 14 Apr 2026 21:05:25 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266366992f0d4ab627f18cd30330fda0d0c390ad42cf45dae725b5f27855c391`  
		Last Modified: Tue, 14 Apr 2026 21:05:25 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f9a30f9a8859244861f532d203ca9ce5f237a9c049b757a375e5759d946b59`  
		Last Modified: Tue, 14 Apr 2026 21:05:25 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6285f072db10b869a4b5a2b7d0f20159fdde0ac614107830c872d0d8a12e9d`  
		Last Modified: Tue, 14 Apr 2026 21:06:09 GMT  
		Size: 311.4 MB (311388364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77b9f7b789aaec1bde55536f689f3ccd0130a824015a813f91b26683c47a2bf7`  
		Last Modified: Tue, 14 Apr 2026 21:05:25 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
