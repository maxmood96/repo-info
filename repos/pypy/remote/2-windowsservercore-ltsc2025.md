## `pypy:2-windowsservercore-ltsc2025`

```console
$ docker pull pypy@sha256:1310f4877b71f4ad12e0608f9aa8cc37a3f3e9a8b882813bf969a984f2dc2532
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `pypy:2-windowsservercore-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull pypy@sha256:3f6e00b65a9a582cfcb8f1451b3aa42dfbf7087b19e2caa29b0a068b4855c958
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2247368440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a21603224ed31044954d61eed2e1bd60349e08153973db38bb49a1395f53e11`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 10 May 2026 10:08:54 GMT
RUN Install update 10.0.26100.32860
# Fri, 29 May 2026 20:21:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2026 20:21:48 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 29 May 2026 20:22:54 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 29 May 2026 20:23:31 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:23:32 GMT
ENV PYPY_VERSION=7.3.23
# Fri, 29 May 2026 20:24:17 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.23-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '005fda0a46e0e3f34476967c27e9f7f80d8b60a1095a2cda380e5eb47c3733ef'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.23-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:24:18 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f787ad06f38db673c3d304f21c09a82ff9a1ced32062515ea52fdb0383457b24`  
		Last Modified: Tue, 12 May 2026 18:03:01 GMT  
		Size: 682.9 MB (682882530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2f4f345af8d7ed430e91fdfe9484ee5f3f717dc8269428fabbc883881bdeec5`  
		Last Modified: Fri, 29 May 2026 20:24:27 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449b63854cb9f33baff8504ff6a5ca6fb661a0609bde6d1df9af1ea22a25f3fd`  
		Last Modified: Fri, 29 May 2026 20:24:27 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413e0e1a6b1e6be1e6f52d07c511aa210ec5044fae887395895a09d68938acb1`  
		Last Modified: Fri, 29 May 2026 20:24:26 GMT  
		Size: 427.3 KB (427346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d007cdf23d8c486de3ac9928cb8d986fe5228dde5883d2ce7ad8c823e3273b`  
		Last Modified: Fri, 29 May 2026 20:24:32 GMT  
		Size: 15.6 MB (15605152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20360c07be525ff9923316e4ef19c27630912742684195cb016f8389730c3bd`  
		Last Modified: Fri, 29 May 2026 20:24:25 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e6db583751f97b767087edbed1fe841b9714af36c0a1ec9b00feeae269b91d`  
		Last Modified: Fri, 29 May 2026 20:24:29 GMT  
		Size: 25.4 MB (25388920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc5967beabe33284ad07d7dd1d95f10d1b1b237b8f1e78cd36776fce043ef1`  
		Last Modified: Fri, 29 May 2026 20:24:25 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
