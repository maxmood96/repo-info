## `hylang:1-pypy3.10-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:01804d51cce99fcac39951c97a40622cbf8b4c79679a4e038fad8f74354843db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3692; amd64

### `hylang:1-pypy3.10-windowsservercore-ltsc2022` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hylang@sha256:d44b2ebdc7e7d36f455917b194f00ec23b184aba23657de2d955919924cff890
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327086325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:291071b12482a95cf1c22c71f71b8c09a73371ae728344842d35419d43ceccd6`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:00:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:00:18 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:00:27 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:00:28 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 14 May 2025 21:01:00 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:01:01 GMT
CMD ["pypy"]
# Wed, 14 May 2025 21:18:52 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 21:18:53 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 21:19:47 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 21:19:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a0a977abaece075aa2f4241d346d5c62c0e61a80b452072fabf65760f7ef45b`  
		Last Modified: Wed, 14 May 2025 21:01:07 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2413ea6c8bf2eab55d16cf0b5b8ad588b00b0f3eb1b5759cc6860014820c8beb`  
		Last Modified: Wed, 14 May 2025 21:01:06 GMT  
		Size: 339.1 KB (339118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a975d3015ac5ff9b8f091e4937cfc2d5c3da0209812bacbd7b8802d58d8e32`  
		Last Modified: Wed, 14 May 2025 21:01:07 GMT  
		Size: 15.5 MB (15525612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bf139be26d5cab70b226174b568b74278ba7924e9bfcc1c5c2ed36d154398b`  
		Last Modified: Wed, 14 May 2025 21:01:06 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb7678649b01b944a30404297342987e0b1ffb536b19e711aeaf9786a0fb7b3`  
		Last Modified: Wed, 14 May 2025 21:01:10 GMT  
		Size: 30.3 MB (30291989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c05700f69afa93dbf636dd4f21fb7e4608316b3ca3134ec528531ed30b69ca0`  
		Last Modified: Wed, 14 May 2025 21:01:06 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14525b65eed1c9bbd3bf7ae3ddd5bc3a41abccd8a4bf7042aecdc771aa49e434`  
		Last Modified: Wed, 14 May 2025 21:19:51 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c61e567b70bfb72f5e187a13a73447115da36f2d8a5ac05e0978856ee2c903`  
		Last Modified: Wed, 14 May 2025 21:19:51 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cb120ce54073863a759258b218ec47e17c7c075fe1646a52c0ace386e81c3e6`  
		Last Modified: Wed, 14 May 2025 21:19:52 GMT  
		Size: 7.3 MB (7293772 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0455b448234822261c5f4e7cd676c473714cefdb51fd8a0344ade5bad5c8435a`  
		Last Modified: Wed, 14 May 2025 21:19:51 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
