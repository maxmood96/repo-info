## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:59fb363a93cf0e1e97db5de6e53d0679e48f07f37c514add05f7930edb146a14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.825; amd64
	-	windows version 10.0.17763.3165; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.825; amd64

```console
$ docker pull julia@sha256:f69c9bf069ececc6d9b244017e78a66d56f3781f0b3a7345e2228094659c5224
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2460153604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0292a7024e1d0d6fcac924dd1fb1d0f2e91b5fe62dbda6193bcf03e4ec3e777b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Jul 2022 19:15:56 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 19:15:57 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.0-rc3-win64.exe
# Mon, 18 Jul 2022 19:15:58 GMT
ENV JULIA_SHA256=fd861d6c4a97f5319cbb5a4b508fc16fc3aaacbe113fa5cbe31b37fa00e4f18e
# Mon, 18 Jul 2022 19:17:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 18 Jul 2022 19:17:32 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e73b3b8f6da6afb1a5493041710bddf5235c0fec8dcc2ffb3e79ab2d28ba0c`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab7128d15a612012fee5edfe7c8c7e4e3ac5903c6bbcb274bd39669fd79b91e`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ba394c9ef183c1f69545fad25a946eb3dd5da3f7dcecebdcd6a4e69f227cff`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33570793b612bc509b94ba4f6c7d0c6a290e1a9371dd67556de5fa3b861badb`  
		Last Modified: Mon, 18 Jul 2022 19:22:22 GMT  
		Size: 159.9 MB (159914919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19186e3b06a4dc04c883be9db2fd4d830ecc9e1515feeac10109d3edf4d5d033`  
		Last Modified: Mon, 18 Jul 2022 19:21:44 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.3165; amd64

```console
$ docker pull julia@sha256:f715778ac965c4dd477b2b0fa0562904f7f132d3fe7dbead63aeabee2d8e50ff
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2831689977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81ded5843fc58f3ddd08b2ce57be07041699dcfaecf367c2b5b964475cb147ff`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Wed, 06 Jul 2022 22:37:15 GMT
RUN Install update 10.0.17763.3165
# Tue, 12 Jul 2022 19:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 18 Jul 2022 19:17:39 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Mon, 18 Jul 2022 19:17:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.0-rc3-win64.exe
# Mon, 18 Jul 2022 19:17:41 GMT
ENV JULIA_SHA256=fd861d6c4a97f5319cbb5a4b508fc16fc3aaacbe113fa5cbe31b37fa00e4f18e
# Mon, 18 Jul 2022 19:20:18 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Mon, 18 Jul 2022 19:20:19 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7aca8de30754f19fe03ee4c21eed0762efb5e91bf684b0cc36cc92b2af13446d`  
		Size: 794.9 MB (794877652 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:912efe6370f7047e630e1f70d9201e3143571e3ed1fe50a1e61754d2d536ea95`  
		Last Modified: Tue, 12 Jul 2022 20:21:55 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01b4e97a338ebae8595c5fbbd57d88a74fe7beb584b9891bef16e7d9c3f4dcfd`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d675d547bb1946edda8fab0d35eaa9541bbcbd6e002aee1eb62025d7bf7e7eca`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:292ed2e65b39804dc581777c92aa01bfb8c3e6fb255a0880d4ac79e444121218`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87edb9d9009ed02be7d5d8c813db0daa41c6bd3098653d4d8b3a1fb0f997aeb`  
		Last Modified: Mon, 18 Jul 2022 19:23:10 GMT  
		Size: 159.6 MB (159639126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c0b87b16b9b6d5dd243f03ac900202d7c8d5568074be1509a1574065d29df5`  
		Last Modified: Mon, 18 Jul 2022 19:22:34 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
