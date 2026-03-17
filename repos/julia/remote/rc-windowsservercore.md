## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:135f16564ba75b8cfc711088956e17e32f52062106cf571ccef3bcb6cc244b3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `julia:rc-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull julia@sha256:82723a5251b34305774e6bcfb591ac8e2aeb82e95dd0b5139789f66f6f4cee54
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2392496983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a84f0c88888e4f40c3ea823785ab2c75c562bb005554b65593be134f3ce5f721`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Tue, 17 Mar 2026 17:43:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Mar 2026 17:43:08 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 17 Mar 2026 17:43:10 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta3-win64.exe
# Tue, 17 Mar 2026 17:43:11 GMT
ENV JULIA_SHA256=3ac4b3824830783ec9661cdbcca93875faea1c2ffb33568aeba1924e26466cb2
# Tue, 17 Mar 2026 17:45:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 17 Mar 2026 17:45:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d1c2ce2f27ffb6077908fa6292ca7dc54b4a8e61f8005acb358da8ef863d2a`  
		Last Modified: Tue, 17 Mar 2026 17:45:49 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e050118bc471de0e012aaa76dffe4fdb2109c671409e9d52fad345db6ed30d5d`  
		Last Modified: Tue, 17 Mar 2026 17:45:48 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9f0c2b4bd40b962bce4b88bffb05dae543f83761207a9096e05dff1de83e4b`  
		Last Modified: Tue, 17 Mar 2026 17:45:48 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed39dca27b5e7548d7507e2584844a2ccb870c96c3a502927627f99403bcda`  
		Last Modified: Tue, 17 Mar 2026 17:45:48 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19484f5a86b507e31ccec76f0ee807c2acd07ff490c8a42e9bb90932548df35e`  
		Last Modified: Tue, 17 Mar 2026 17:46:34 GMT  
		Size: 311.3 MB (311294398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965843dd101ee712b625f1b8d725c43ecb4a32866ae4680163fb7c83d291e3d3`  
		Last Modified: Tue, 17 Mar 2026 17:45:47 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull julia@sha256:51864206a6a750618a20db2a79162012afb1ae4f708b55aadb2ed88d8ad521df
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2293705592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2c34cfeb418e0b08183960b531dbfee95860448a40fce85947f5b5a2194ccb`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 17 Mar 2026 17:45:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 17 Mar 2026 17:45:14 GMT
ENV JULIA_VERSION=1.13.0-beta3
# Tue, 17 Mar 2026 17:45:15 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta3-win64.exe
# Tue, 17 Mar 2026 17:45:17 GMT
ENV JULIA_SHA256=3ac4b3824830783ec9661cdbcca93875faea1c2ffb33568aeba1924e26466cb2
# Tue, 17 Mar 2026 17:47:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 17 Mar 2026 17:47:44 GMT
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
	-	`sha256:26117b6ad3a47350d4334b6cd3202fc105adb14741b00113c3bf829d9dcd4019`  
		Last Modified: Tue, 17 Mar 2026 17:47:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813213f4b6ee08dbdffb17dcbe3313427f7d1e4faee61f9283129382b57d2423`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e24179a211b65135995fd9726b7e6f6245af633fc2f9b61af57bbc2408070c5`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fec5be4f0725c7d9918a025c419253fe8343dfb1461e8cd8803b28b5b28e2a6`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8659cf43fcfa5cf93d4df4740eedd56f682900baf106116ee34d046d60bfb436`  
		Last Modified: Tue, 17 Mar 2026 17:48:37 GMT  
		Size: 311.4 MB (311417685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7887c8b203340d29d1cac05bc5f78ff15c95fe4727325d1dbfb2e331c06cee7`  
		Last Modified: Tue, 17 Mar 2026 17:47:49 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
