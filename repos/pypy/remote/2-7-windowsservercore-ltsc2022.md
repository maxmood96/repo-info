## `pypy:2-7-windowsservercore-ltsc2022`

```console
$ docker pull pypy@sha256:f6af1f8ef948f50235e4f0901acf31c3f22a6a4298f559dbacfc9c94d719ac36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.825; amd64

### `pypy:2-7-windowsservercore-ltsc2022` - windows version 10.0.20348.825; amd64

```console
$ docker pull pypy@sha256:2333fd4a9a55b5abd383b02c815612209e60201b82b748c6e3f8aa3c1e973988
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2342562349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63de1a03142064f332603e5e88af93f8ecc30890d1bf4a19ce29474ef1ec173b`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Mon, 04 Jul 2022 17:46:55 GMT
RUN Install update 10.0.20348.825
# Tue, 12 Jul 2022 19:25:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 Jul 2022 20:35:01 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 13 Jul 2022 12:25:37 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 13 Jul 2022 12:26:10 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 Jul 2022 12:26:11 GMT
ENV PYPY_VERSION=7.3.9
# Wed, 13 Jul 2022 12:26:58 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.9-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'ca7b0f4c576995b388cfb4c796e3f6f20b037e5314571bf267daa068a3a2af31'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.9-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 13 Jul 2022 12:26:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 13 Jul 2022 12:27:00 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 13 Jul 2022 12:27:52 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 13 Jul 2022 12:27:53 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e1a27cb9d4615dec325f2cbabac4ca1f65413bdbb8b440cc961df032993a9b81`  
		Size: 863.4 MB (863367943 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:6452cb934201756f0ed9fb5e0cbea54a22a66412cb696ff30a1923d456e28bcf`  
		Last Modified: Tue, 12 Jul 2022 20:20:48 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef330eb8cab3834d9737ff92915047264f01ac2d39da71a4aa5e63eddef3204`  
		Last Modified: Tue, 12 Jul 2022 20:56:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84afc0bdd6b46b0d547e2e3558502181bbd788ed50d22582dddd2dff464f1c0`  
		Last Modified: Wed, 13 Jul 2022 12:37:36 GMT  
		Size: 653.9 KB (653899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5226a9d1e17694b67a6d832aa2f3a934ddbf5549a8bcfe9bc2ecddd7ff7fb4eb`  
		Last Modified: Wed, 13 Jul 2022 12:37:38 GMT  
		Size: 15.7 MB (15745018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d99da6f2eef6f39ce68e0f05c1c42b64d88495429a5586c2ce6ef88223673c38`  
		Last Modified: Wed, 13 Jul 2022 12:37:34 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09409b9d7af0f10421547f3d8040925a6f29a13070ab892dc26078c331323e1c`  
		Last Modified: Wed, 13 Jul 2022 12:37:39 GMT  
		Size: 23.1 MB (23076660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee4de9aef07ed869386bc077a216025e8d784f183d64a83b0b203bc941f2dd6`  
		Last Modified: Wed, 13 Jul 2022 12:37:32 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55177939cb56389729a9d00f6aa390262b49a963bf6ec1df46f9d06138618539`  
		Last Modified: Wed, 13 Jul 2022 12:37:32 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c1d04c03c3ece2f4d86722de9a850d1543a131252f3ae62575db73197f048e`  
		Last Modified: Wed, 13 Jul 2022 12:37:33 GMT  
		Size: 2.8 MB (2846805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2f77ad755f5bc63886e24746e6a6e8851f39cd63ee647117325bf9a0b30a12`  
		Last Modified: Wed, 13 Jul 2022 12:37:32 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
