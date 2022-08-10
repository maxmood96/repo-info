## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:a7dfdcdcd9e1d43eb9863ebc0395faee0baf8ee86f6a4cbf541eedd449e9aeb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3287; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.3287; amd64

```console
$ docker pull julia@sha256:12fa7ba87cbd1bade1f50f2cfb4289257f1b0abd8fc7423e3b795276e227a4c6
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2837334732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe628fd92a5e119864948c23b1410b8c223fff8b877590c891284d4f1d78d50a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 06 Aug 2022 18:30:32 GMT
RUN Install update 10.0.17763.3287
# Wed, 10 Aug 2022 12:16:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Aug 2022 15:12:33 GMT
ENV JULIA_VERSION=1.8.0-rc3
# Wed, 10 Aug 2022 15:12:34 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.0-rc3-win64.exe
# Wed, 10 Aug 2022 15:12:34 GMT
ENV JULIA_SHA256=fd861d6c4a97f5319cbb5a4b508fc16fc3aaacbe113fa5cbe31b37fa00e4f18e
# Wed, 10 Aug 2022 15:14:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 10 Aug 2022 15:14:41 GMT
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
	-	`sha256:e73a313fd2c2cce56609e84053c0ba671a43bf3312273b1abc83724add347f2a`  
		Last Modified: Wed, 10 Aug 2022 15:23:23 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75e018da640b1d4c0c31eef60b965f698a0d6fce4889f5c618c9290fa6290b8e`  
		Last Modified: Wed, 10 Aug 2022 15:23:23 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30cd4d32d6970c7be80ec373b02a7e34f09c373601f18676dd6378c212f1d4f4`  
		Last Modified: Wed, 10 Aug 2022 15:23:23 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b970273330d6f622dc4b3ec4b7d1c313144628bfc06ee81d3a8625100dd12ffc`  
		Last Modified: Wed, 10 Aug 2022 15:23:59 GMT  
		Size: 159.6 MB (159614883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab59657049ad13a6ee688e6db4cf27dd5db99b450a7eea90e1d6f538d33d35d`  
		Last Modified: Wed, 10 Aug 2022 15:23:23 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
