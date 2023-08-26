## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:bfa7ca0a9722278fcaef1e970abe09f629bc3afa2a39afeb6e29e944e11df386
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull julia@sha256:e34fc33d763c0214566aad9b5c90c10ec72b65e6b5a8fd0b8547d1edcab038dd
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2157669890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84f0e1848529280db865bc64af24ecb56bb5b7727cb7263a039561b78c465183`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 02 Aug 2023 09:07:15 GMT
RUN Install update 10.0.17763.4737
# Wed, 09 Aug 2023 23:36:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 26 Aug 2023 00:21:13 GMT
ENV JULIA_VERSION=1.9.3
# Sat, 26 Aug 2023 00:21:14 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.3-win64.exe
# Sat, 26 Aug 2023 00:21:14 GMT
ENV JULIA_SHA256=eb5a6464dcb1653143caf117a76f9e9126da8c960b737d1c82e4c46d165061f0
# Sat, 26 Aug 2023 00:23:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Sat, 26 Aug 2023 00:23:23 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95f433aa7d90194e65f6b08a599b3ee12292e124d47c204107baedfd71054c1`  
		Last Modified: Tue, 08 Aug 2023 18:31:16 GMT  
		Size: 345.3 MB (345334986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03d23fbbd4f650b6f60106a3cc28d711efce2f97cfb80b67e2dec305e011aa3`  
		Last Modified: Thu, 10 Aug 2023 00:19:47 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa48aea30e3535088afb895d06009580dfea08f902caa18a043620ce091a303`  
		Last Modified: Sat, 26 Aug 2023 00:27:05 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1fd9360584462063a819826203c37cd8a8c0e4bdc5b2d08008fff1458aada42`  
		Last Modified: Sat, 26 Aug 2023 00:27:05 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d6b36873c6ec37ab969a57e2f8867813c52acedace25531158b5451681ea0d`  
		Last Modified: Sat, 26 Aug 2023 00:27:05 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f947498c2dfb9c9b591c2a5f6553cc1062e1b2f78832a358bf68f6ae790b3f`  
		Last Modified: Sat, 26 Aug 2023 00:27:41 GMT  
		Size: 161.7 MB (161707546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebd4b8de7a9405b5c4dd50eb19d01e211f64822fb06ba99bf8f012ec8770c15`  
		Last Modified: Sat, 26 Aug 2023 00:27:05 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
