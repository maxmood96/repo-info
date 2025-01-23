## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:1eb9a74451306dd33a9bc7fa579743f12f360f011137705318dc2581ef72d41c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3091; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.3091; amd64

```console
$ docker pull julia@sha256:953e008cabe6e364e58f46c4599471bce3061d7754d6a953c463c4065f8f4f63
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527162325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b3d5c5c8c37022995b43e17cda09929a503c4891c29f7a95ef8f6fe04b7c21`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Wed, 22 Jan 2025 20:44:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_VERSION=1.11.3
# Wed, 22 Jan 2025 20:44:52 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.3-win64.exe
# Wed, 22 Jan 2025 20:44:53 GMT
ENV JULIA_SHA256=89a33237cb6458c286ff35214b157bfde00a8ebaf79bff2c406a47553bd2a286
# Wed, 22 Jan 2025 20:46:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 22 Jan 2025 20:46:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34a9485678f0402423965eff733b61a99f6273af7a364223bc6304f6e861d97`  
		Last Modified: Wed, 22 Jan 2025 20:46:10 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f445b400674ad239b8e8ae82ae4d77aa28c96307f3c5cdefb135dcea400064c5`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb1e884f7e71752020d103ba70a52b0ba4aad03e92aa9624ef40d83ec516149`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4836ff19d0bc7b042214ef025c2f7068915b4538a768c2a980ee95cc528150`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3922cba308371d1b39a60037b26d4afb6efe9d81c751a42e4168d52ac8f9f84`  
		Last Modified: Wed, 22 Jan 2025 20:46:43 GMT  
		Size: 264.8 MB (264770651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a1ffe1d2b351badf13a8697a07702582ed09ad4ac74ab4f083170d2c855d013`  
		Last Modified: Wed, 22 Jan 2025 20:46:09 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
