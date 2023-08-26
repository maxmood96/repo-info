## `julia:1-windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:d4c31a0cc697267f41d5c5689f1eb451f7516755ef3a9730fa65cc7e5bd4f130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1906; amd64

### `julia:1-windowsservercore-ltsc2022` - windows version 10.0.20348.1906; amd64

```console
$ docker pull julia@sha256:d912a2fdf872b1af3827ea4631b46c83110af20e003654081611f0e24d0386a8
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1959071456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cd4776837e2aa78820a9b0d16195b26601a2942b0fb375f31d4e8e3cca635bf`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 03 Aug 2023 10:01:10 GMT
RUN Install update 10.0.20348.1906
# Wed, 09 Aug 2023 23:35:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 26 Aug 2023 00:19:30 GMT
ENV JULIA_VERSION=1.9.3
# Sat, 26 Aug 2023 00:19:31 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.9/julia-1.9.3-win64.exe
# Sat, 26 Aug 2023 00:19:32 GMT
ENV JULIA_SHA256=eb5a6464dcb1653143caf117a76f9e9126da8c960b737d1c82e4c46d165061f0
# Sat, 26 Aug 2023 00:20:55 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Sat, 26 Aug 2023 00:20:57 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a441455ace20af58f01367d769afc2b25c3db3e4a7aee67a634d14826f6f19`  
		Last Modified: Tue, 08 Aug 2023 18:20:41 GMT  
		Size: 408.8 MB (408765102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d0f5bc5dd4cb7976f788ee32f7195b84c7964cb22bc38a49eb55673629149`  
		Last Modified: Thu, 10 Aug 2023 00:18:32 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a3432ab33f72bdcddcd8f65efb464d64d92eee48c40d87245a423926c41dd57`  
		Last Modified: Sat, 26 Aug 2023 00:26:15 GMT  
		Size: 1.4 KB (1384 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9185654cfa0b8f9ef5830e0c5dd61392e8bb01ab61ec180b18bb3aac268f0fd2`  
		Last Modified: Sat, 26 Aug 2023 00:26:15 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42dea023d6c21a245c6f33827f189dafe1ab3019eb6caba1c3a99f8bda37bc3d`  
		Last Modified: Sat, 26 Aug 2023 00:26:15 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08af1259bb4e82bbe05b7c75a4c2631fc62674ebd9d60fecc7da2af50c899032`  
		Last Modified: Sat, 26 Aug 2023 00:26:51 GMT  
		Size: 161.7 MB (161700518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc9860e356fcab64d200c5cf98c0b79667a17f10b4ad7c9db0a5361508c2e03`  
		Last Modified: Sat, 26 Aug 2023 00:26:15 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
