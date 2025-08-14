## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:bbaec6d3abee70522c8dc899a00eebcf557e9118c1e7ae69bc0d3a72c0a543be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4052; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.4052; amd64

```console
$ docker pull julia@sha256:2423a742978fadfcfc4bfd263bfa254579004cffb27854ff7adfad112d2b3406
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2564527164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f15b4689849c394e4f51c0e5f6a5187d3aeb80f32e6244da1e8f7c77c18ff8c`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 08 Aug 2025 18:40:34 GMT
RUN Install update 10.0.20348.4052
# Tue, 12 Aug 2025 20:26:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Aug 2025 20:26:21 GMT
ENV JULIA_VERSION=1.12.0-rc1
# Tue, 12 Aug 2025 20:26:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-rc1-win64.exe
# Tue, 12 Aug 2025 20:26:24 GMT
ENV JULIA_SHA256=34569cb903c4713787ee8f1b7ddb1a8c57e44f64b1312eb80635ca7041aab409
# Tue, 12 Aug 2025 20:27:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 Aug 2025 20:27:53 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06b9b30319b49e62edeeff59663c236bf6a406712417e8a1be70ae07afd76e2c`  
		Last Modified: Tue, 12 Aug 2025 20:45:17 GMT  
		Size: 819.5 MB (819499548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c3dbe92bff2ec3608e01f08651bb19d64ffdce32d71d699e0bc4327c66238a`  
		Last Modified: Tue, 12 Aug 2025 20:29:34 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4d76a623f03aabb0f9ebc4dcb352c4e08af1e75fddcd1b7be73a8dbc7f30a8f`  
		Last Modified: Tue, 12 Aug 2025 20:29:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3f3dac637660c67d2fbf58e208ec93b90007b71b1df14c08671322aa95afe3c`  
		Last Modified: Tue, 12 Aug 2025 20:29:35 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc762b2a4293f7f099167e8b2c72c1329e9618a7f8f7320815720f9a769158d`  
		Last Modified: Tue, 12 Aug 2025 20:29:34 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5cec9638edb591e025dea848ed08108af9e340e557241be7e34ca44eebb90e`  
		Last Modified: Tue, 12 Aug 2025 23:04:44 GMT  
		Size: 282.8 MB (282828777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99b8d840dbcc032ccaa1f0550c10570b2d78f789a9d61fc950c1b9d1701fdb26`  
		Last Modified: Tue, 12 Aug 2025 20:29:35 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
