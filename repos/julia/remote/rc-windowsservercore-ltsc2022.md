## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d77fdc67bdc74829a3ecc8f798502c23d57e5dce7f2076410c8bc29918918bf7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull julia@sha256:214fd6284562b99272e531af29836f2bfaa1eb395577c40cb775f16626f8b20e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2174033131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b8b8228168a84fa6e08cb757dd42383bfe2c0169a7b93fa4a37b648ceb85754`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:53:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 22:53:51 GMT
ENV JULIA_VERSION=1.13.0-beta2
# Tue, 10 Feb 2026 22:53:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-beta2-win64.exe
# Tue, 10 Feb 2026 22:53:53 GMT
ENV JULIA_SHA256=bcba1c45109550ad6da10076aa32c7c40d83af41a751341b22bb0f3046111a11
# Tue, 10 Feb 2026 22:56:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 22:56:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d9712892c3b62b0941022f4bb1d3ee8d33ed7ba2adf3e7966feb097a46ea7a`  
		Last Modified: Tue, 10 Feb 2026 22:57:10 GMT  
		Size: 1.4 KB (1368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86743f981cfa9646ec800c3ae3423a7ec09940a81fb0da6c11c7eb4720a99052`  
		Last Modified: Tue, 10 Feb 2026 22:57:09 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99ce9c2f595468fa928dba5ddba1335e83d03eb95108eaee6dfd285421466738`  
		Last Modified: Tue, 10 Feb 2026 22:57:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bff2457365c38d29541b4e40ecdd8f850e7a236e911525d569204fec781de3e9`  
		Last Modified: Tue, 10 Feb 2026 22:57:09 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b960f4a14a2d0a61ef99175854abb007b1cf449ae40526dec10cc7dca67c9f97`  
		Last Modified: Tue, 10 Feb 2026 22:57:55 GMT  
		Size: 311.4 MB (311369357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5815f6a1dc1bd258f7d316610e0071e7ea3124d0cf19045e39dd872bddc6db5e`  
		Last Modified: Tue, 10 Feb 2026 22:57:09 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
