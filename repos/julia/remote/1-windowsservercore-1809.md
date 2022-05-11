## `julia:1-windowsservercore-1809`

```console
$ docker pull julia@sha256:6ac6cc886cc86c5ed0fe6c936e0b8c89ebcb3fc473ccec15801ac0df90ceaaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `julia:1-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull julia@sha256:35c6fbf65fd4022c2529cb6c678dadb3034c720aa2441931ce8b0c6a71df33a1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2648952950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:772a78092f49150c191fc631ea22a6a69682483c0ef37c81c3fe6f9e268ba6fd`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 May 2022 14:17:50 GMT
ENV JULIA_VERSION=1.7.2
# Wed, 11 May 2022 14:17:51 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.7/julia-1.7.2-win64.exe
# Wed, 11 May 2022 14:17:52 GMT
ENV JULIA_SHA256=bede21e00130c2dcb6973a968b7ed43c35d69712008a95bb08d5536d3c9e2585
# Wed, 11 May 2022 14:19:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 May 2022 14:19:50 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a143edb63a8c1d8dbed26e21eef0b2aa1233ee942561a5000ef8fee410fd3f8d`  
		Last Modified: Wed, 11 May 2022 14:30:58 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f37df932ec8945ad7f79f3e9ea852ccef959993a7be0088edbf51f846110623`  
		Last Modified: Wed, 11 May 2022 14:30:58 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3de87aca7c57928282d88e86e85b8889c8732e7076bdd0c7ceaa5b83f777cf5`  
		Last Modified: Wed, 11 May 2022 14:30:58 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17c7340442079493563d40e32593d4c8623511332c1a24957f659a24479810e3`  
		Last Modified: Wed, 11 May 2022 14:33:41 GMT  
		Size: 144.9 MB (144889981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:371bd5c007a51e16b5d69c561eed79ef2964f9a26f1634e5e84163a2bb3ebfad`  
		Last Modified: Wed, 11 May 2022 14:30:58 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
