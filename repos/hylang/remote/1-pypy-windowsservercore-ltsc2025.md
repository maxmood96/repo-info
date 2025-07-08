## `hylang:1-pypy-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:a5284ed833754109e993ee9dd937ae3944431e6a05a8cfdfc16df86137ab01f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `hylang:1-pypy-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull hylang@sha256:36b129304cd3ec955aa207e0e56974f43907ff098f3198e90317236c76bf35b5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3530283477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e27fa46d7dbb8097686f7a08cb2161930c01fb7241ca199e0b91272020276c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 07 Jul 2025 21:03:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 21:03:18 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:03:30 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:03:31 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 07 Jul 2025 21:04:09 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:10 GMT
CMD ["pypy"]
# Tue, 08 Jul 2025 17:04:08 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 17:04:09 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 17:05:03 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 08 Jul 2025 17:05:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8b61d8f1bb5129502a06cea04657715aa68d500a1dc0ddcf37003afcd263c28`  
		Last Modified: Tue, 10 Jun 2025 22:09:36 GMT  
		Size: 1.3 GB (1260866861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a3791bb1e4b42c77a121442fe4873f944c3176300a7438e2209e4f11e9ee840`  
		Last Modified: Mon, 07 Jul 2025 21:07:33 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c694b292a2cab3e54433c2e1f1f3b2979860248023f527c53765c66b99e89b7`  
		Last Modified: Mon, 07 Jul 2025 21:07:34 GMT  
		Size: 401.1 KB (401076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e371835d5dee70256c10a146b125b694af9d97abcf5406f7db0b52cd0765fa37`  
		Last Modified: Mon, 07 Jul 2025 21:07:36 GMT  
		Size: 15.6 MB (15576098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6c886643c39f37eb2685b023cd857fc6e2f5705d4796da3f15d375ebcd42050`  
		Last Modified: Mon, 07 Jul 2025 21:07:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d66e9d5976adf66667ca4e75a455558054c76e8c551479beb5ce8e5a6231895b`  
		Last Modified: Mon, 07 Jul 2025 21:07:37 GMT  
		Size: 30.7 MB (30699168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73ef8169fe18e96f15396d98cb8e1af3fb4a36141b109ba83cdb11897fb8d04b`  
		Last Modified: Mon, 07 Jul 2025 21:07:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec580067e3e785b526e1354ca11816ea2c56f5eea8000ef5cfb434c268fb9a6`  
		Last Modified: Tue, 08 Jul 2025 17:19:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c898d2e74b7ed63e434917c01783c130e69a96adde6db3faee3f9ed84604961b`  
		Last Modified: Tue, 08 Jul 2025 17:19:12 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e91c4902b4fa21b4c06f2731bf592baa3483c25b3bc59ad5d037f51cee4df3`  
		Last Modified: Tue, 08 Jul 2025 17:19:14 GMT  
		Size: 7.4 MB (7425292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742e03c4f2a6c19a046b44097da162f233ccdae8a6b6f6652d7a4f4ebbb713c1`  
		Last Modified: Tue, 08 Jul 2025 17:19:14 GMT  
		Size: 1.4 KB (1381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
