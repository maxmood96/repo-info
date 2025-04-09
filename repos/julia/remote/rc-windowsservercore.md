## `julia:rc-windowsservercore`

```console
$ docker pull julia@sha256:1ae998dcb2055a29eddf46127d50fb9720b92c105b93ea68246aae0555f3a8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `julia:rc-windowsservercore` - windows version 10.0.26100.3775; amd64

```console
$ docker pull julia@sha256:bfc0ce8df2d3b37eaa55555a234900bfa3dbb6fa5865edda2ab2e4df766b6ee2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3689235186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fa49f09d1020a41719f7fabfa51d32ca331e7c4fc2cb3c736bb2398c234982f`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 00:39:52 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 00:39:53 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Wed, 09 Apr 2025 00:39:54 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Wed, 09 Apr 2025 00:39:55 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Wed, 09 Apr 2025 00:41:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 00:41:06 GMT
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
	-	`sha256:3d4de04f0af33151121df4bb9341c8f0a1894d8511ddcb7bad4578cec91985cb`  
		Last Modified: Wed, 09 Apr 2025 00:41:13 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5982cd634f47530cdfb6b8f8ad5732478299d5d3b422a8f0355f21b2e32faf0`  
		Last Modified: Wed, 09 Apr 2025 00:41:11 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff679ae83b9fd5f7d7125c7cdc1780c6ea351e74df070faee0786d45f8f65cff`  
		Last Modified: Wed, 09 Apr 2025 00:41:11 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cae6460067d31715b35fcfb7ddf999793f5787d9d6caadd1a9d8969c3f6019ef`  
		Last Modified: Wed, 09 Apr 2025 00:41:11 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406db77ac237ba547ac20fbf9cd96fc889f55a9494bd734dcd9890e671bc6951`  
		Last Modified: Wed, 09 Apr 2025 00:41:57 GMT  
		Size: 294.5 MB (294549181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d24961aad53513a602241e91ba1e366fdd0d203beae82355b875c5b67311dc0`  
		Last Modified: Wed, 09 Apr 2025 00:41:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.20348.3453; amd64

```console
$ docker pull julia@sha256:c468ed3709032e3c90cf21f770ef5f8c762b32e42b8ed509bda941f85b2ee5d9
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2565459500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6358d7a152a5ba9167451f45cb244e7f6ffcbeffb1dbf102bfa7a5cbdf966d3b`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 04 Apr 2025 23:10:04 GMT
RUN Install update 10.0.20348.3453
# Wed, 09 Apr 2025 01:53:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 01:53:07 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Wed, 09 Apr 2025 01:53:08 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Wed, 09 Apr 2025 01:53:09 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Wed, 09 Apr 2025 01:54:33 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 01:54:35 GMT
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
	-	`sha256:a269ff92d9ee8a3145e4f0fb4f9a8547e14e1c441621f71d5e294006db51fabc`  
		Last Modified: Wed, 09 Apr 2025 01:54:38 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e29900243d33ff01b9e0bdfb74460c556a41af35212d7aeb3b599158c59f53aa`  
		Last Modified: Wed, 09 Apr 2025 01:54:37 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e9dd3d5f8c49434f38a72bf06aefa6fcc28d96e26595441ad43be25e00657a`  
		Last Modified: Wed, 09 Apr 2025 01:54:37 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ecce5465352d2bb8698c4414849492981651ae3f4f5df6a799cf40546bafd36`  
		Last Modified: Wed, 09 Apr 2025 01:54:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc0e102fb41640683cfd26547b3169b6df85f3bfa517b5cc0b372b8d4c3fc1f`  
		Last Modified: Wed, 09 Apr 2025 01:55:16 GMT  
		Size: 294.5 MB (294457379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdb2ba3c9e84bb4b0fa7a05fcdc2f2fce7efbd422543ad52584fb98d485e71b4`  
		Last Modified: Wed, 09 Apr 2025 01:54:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:rc-windowsservercore` - windows version 10.0.17763.7009; amd64

```console
$ docker pull julia@sha256:9f323c6efa03081c6029bac8326b8c92e2a25711db41b93839828ed2ccdd1441
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2446098359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2695532901249b38a561f21f203cdafb0b089963c4e08273a6c215d2dd186a34`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Fri, 04 Apr 2025 20:45:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 04 Apr 2025 20:45:35 GMT
ENV JULIA_VERSION=1.12.0-beta1
# Fri, 04 Apr 2025 20:45:35 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.12/julia-1.12.0-beta1-win64.exe
# Fri, 04 Apr 2025 20:45:36 GMT
ENV JULIA_SHA256=b9ec290ab3f5262553d30ebf852e9acf4f9c96ef415b9ef8005f1eadde807ca1
# Fri, 04 Apr 2025 20:47:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Fri, 04 Apr 2025 20:47:30 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ff501210bf55cb8ad0d39d68271e0606c132b50c2b183c08d389b2fc27198e`  
		Last Modified: Fri, 04 Apr 2025 20:47:37 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81eb52d4e932b0aa0c79da3561f6ad4315739cf28ab9746512d77ae04a76cfb`  
		Last Modified: Fri, 04 Apr 2025 20:47:35 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:068813c71025640ba95fc9dc66b041d62c614e99615529a00f2033dddde491dd`  
		Last Modified: Fri, 04 Apr 2025 20:47:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bc008a6c3a406d8af1141a1e433b01ebdaffba34f780f920d539d558384625`  
		Last Modified: Fri, 04 Apr 2025 20:47:35 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:844e960bdd3a9030c7acb5e4a016c00d5070f0e2e85f138ca0d79043e17c0004`  
		Last Modified: Fri, 04 Apr 2025 20:48:14 GMT  
		Size: 294.5 MB (294457240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd82c2c2773d998360c958ce0f52993683fcc80a3aede2ecb13123977474ac3`  
		Last Modified: Fri, 04 Apr 2025 20:47:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
