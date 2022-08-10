## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:25f923ac8ecbff42de82940f1cd3d0112d8b56fc4c04703ba5526cf6f63006e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull julia@sha256:bb45a32322f4fbc1db68b8fdc3feec344afb6c494166dc0909d9dce472e75bd9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2822655153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c71ce1fa11e94e9f82d7ed9988f476705764339d691dd4beca08c287fecb89a7`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 12:16:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 15:16:32 GMT
ENV JULIA_VERSION=1.7.3
# Wed, 10 Aug 2022 15:16:33 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.3-win64.exe
# Wed, 10 Aug 2022 15:16:34 GMT
ENV JULIA_SHA256=ef5915eaf35bb71359072e8c41f84fa73f1059fecb198e7fc838270d4ba5bbae
# Wed, 10 Aug 2022 15:18:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Aug 2022 15:18:18 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:294d77ac553d7210b662d07674ef9e39a6c2e88dc15b9d2788d51e509bc8b54e`  
		Size: 800.5 MB (800546641 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d64f32398ff5e4ac4cbab317ffed87a2fbf4e4a37210284dba19f2929d631a95`  
		Last Modified: Wed, 10 Aug 2022 12:42:57 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a97af06224427b44d011043445b52a6ee8aa210397722cb1a8fcf225827edfe`  
		Last Modified: Wed, 10 Aug 2022 15:24:55 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1406de16af7a0f20bebb16a3d4765b2106caa5a64bb62f2a3fe6456426113bc`  
		Last Modified: Wed, 10 Aug 2022 15:24:55 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0af281c3bf83ebe5c5e8f56717d2e78ccfc9cfbf55abde4ba290e8af83eaec7`  
		Last Modified: Wed, 10 Aug 2022 15:24:55 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87813d724011911b73799a61fbeb9654187960145f29e217aa982564018db81b`  
		Last Modified: Wed, 10 Aug 2022 15:25:24 GMT  
		Size: 144.9 MB (144935799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3df50fd7784a7e03f4c7f04d5a6fc3b1506260690862e48c86c9a99a2fbbe9`  
		Last Modified: Wed, 10 Aug 2022 15:24:55 GMT  
		Size: 1.3 KB (1306 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
