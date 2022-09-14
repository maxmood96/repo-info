## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:f21df5147ee24f953f369cca1661278da236866aeb2351a84d5afcbe0dc47a2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3406; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.3406; amd64

```console
$ docker pull julia@sha256:8085d9e38187ecd0227c910077d3c39c8ba264f93e98b872c5dfb265f96a267b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2863840764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f8b8793b7c384aab74c52340da604e5d474230b4b899a9e7078f398746c8e93`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Fri, 09 Sep 2022 22:43:02 GMT
RUN Install update 10.0.17763.3406
# Tue, 13 Sep 2022 18:21:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:04:55 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:04:56 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:04:57 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:07:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:07:34 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cee64bf279e2ca8e924884a10ecb98bfa79c7f0cc8d25e73039b9aeb940815b6`  
		Size: 826.4 MB (826398623 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2bc395c8c47e61e593d2e905e0e051d40e7d25e4aeac7dbe08d3ec57acd0e68f`  
		Last Modified: Tue, 13 Sep 2022 18:25:24 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726a7fa050422b140994888c3ee8f06178e789dfcacf2ff3a16b177c55193cfe`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c36ead5353e095555b2ed8c9023f3438fb137ab52027d139c5ee4c35ca9c0c2`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4d274278b614b2c1ab6de605de948dae8839931f04ffaae21a0629855a2428`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fd7540aff3d0e979977da933bff2be1430e5a1c14cf0e254aa973a449506899`  
		Last Modified: Wed, 14 Sep 2022 15:36:38 GMT  
		Size: 160.3 MB (160268991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f1301d66a0c3c1c29c6ac3d664094a6b25ffeacac8ba910bc25ee57cc0c2018`  
		Last Modified: Wed, 14 Sep 2022 15:36:05 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
