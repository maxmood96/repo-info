## `julia:1-windowsservercore`

```console
$ docker pull julia@sha256:46d770a328a4f3c7cc745ccdc5290a7bc75d632f305bfd620d769375f2e68cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `julia:1-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull julia@sha256:da8380351f5c20a42e77ef4352cb4bc238c8900a6d5987342775bd9cbcd4854f
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3680267445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9b15ba2563f1a95069959638ada6ee1a6e913ef06281f6444e2fa1c2a3baad`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Tue, 15 Apr 2025 21:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 21:58:36 GMT
ENV JULIA_VERSION=1.11.5
# Tue, 15 Apr 2025 21:58:40 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Tue, 15 Apr 2025 21:58:43 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Tue, 15 Apr 2025 22:00:03 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 15 Apr 2025 22:00:06 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb8cc15862a2e6faa6b7c2aef9525ad997936d7f213ccbe43f70b1aa57b530c9`  
		Last Modified: Tue, 15 Apr 2025 22:00:11 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:655a1219e626e2d72d38099f28627b8e3d7bd360aa48aaffb44528b9208fd9cd`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c57154cd54d9aad740a4cdc99c11418f28e436c76fbe5797d314f66589ba083`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a2feaaeef37345a6b592063b4b13b54465bc0d4a1df39cb8b7957656c1b3a8`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5da0acffce31438a2cdb404e35eab8a50ccf4575b51074bd0535ff9f4394d374`  
		Last Modified: Tue, 15 Apr 2025 22:01:01 GMT  
		Size: 285.6 MB (285581419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bda492c83d33cc6270f6624469632fde9a3736245e480a6da77f31c2e9964fbd`  
		Last Modified: Tue, 15 Apr 2025 22:00:10 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull julia@sha256:4692a238c3a42cf0ad01ac03858884d3c39d65933efc0e3bf99bdf310a5d557b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2556462029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da15b5affb2d343f2e5d168430aaaeb121e4339abb5a0283440d268849fa419d`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Tue, 15 Apr 2025 22:11:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 22:11:27 GMT
ENV JULIA_VERSION=1.11.5
# Tue, 15 Apr 2025 22:11:28 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Tue, 15 Apr 2025 22:11:28 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Tue, 15 Apr 2025 22:12:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 15 Apr 2025 22:12:49 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510f1abe0ffe1466f946291b3ac20345b4a5e2063a896736990eae81bbf4bdb4`  
		Last Modified: Tue, 08 Apr 2025 21:40:38 GMT  
		Size: 808.8 MB (808803243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0668eb4ab6538a007d7d921f86dc81fc9e022fd4281369049af6b80a4ca828a5`  
		Last Modified: Tue, 15 Apr 2025 22:12:54 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945d11cd5e04d63d6222d3278f37c4dd6d6994df62da17aac8e71ac22f1db208`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:201bd3be521ed32686d3e4564f52d6bd04aa55f25883d5479fc22c38aba4d32f`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5decd5cb85982b35960661bf50aa7eeef035d39f2799fad05c045df687a67a`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39ff4897cace2368d20d6984fed7f68f1a17c1fac2bc1231d8fe911a0f7f62b`  
		Last Modified: Tue, 15 Apr 2025 22:13:29 GMT  
		Size: 285.5 MB (285459956 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c626e16efd1d216f79e2bd6ef4ee6c53c79fd08210696141dcfa6c7dd8a1ef0`  
		Last Modified: Tue, 15 Apr 2025 22:12:53 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:1-windowsservercore` - windows version 10.0.17763.7136; amd64

```console
$ docker pull julia@sha256:3cd406ae39c86f599deea0b1950ddb0785de06e78339947ddc5f32d4f59e36e1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2448173278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f73564b63db4d2693ce368c6caf86faa0efa86aca21d9807d0fd632ed5be3e`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Tue, 15 Apr 2025 21:58:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 15 Apr 2025 21:58:31 GMT
ENV JULIA_VERSION=1.11.5
# Tue, 15 Apr 2025 21:58:32 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.11/julia-1.11.5-win64.exe
# Tue, 15 Apr 2025 21:58:33 GMT
ENV JULIA_SHA256=1556bcf559b5524f858e93f0c7d2eef4f78e4b06fc42560ed3922d9d03f878bf
# Tue, 15 Apr 2025 22:00:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Tue, 15 Apr 2025 22:00:17 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a6e7d6f7409481b381eecddc0b058c381adb10b23f07ca069bf360461a0623`  
		Last Modified: Tue, 15 Apr 2025 22:00:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9974842900d4f42967d41714437ed0bfec017aef0af21072c184b410e7130faf`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a383d2d34a0b5a3b8cf8fd04f9cefceff4154f59b556504a4e4ec8544bb9a534`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a982983cc724b1c66fb2c77b8ee3724c4721302636e902e18f9f21c9277f8c1`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b27e82e0767ec5e7e0405771e027d1e57f91b56a37f25bc0f3dcbdd3e6c77`  
		Last Modified: Tue, 15 Apr 2025 22:00:59 GMT  
		Size: 285.4 MB (285440974 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b289b23c8c703f98dfb0a7c384735b1dcae5ef1a94b227bc5378384e8d11740`  
		Last Modified: Tue, 15 Apr 2025 22:00:22 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
