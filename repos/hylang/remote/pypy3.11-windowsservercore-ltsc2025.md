## `hylang:pypy3.11-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:0eb8fab190a76799be9674ad0d2caa41bf82c4b75897dc5e0a35fd6d65fb50f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:a9073796cf07018de3e0af56ce858de90609bbc29647c222503aa483556b9ed4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3484717977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598f9c0bdb898982cb15e5365e95248b78512fb214c9945b14f49b52fbc24bcb`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:02:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:02:24 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:02:25 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 14 May 2025 21:03:02 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:03:03 GMT
CMD ["pypy"]
# Wed, 14 May 2025 22:13:08 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 22:13:09 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 22:14:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 22:14:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098833f947643744e5991c909aec1ebeb70388ef7ceb347dadb7f8bfa9b3973`  
		Last Modified: Fri, 16 May 2025 17:42:20 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e207549521cc696415e0b0eee10e37aa1b50123893e918e0dbb64e3740f91e`  
		Last Modified: Fri, 16 May 2025 17:42:21 GMT  
		Size: 359.2 KB (359196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f79419b50f409a1953c76c10e3b6d90c89d9d51926835771fc0e778ce50b7a`  
		Last Modified: Wed, 14 May 2025 21:03:07 GMT  
		Size: 15.5 MB (15537422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d2fd4631a03722ab9590155c1609c638b3360d097da6dfa6de3c4652b0765`  
		Last Modified: Fri, 16 May 2025 17:42:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622466bfc71a28f5d443525ac042b3f5af8cdf3ea86006dc3d9f02260f121664`  
		Last Modified: Wed, 14 May 2025 21:03:10 GMT  
		Size: 30.7 MB (30667297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e41d8d72424a5409b0823a7ed45892937c80b20f837df0f92abfdc6d73fa8d`  
		Last Modified: Fri, 16 May 2025 17:42:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0660df8f2b435b655e977631a6cb9348203b1b34872d9dc4d28a0695f2de201b`  
		Last Modified: Wed, 14 May 2025 22:14:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b1fe7b52f676ac162175e25a026e78f0eb26f4a68575bbc8fc10c51131fe4f`  
		Last Modified: Wed, 14 May 2025 22:14:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86ec72210266bca54697f4a5796a297d3d346a10ec6b7a0723d0a1b348dfa89`  
		Last Modified: Wed, 14 May 2025 22:14:12 GMT  
		Size: 7.4 MB (7380452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a853ecd159bdd05b2843ff8fa120a2d1ce0085ef2e257f34e204ad002dbfe7`  
		Last Modified: Wed, 14 May 2025 22:14:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
