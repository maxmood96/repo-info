## `julia:windowsservercore-ltsc2022`

```console
$ docker pull julia@sha256:12dfddf543c66c842e918b5c92bdb2da960d977556a2a4f65c9a6476a1146543
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.1006; amd64

### `julia:windowsservercore-ltsc2022` - windows version 10.0.20348.1006; amd64

```console
$ docker pull julia@sha256:2141d08277056db76002082a94e7cff274be75e61747d15a8e35c9521793216b
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2507453180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c839bf7aa95f7911daf3f72bd2e31eff067cd952d1a473a703ddf4463eada7a5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 08 Sep 2022 20:30:55 GMT
RUN Install update 10.0.20348.1006
# Wed, 14 Sep 2022 12:09:34 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Sep 2022 15:03:12 GMT
ENV JULIA_VERSION=1.8.1
# Wed, 14 Sep 2022 15:03:13 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.8/julia-1.8.1-win64.exe
# Wed, 14 Sep 2022 15:03:14 GMT
ENV JULIA_SHA256=0a14661c4df8ade4ac9b82b56770d5ee8ba23413a49ba7cefa75b4fa82ad7e43
# Wed, 14 Sep 2022 15:04:41 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 14 Sep 2022 15:04:42 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4486102fd3820ed9527fa3e7bfefa8305c2f054e65b46dffe9675755e3d8f288`  
		Size: 910.1 MB (910085953 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c5da8902b0918fe9bb0d466157622ccaf8209e4becbdd188ec41ecb563c068e6`  
		Last Modified: Wed, 14 Sep 2022 12:41:36 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c04a3fe3b96b4e72b50e317482e794ff453223f145b0806baac07b2b3b922cf1`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1ede6e0bcb469b9d31ef48490fe3705a91f309cf9edf9e53d71f02906e0660`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54ff4f050400af4211b8cb579f4a7dbde57a5fb29e4408612c9bd26627bc42bf`  
		Last Modified: Wed, 14 Sep 2022 15:12:19 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87144fd91f507eb3163b564845a24cae07729fa2908cba97418db3372a5bd8d2`  
		Last Modified: Wed, 14 Sep 2022 15:12:55 GMT  
		Size: 160.5 MB (160496471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a371df5e1d001a98c51481470b532e0c9496d0c7cb991a79892c08e6fdaf7adb`  
		Last Modified: Wed, 14 Sep 2022 15:12:18 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
