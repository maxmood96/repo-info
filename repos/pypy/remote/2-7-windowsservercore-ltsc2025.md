## `pypy:2-7-windowsservercore-ltsc2025`

```console
$ docker pull pypy@sha256:f739a10808bcc51eef16f9bcd93382ce4222e4f5febda74c0703c1ffaecb40a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4349; amd64

### `pypy:2-7-windowsservercore-ltsc2025` - windows version 10.0.26100.4349; amd64

```console
$ docker pull pypy@sha256:32f47e4b41bf6cf48807b4ca9d114c5d2a24c8d61e2c0f97f761b826ffa67526
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3517379796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24688c9a697a07abce8b88d6f8e060d246993f4c6347b30586047ca2e59d8b30`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 07 Jun 2025 15:42:01 GMT
RUN Install update 10.0.26100.4349
# Mon, 07 Jul 2025 21:03:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Jul 2025 21:03:33 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 07 Jul 2025 21:03:40 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:03:50 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:03:51 GMT
ENV PYPY_VERSION=7.3.20
# Mon, 07 Jul 2025 21:04:19 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '76d02853601ef8d3c9dd821a9faa84cabf9bc469d6b77797b21ed311b25d5419'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 07 Jul 2025 21:04:20 GMT
CMD ["pypy"]
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
	-	`sha256:b1d203b31b9074bd0d6d5de54e9fe77cee4b4c9553a347fb7a12e135f7941b7a`  
		Last Modified: Mon, 07 Jul 2025 21:07:45 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce1537c22fbcd1ce4690253a5d1eb35bbc6a1efc77d6862794cd9481e9408734`  
		Last Modified: Mon, 07 Jul 2025 21:07:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b110c1fc744a16d0e86bda94671454086ec33332d9068187530af2e01499b9cb`  
		Last Modified: Mon, 07 Jul 2025 21:07:45 GMT  
		Size: 394.1 KB (394088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952b37a76ca7bc972166da06229b280104d292057bad6f69d3198947402f420e`  
		Last Modified: Mon, 07 Jul 2025 21:07:48 GMT  
		Size: 15.6 MB (15571218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6de128b0a2e9e35ef921bf8f62a46951676b004c517cbbb10bd1ede8147a439`  
		Last Modified: Mon, 07 Jul 2025 21:07:46 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb41215e7143c8f33cef600237cfde21ee96725dc19b58016d43f941e412bb6`  
		Last Modified: Mon, 07 Jul 2025 21:07:50 GMT  
		Size: 25.2 MB (25235245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de2e8bdb2324581741b7eae18800867d28c59d11d2f50710b43990dfd0def161`  
		Last Modified: Mon, 07 Jul 2025 21:07:46 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
