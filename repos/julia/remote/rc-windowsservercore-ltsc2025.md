## `julia:rc-windowsservercore-ltsc2025`

```console
$ docker pull julia@sha256:ec62a555cc9f3c0daf40db83fc2fd65c47fa38cb254e58bf233306833fe6ebb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `julia:rc-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull julia@sha256:c3d69fc1e03be68e5367fc668af9f6b2c982ca83e4146a3b7d0ff66b1d6bfd3b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2518205394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b4c27f5972b31ad08cdf37076cc97e4302a3e81397ca92fb3d36c83a682ac48`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Tue, 12 May 2026 23:39:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:39:23 GMT
ENV JULIA_VERSION=1.13.0-rc1
# Tue, 12 May 2026 23:39:23 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.13/julia-1.13.0-rc1-win64.exe
# Tue, 12 May 2026 23:39:24 GMT
ENV JULIA_SHA256=58e3b22f9e99b94f99bd81d26ca049ef1b4fd9aa0f58e7eb0d984f56cd76d4cf
# Tue, 12 May 2026 23:40:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:40:44 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d188d7f4a5421b58c277ec337ae635de99e29dcb259e15d0521f9f034b9389`  
		Last Modified: Tue, 12 May 2026 23:40:52 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fc88a51bd743b9d1a57b174983f9eefc5af4d0e5e509c5736c2f9a59511da59`  
		Last Modified: Tue, 12 May 2026 23:40:50 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478ca1f45a381889385d652abc2f5881dd4eb4e3f3f57787ec850328cee8ea82`  
		Last Modified: Tue, 12 May 2026 23:40:50 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b712bc6f77753b47d528ece647b7eea45604b3617b2872e377bfa7c631a146ee`  
		Last Modified: Tue, 12 May 2026 23:40:50 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c76d9fe3a9932e5b542bb6dc11326b76fe41f870eafc4b7b52f115554f4bf9`  
		Last Modified: Tue, 12 May 2026 23:41:36 GMT  
		Size: 312.3 MB (312256893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af748a1f4221ee130b36edcf4a12661387444fa624b43d063d54c546b5cdd66b`  
		Last Modified: Tue, 12 May 2026 23:40:50 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
