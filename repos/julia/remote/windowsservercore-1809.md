## `julia:windowsservercore-1809`

```console
$ docker pull julia@sha256:a938701490cb6a90e30b5ff77a780cbb61903f659abd750b42874cece1c07a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6532; amd64

### `julia:windowsservercore-1809` - windows version 10.0.17763.6532; amd64

```console
$ docker pull julia@sha256:a42d865ddfe6c244e040fe2ff05b6c593f668bfdeca0fa139074614f7ac5e62e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2295165125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0ec1c4817a3da01b7f29880690a5504be5f1d9da547a205827cb366bd3307cc`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 01 Nov 2024 11:38:40 GMT
RUN Install update 10.0.17763.6532
# Tue, 03 Dec 2024 15:33:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 03 Dec 2024 15:33:02 GMT
ENV JULIA_VERSION=1.11.2
# Tue, 03 Dec 2024 15:33:02 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.2-win64.exe
# Tue, 03 Dec 2024 15:33:03 GMT
ENV JULIA_SHA256=617c6b4d5fadea5ed05cba649377ec7c0c83519da4249c247db5a7812dc6f0c1
# Tue, 03 Dec 2024 15:36:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 03 Dec 2024 15:36:33 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbe2e64e5397827206bfd4f203139650e099ad31c5fa0d7121c12acdbbd16650`  
		Last Modified: Tue, 12 Nov 2024 19:55:08 GMT  
		Size: 290.4 MB (290385422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:006a260a53d4209657a58d816913492ac42da7d26e67df96917556cfcf78c301`  
		Last Modified: Tue, 03 Dec 2024 15:36:36 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1c5c4204957dc942560712f1409b1dc6275a12d49ff88f4f8943af9170a722`  
		Last Modified: Tue, 03 Dec 2024 15:36:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0442a606fa1a26a0b0fcf35f865cf0c2287534d87972a8ff63b1b21b098c5477`  
		Last Modified: Tue, 03 Dec 2024 15:36:35 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207223b3e429f534eeb584fcf8dd472bb2b277364b7ecbe184db5805819d4656`  
		Last Modified: Tue, 03 Dec 2024 15:36:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f989d594779fa5d7f2f958098cb9b9e24a264ac1a170b8c4f9a9cf122a2585bc`  
		Last Modified: Tue, 03 Dec 2024 15:37:09 GMT  
		Size: 284.5 MB (284504881 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9087aa6f6c428ee26ffdea40a5f2311d9b48e57f55c24e08a5fe6a8b6c783a9c`  
		Last Modified: Tue, 03 Dec 2024 15:36:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
