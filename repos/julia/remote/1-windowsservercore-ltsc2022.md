## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:cc91138b8da18073cb65f800c851fd992881d9c0f177b10b20e7a0de12a92032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:73c5fb5073c4a2eb04f9ba64ffcb9f7ad98fcf76e8462408ae85f247bce32fa6
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714924818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07860c441218034ff48c3bda766ebe500e7b6abe20267aa8ac024f652413263`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 09 Oct 2024 00:01:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 00:01:47 GMT
ENV JULIA_VERSION=1.11.0
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-win64.exe
# Wed, 09 Oct 2024 00:01:48 GMT
ENV JULIA_SHA256=7de521dfc4b874150d4d2b3001fc1fdae4083a7a1b07c5d7704d00052b6c118e
# Wed, 09 Oct 2024 00:04:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Oct 2024 00:04:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d051df5d3d007cb93cc808ac0bd9d93ea8d34e023ca41606e7db0f793d32a27f`  
		Last Modified: Wed, 09 Oct 2024 00:04:17 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9632fbf45c9f159613540ed4a8e350bc0cdfc6ce300d7eea3822fc95c5287344`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be8bb7b00247043708cbc824d2e2daeddf800bf3da0e0caddec4abad1223fa8b`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07878319f8dade0b340746108fddd8aeba2cf0e73a617275daba714afd349186`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f21c1ee9f59b4c736bed5ca9b8edb8ce3c7acd0bfb28b3303703b370cae480`  
		Last Modified: Wed, 09 Oct 2024 00:04:46 GMT  
		Size: 252.7 MB (252725957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4711316193833de6e1632c40eada01b83f183c1194dd26e3a5225b3097db8df2`  
		Last Modified: Wed, 09 Oct 2024 00:04:16 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
