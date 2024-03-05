## `julia:rc-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:23c9628488697f4a6f281eeb4ba1fad9e2d4d3d56da8693da088bc7dff774e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2322; amd64

### `julia:rc-windowsservercore-ltsc2022` - windows version 10.0.20348.2322; amd64

```console
$ docker pull julia@sha256:9d761d11866209d1e3a2d0d9e6a0210d283ec342f8973bd2876c188fcb3485fe
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2207257959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06deef0d9fb6d025a04ae5a1e69755b17909f62291c54b6002b8113f3a17ff98`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 07 Feb 2024 06:55:59 GMT
RUN Install update 10.0.20348.2322
# Tue, 05 Mar 2024 00:49:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 05 Mar 2024 00:49:25 GMT
ENV JULIA_VERSION=1.11.0-alpha1
# Tue, 05 Mar 2024 00:49:26 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-alpha1-win64.exe
# Tue, 05 Mar 2024 00:49:26 GMT
ENV JULIA_SHA256=f7479a8164443bf5e96809dc11140755b0b3f3a1c5f23b7fb9a57404bb357f86
# Tue, 05 Mar 2024 00:51:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 05 Mar 2024 00:51:49 GMT
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
	-	`sha256:7a3d5c4e8e9d5c68f14619c9473e7a0980a18a154b45bfd3c92116ec199db24d`  
		Last Modified: Tue, 05 Mar 2024 00:51:53 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f977e6ffeabc521e2e0331155beff62216cbe683056ffad1549019ca044843`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17b2ac6af3f3bdd4b2c9e9856bf175bd2e01671e0bdd212aa497027dec26992d`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09733da4e960ac74550144ce5aa85f4d4323a20fde1a42251c94d176d5eeb09a`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:870d981cdb3c5dc9158ed6decdaf3bbbd826d79f03cddf626bbfd1369a683088`  
		Last Modified: Tue, 05 Mar 2024 00:52:28 GMT  
		Size: 296.6 MB (296597317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c4523a317f402256d0545ddd207df63296f3cf089668bc63008bc5c3a0c8a47`  
		Last Modified: Tue, 05 Mar 2024 00:51:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
