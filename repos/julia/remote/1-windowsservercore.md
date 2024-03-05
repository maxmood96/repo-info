## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:32bdcd5ec58ae1a8a8a91e462f7e09bdcc1a64b4a9dd35f8f441a3f39368dca8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2322; amd64
	-	windows version 10.0.17763.5458; amd64

### `julia:1-windowsservercore` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:7b73929fae2e04d2dc25c81f1dbfe790d86366991e47ece1a8c6e3220f7e789e
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2160647547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:833323d352b7c7442566e640f21563b21a501c2d6a9573a8deb48ad4838660b6`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Tue, 05 Mar 2024 00:49:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 00:49:31 GMT
ENV JULIA_VERSION=1.10.2
# Tue, 05 Mar 2024 00:49:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.2-win64.exe
# Tue, 05 Mar 2024 00:49:32 GMT
ENV JULIA_SHA256=5ba6bac56753f4fffe18390721816680f1fdf268b6bae920179a24fe5d588c4b
# Tue, 05 Mar 2024 00:51:38 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 05 Mar 2024 00:51:40 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:855fa6b82f2f8fea22646f0d4aa228ea8cbb8bc562afd14a163a8f3d0eb010e1`  
		Last Modified: Tue, 13 Feb 2024 18:28:53 GMT  
		Size: 522.1 MB (522055371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62c9bdfe4d2ce71a5ddebfba7210ad882022e7cc08e53074b089156ad9fd2ec6`  
		Last Modified: Tue, 05 Mar 2024 00:51:46 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f024063f35db82df064a1870ed8ce0b246e47354b3ebd2667c8892acfbe23e7`  
		Last Modified: Tue, 05 Mar 2024 00:51:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:115e836f7876d43bf98e18e374c6e43445cb975bd8e77314a6fdd3947d274233`  
		Last Modified: Tue, 05 Mar 2024 00:51:44 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6b8292736e7de561daf099c63655e8ad6d6e775bd779925a82c1359017b0b3`  
		Last Modified: Tue, 05 Mar 2024 00:51:44 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf2c6646da00f8f70dc32c1105c626de05863442b36ce5bfb64735e95537d15`  
		Last Modified: Tue, 05 Mar 2024 00:52:16 GMT  
		Size: 250.0 MB (249986905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d219e3f66cf0a79523e39ba46cdf5d3d83b1abb31263a4b7c466232f11c643`  
		Last Modified: Tue, 05 Mar 2024 00:51:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.5458; amd64

```console
$ docker pull julia@sha256:e3ab5ff643f73dfe0d44ccdee33dc16ac619ea72af75c8261e5f38614ee21e47
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2330426397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c1368cfa1ba157f9d0d168d3a80afd97a861791cb41541d17ee6c191e71d73a`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 04 Feb 2024 04:14:09 GMT
RUN Install update 10.0.17763.5458
# Tue, 05 Mar 2024 00:49:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 00:49:34 GMT
ENV JULIA_VERSION=1.10.2
# Tue, 05 Mar 2024 00:49:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.2-win64.exe
# Tue, 05 Mar 2024 00:49:35 GMT
ENV JULIA_SHA256=5ba6bac56753f4fffe18390721816680f1fdf268b6bae920179a24fe5d588c4b
# Tue, 05 Mar 2024 00:52:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 05 Mar 2024 00:52:24 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda007680e5cddfaf6f5428f70f8c514ac0b9dd099972b7d475cce4c5c899558`  
		Last Modified: Tue, 13 Feb 2024 18:23:52 GMT  
		Size: 429.8 MB (429828428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a1ab1c30c313f1a8225c21251b3cdea88eb8782e535dbcf3b3da759d7d35315`  
		Last Modified: Tue, 05 Mar 2024 00:52:31 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1d38736dc1a157784110b169e2f5d1d23f54881f54c132b51dd3d8e1cdb4cd`  
		Last Modified: Tue, 05 Mar 2024 00:52:28 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d43a7649908b8dc7f44cfd5dc263b8b5b4a8461997a8c07ce155978efec7f072`  
		Last Modified: Tue, 05 Mar 2024 00:52:28 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cc33e40deaffca94f644a33d3cf54e996d3836fe021bd7d57b6966fd656a9a`  
		Last Modified: Tue, 05 Mar 2024 00:52:28 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:536fe5e06cbaf6d7410a969729c209ee4bc88d4dcbb5b6cf1ed962cfef169b7c`  
		Last Modified: Tue, 05 Mar 2024 00:53:01 GMT  
		Size: 250.0 MB (249971146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936af997e752803da179cc6d50143e80aadb4a9bbb6548948736cf19d53649ad`  
		Last Modified: Tue, 05 Mar 2024 00:52:28 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
