## `julia:rc-windowsservercore-1809`

```console
$ docker pull julia@sha256:1246fa60321b0f4df42f779c841a0c4ce12187faa86f32432954cb5d517eb993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `julia:rc-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull julia@sha256:3db76a9354a5eb9b3bf518c4f57f62ad6f6fef50949dfb52efcdcee0f57c394f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2457179763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9cd32b07ad68346efc12397ffe8af0a2fe1ae09e0bdf5c1bb95eee1226429db`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Wed, 09 Apr 2025 00:53:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:53:26 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Wed, 09 Apr 2025 00:53:27 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Wed, 09 Apr 2025 00:53:28 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Wed, 09 Apr 2025 00:55:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:55:05 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe338ffedab6c27d930e9352eedcf7347a212f6ba18ef90a2cc6ec3a7b305f6`  
		Last Modified: Wed, 09 Apr 2025 00:55:09 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35cb18073cb9ab10b99a91c4e62d737879da7fc774eea93271986bca77d2b20`  
		Last Modified: Wed, 09 Apr 2025 00:55:08 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc5398e765de9925d3e7ac3db7de1fca7c904d0ad4a458c84e2a7f188990bf3`  
		Last Modified: Wed, 09 Apr 2025 00:55:08 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151ac6cd9e20abd3c396bf5d0a93fd649d8db76e9913a5cde132af624ceddd11`  
		Last Modified: Wed, 09 Apr 2025 00:55:08 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d9f6a0e31f6ccf7a070b353d35eb9cd4945bb1f8dab9cb165f21686978220cf`  
		Last Modified: Wed, 09 Apr 2025 00:55:47 GMT  
		Size: 294.4 MB (294447430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ca78691bba9232a2e7c5f02cdba68c1f7c5ef9be33546acb869d8533f8c6b4`  
		Last Modified: Wed, 09 Apr 2025 00:55:08 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
