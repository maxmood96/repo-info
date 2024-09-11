## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:2d3f7163e77632196ec7f20b44462da98a60f459e04022953b76dac8a33e676b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:rc-windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:bb4978af6e5f8b1bf4a45b7fcf4ef9e205de07c8dbabab0b4e1713e6d6f7e7d5
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1714313821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ea8e2ddf0fc125dec2f84921630f6cfb194a32ba2fd2e3fc7550feaab9db01`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:57 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Wed, 11 Sep 2024 00:01:58 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc3-win64.exe
# Wed, 11 Sep 2024 00:01:58 GMT
ENV JULIA_SHA256=c8cf68a67216205306760cf5c0adbbaa281a859a61483409e9320b0e8c8ce605
# Wed, 11 Sep 2024 00:03:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:29 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c88b2464fbf2892050d8c95b14c3d5a9a1f0d73a55698979cc9845fe997fd0`  
		Last Modified: Wed, 11 Sep 2024 00:03:33 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2af5554b5599868a6ce3bd45408c9d9801fd05e8efe7a8e1857ee0d973e912`  
		Last Modified: Wed, 11 Sep 2024 00:03:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1fc3ebf3104acedd2de85b1e8daf7103f565c6cd05a76cd335a9434ee5869b`  
		Last Modified: Wed, 11 Sep 2024 00:03:32 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a80e8ff71337c96fc1aeaed2693a394daa36db8c4b39637db0e24464c98950e`  
		Last Modified: Wed, 11 Sep 2024 00:03:32 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c96345acd25673a2c17889767a66a4f505e14c1fd6e6a72249373aef85ac5f26`  
		Last Modified: Wed, 11 Sep 2024 00:04:03 GMT  
		Size: 252.1 MB (252114923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa3961c2b35c42c584396598c9f3318908f34f06041d48aa05620b9a679ad22f`  
		Last Modified: Wed, 11 Sep 2024 00:03:32 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:7028ba00bd174a141b94836ca77f5b0d744358c854ad7984ec46bb0976181316
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1972356434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14ea92e671f994cee997c8079532781094527dada94ec66da50d837f27000ba`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:18 GMT
ENV JULIA_VERSION=1.11.0-rc3
# Wed, 11 Sep 2024 00:01:19 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.0-rc3-win64.exe
# Wed, 11 Sep 2024 00:01:19 GMT
ENV JULIA_SHA256=c8cf68a67216205306760cf5c0adbbaa281a859a61483409e9320b0e8c8ce605
# Wed, 11 Sep 2024 00:02:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:02:41 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4809fc71b84761bbd3050e1ebef343646a3b2d4601a4e71eda2f601adc60dae3`  
		Last Modified: Wed, 11 Sep 2024 00:02:47 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504c749651207ed648f7f2d2c19f32a8d778469d7257e4dd9657c70a25e3d16f`  
		Last Modified: Wed, 11 Sep 2024 00:02:45 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d3fe72cbc66ad347616a6aceb92bc240067bc2e61fe9a80c6797dce60a1586e`  
		Last Modified: Wed, 11 Sep 2024 00:02:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62979f58f7d0f71e9056c8829b48a38dd6342fdd5511f078787a9132d9314041`  
		Last Modified: Wed, 11 Sep 2024 00:02:45 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3c9c11facb6b60ede8de73e59de90e49b3307cf31f20fd632c1b132f0d2204e`  
		Last Modified: Wed, 11 Sep 2024 00:03:17 GMT  
		Size: 252.1 MB (252081568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d62ec08860090160e445544403512bbc65e30702492fc79dbd30d1cda80166dc`  
		Last Modified: Wed, 11 Sep 2024 00:02:46 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
