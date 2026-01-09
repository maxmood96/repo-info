## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:6db2cfe8bdbaa0deccf3340655e2c1674b3ed5176a6b6ed493202bc7a32bb851
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7462; amd64
	-	windows version 10.0.20348.4529; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.7462; amd64

```console
$ docker pull julia@sha256:3812efd7cda1f33f17589be8fed11480dde73ffb2a83afcde0fc53c71ae14d5a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640512766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3067b45c167a3153a3a45711a7d022900ed5d21e17b7da3dcb86ce3b2a5cd9b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Thu, 08 Jan 2026 19:06:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 Jan 2026 19:06:59 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 19:07:00 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.4-win64.exe
# Thu, 08 Jan 2026 19:07:01 GMT
ENV JULIA_SHA256=6b0e030497bd1abc0c12054105e70f0c5600f312be1dadd728d9b6624f9f8940
# Thu, 08 Jan 2026 19:09:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 08 Jan 2026 19:09:43 GMT
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
	-	`sha256:d126de1694a43d0102a4b151fadbf540a854e91ba7bd0acc8c78c53874728b7a`  
		Last Modified: Thu, 08 Jan 2026 19:25:01 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f66e44154192550e92a284d5674c77bcdea0477bc64f226edb46370cbffdb81`  
		Last Modified: Thu, 08 Jan 2026 19:25:01 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e819a62c3a1471c27d528140f81e81e17b7b299eb0d8049b399d06c84e7d16ea`  
		Last Modified: Thu, 08 Jan 2026 19:25:01 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3f9407a3698dd2472c340ea451a05c01d922a4f920bbb1d51928109beaaf78`  
		Last Modified: Thu, 08 Jan 2026 19:25:02 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a75bde047c6a14ad49c470208b7ac4712cd4aa8bcd9c199a80adf07a51dcd6b5`  
		Last Modified: Thu, 08 Jan 2026 19:25:24 GMT  
		Size: 387.4 MB (387385755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453ded3a3e51e437a30ef6b3707dcab798b1a26797612484da544e71c271533c`  
		Last Modified: Thu, 08 Jan 2026 19:25:02 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.4529; amd64

```console
$ docker pull julia@sha256:93c9ee5b6de1057aded6e9f1de2c52ccddede5676ebaafb3fb0c2ff04bfd0eb2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2167349380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88388e5d18b5a3673edd7b202632b12ef2bcc69d67f0605dab480f37721ad97e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Thu, 08 Jan 2026 20:57:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 08 Jan 2026 20:57:35 GMT
ENV JULIA_VERSION=1.12.4
# Thu, 08 Jan 2026 20:57:37 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.4-win64.exe
# Thu, 08 Jan 2026 20:57:39 GMT
ENV JULIA_SHA256=6b0e030497bd1abc0c12054105e70f0c5600f312be1dadd728d9b6624f9f8940
# Thu, 08 Jan 2026 21:03:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Thu, 08 Jan 2026 21:03:58 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Sun, 14 Dec 2025 00:17:28 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60080bcdf91ac82d9335a1c9800f8aaa099ac4ac23b90a4054a48927c3a26993`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55c359ddfe0fd68cb005cd7e0bc4b03dbb728a55cec9d56cac3f95c7cbbd27be`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1b658395a5475e656d6091f6f0278cfdb8875b9c97f6d9c0df90a1587a99b61`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e136e007a6f13a679296c716b7c77ba21942c30f1aaf4d904e479e82b9ace14`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a6e003b6310cf9296a6e6035dcc2d11c0800e3286ca12418ba62442601e2831`  
		Last Modified: Thu, 08 Jan 2026 21:15:47 GMT  
		Size: 387.5 MB (387463550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e96149f0052c374567d3ddf528b36cc9e385b7545890288eedb58b4a7aa2229`  
		Last Modified: Thu, 08 Jan 2026 21:15:34 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
