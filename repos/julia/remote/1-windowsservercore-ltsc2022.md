## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:ed23dc439f38a107790c3ad2c5b8006df13f2ab4a707e87391f6c635b948acea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull julia@sha256:29d44f8029955f9d0bd1de5cdeb16fc4b0548bb2200ebd7ca84aeea3df4ee82f
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2538239672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375a9c380a4ece14ecc08215300d76e42b8cc16e3760cffc09ebbf64718c751c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:32:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:32:58 GMT
ENV JULIA_VERSION=1.11.2
# Wed, 11 Dec 2024 20:32:59 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Wed, 11 Dec 2024 20:33:00 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Wed, 11 Dec 2024 20:34:07 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:34:08 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda9c04397413f58315de3553f61712659cf2f1ed06145c66e1231ed413a9f00`  
		Last Modified: Wed, 11 Dec 2024 20:34:15 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:597ca1d00160a4eb64ea9e2f32cc0c8bb26b789809229f03b76a3f85fec4fb0f`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35879923f8ac58a45b212252065761bb73266a76b06f3185e4caf47a4e84aea2`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9fc6234b2d5752df9a6df8c80ddbb0ba89edc16968c57f0d5faccf0e3895e7`  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81ce2b63af24e51695aac4c1260b86492b3e63a61612c4afee293de1c0f0ecdf`  
		Last Modified: Wed, 11 Dec 2024 20:34:49 GMT  
		Size: 284.4 MB (284359584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8808becd035284a49d4035cc0c4682a647642722ad225bba0902d38b18cd6c96`  
		Last Modified: Wed, 11 Dec 2024 20:34:13 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
