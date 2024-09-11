## `julia:windowsservercore`

```console
$ docker pull julia@sha256:c4fc77ea32ad538611320462a177287d2afeaf005cec47bcec0ef8f079ee3cbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2700; amd64
	-	windows version 10.0.17763.6293; amd64

### `julia:windowsservercore` - windows version 10.0.20348.2700; amd64

```console
$ docker pull julia@sha256:f5b7a5d89a776a52654df6cdc2f453acb0a23d7d3f255995341b08e613c20fea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1650770905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ffaed81f3ddd0160dee4292b8760a00b15daa2284e6d7550809db7b474c8ff5`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:06 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:07 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:12 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:13 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d98c3a27050e21570df353f32e34737975c167124ff93b0aabcbcfebd6da02f`  
		Last Modified: Wed, 11 Sep 2024 00:03:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779194b4faf7d90e8b8103b561f6ca5fc3682a86eccd8e31a15cce8b5fee36f1`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e74dec76cb2ab6e6ac2c4ca4f74778e51672e33cc296fabb2173e734ea3c1b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009491f9c893e7c5a3253f95583d0ecd8184a6454de6070a5a7cc1a89f17693`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcefd18a962d106ad9c0fc49b9dc5212671fb25eed18744837eb00e4fcab7b70`  
		Last Modified: Wed, 11 Sep 2024 00:03:40 GMT  
		Size: 188.6 MB (188572040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aaa1274fe7b347c3a0a7e742d9ae6fd44bd035eb50e3a1fe113217abc7989b`  
		Last Modified: Wed, 11 Sep 2024 00:03:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `julia:windowsservercore` - windows version 10.0.17763.6293; amd64

```console
$ docker pull julia@sha256:2cab9a25c9d3bfe25aeaa95a6834b1c3b556983fc27d9c56ea4e75489090a653
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1908828121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:214453b717c0ff79e61203d426a7f28735e6f86956dbcf4d5a519a3091f8ad79`
-	Default Command: `["julia"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:45 GMT
ENV JULIA_VERSION=1.10.5
# Wed, 11 Sep 2024 00:02:46 GMT
ENV JULIA_URL=https://julialang-s3.julialang.org/bin/winnt/x64/1.10/julia-1.10.5-win64.exe
# Wed, 11 Sep 2024 00:02:47 GMT
ENV JULIA_SHA256=82b4674bfb6d0422c2f1ccc4794c6d910252a3063f0220f68f80891f53aa581e
# Wed, 11 Sep 2024 00:03:50 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JULIA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JULIA_URL -OutFile 'julia.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:JULIA_SHA256); 	if ((Get-FileHash julia.exe -Algorithm sha256).Hash -ne $env:JULIA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process -Wait -NoNewWindow 		-FilePath '.\julia.exe' 		-ArgumentList @( 			'/SILENT', 			'/DIR=C:\julia' 		); 		Write-Host 'Removing ...'; 	Remove-Item julia.exe -Force; 		Write-Host 'Updating PATH ...'; 	$env:PATH = 'C:\julia\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ("julia --version") ...'; 	julia --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:52 GMT
CMD ["julia"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:763e87ce4def28983a85a8feae259f722a11d49bc0b84d749b7e34913356dc95`  
		Last Modified: Wed, 11 Sep 2024 00:03:58 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:953baccfb54d37992b9fb3999ffc13b8a8df9ec38a24cb180f50bda01624d623`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c02261425b7f2c15a5ebc1110304f56df360da36ddad112dd5d9bcec1c672ec`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d1b4bdfffdbadfef9b29758beba56c09132c973f2416598b7bfbf95bc8e5f16`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ab808b08890c898b38424587225b2749d4ee9161eabd606f013d23fef083d93`  
		Last Modified: Wed, 11 Sep 2024 00:04:20 GMT  
		Size: 188.6 MB (188553269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2aa7d806365baa294ec32907681acaf995fb87ae4e5e5eca5c0117dd2f6ca50b`  
		Last Modified: Wed, 11 Sep 2024 00:03:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
