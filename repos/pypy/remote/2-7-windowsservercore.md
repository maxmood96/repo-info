## `pypy:2-7-windowsservercore`

```console
$ docker pull pypy@sha256:18468d3bd6080934a96ac6f15f7731d87569f92762b6d2edc21bc1003cfe8671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `pypy:2-7-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull pypy@sha256:e9cf493fc5e336d1cc344ba80230085ba3c5e4802b2946d6aaaad99e0e25b937
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3261601283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62db2588c13978fa0e7318860fe5bf8ce4552c776412ff106399f60a7e98a944`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:55:02 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:55:08 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:55:16 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:55:17 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 14 Oct 2025 20:55:44 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '76d02853601ef8d3c9dd821a9faa84cabf9bc469d6b77797b21ed311b25d5419'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:55:46 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f932d6c77dfb1597daf851eaea0980e3b4dd60d90a5555c07c6a65507e2822`  
		Last Modified: Tue, 14 Oct 2025 20:51:14 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761b5e7fb93dabe611a5062439a04eaa5b6991ac930f93f8c65cb5703349dfcc`  
		Last Modified: Tue, 14 Oct 2025 20:56:08 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322f5ed6e73766fdc643253283b6d4550838d7ca083f612ac1d1e44b79f8a170`  
		Last Modified: Tue, 14 Oct 2025 20:56:09 GMT  
		Size: 372.6 KB (372565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50a14e1fec87a95a0dcb779ec27c4674d8455ccba6b5c4893512781036d7d1dc`  
		Last Modified: Tue, 14 Oct 2025 20:56:10 GMT  
		Size: 15.5 MB (15543047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941606033a542b5c2ecc1f1907152729a21c41cb512a39076c84d8fa2d0c5013`  
		Last Modified: Tue, 14 Oct 2025 20:56:08 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07e0efa200863770a8b227cf1a480dae1bdb7f0519bce5d99eff84c8f28893e2`  
		Last Modified: Tue, 14 Oct 2025 20:56:11 GMT  
		Size: 25.2 MB (25199947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e0c83c83b0c0579bd9ef017d510ebf4fe105641351f45200d2aaef18a7f6bd`  
		Last Modified: Tue, 14 Oct 2025 20:56:08 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull pypy@sha256:cb3b74b4b48fd81cb8faf8c0d18e4a0d1f12f75081296529616199d1c9524784
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1530094113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef25abe6a3b45762ae44f8ef6ab048fc98bc32f5f414b7a181aa87faf9b61efa`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:41:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:51:12 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:51:18 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:51:27 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:51:28 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 14 Oct 2025 20:51:59 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '76d02853601ef8d3c9dd821a9faa84cabf9bc469d6b77797b21ed311b25d5419'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:52:00 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d69910297fad50ffc461b607623e7deea128c2f2ed652341ab8682223c1249b`  
		Last Modified: Tue, 14 Oct 2025 20:45:19 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3446127170afdeb57742ca016297854803b344289f853d2569ae7f8ad174ec26`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46db117e0166d47843232ca8985b21f1f0f247538f7d8d489a97282bbd6ecd5b`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 352.9 KB (352886 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8affea3676dfc5efc888ec2e23d3e69c95a84aa083cf2c610e33c9611bb29c0`  
		Last Modified: Tue, 14 Oct 2025 20:52:17 GMT  
		Size: 15.5 MB (15529497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3a0e021229967df4f6cf45cbdc6eaa3ef92942f2f748c3329a086b05dce4aea`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd3b10b58e4dd41e93044cf8d3d5426f34bd60c8d5db36d37b6b2b144f1d31e`  
		Last Modified: Tue, 14 Oct 2025 20:52:21 GMT  
		Size: 25.2 MB (25187392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cee6e0f90e81db17a2e76eca3598cbc71863e0aa80fe1f20cc352ebd3905377e`  
		Last Modified: Tue, 14 Oct 2025 20:52:15 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
