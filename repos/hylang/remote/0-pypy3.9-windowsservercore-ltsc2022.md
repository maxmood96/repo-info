## `hylang:0-pypy3.9-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:53e429ca5d92b0761886ce14441a935e88464cc43a5e53d5af8ef49b480f904d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `hylang:0-pypy3.9-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull hylang@sha256:aea02f34f689efa165c7be59fca0861f5aef3acb981f16fc080a60412aad6d57
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1952891340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae3ec94d4f02dde4944ad7c43205e5dfe4c7e3d5b1ca43f4c4ab328d88333f03`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:06:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:07:07 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:07:22 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:07:22 GMT
ENV PYPY_VERSION=7.3.14
# Thu, 11 Jan 2024 00:07:42 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.14-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '9b3d8496f2a4729fdf20d9f835299902048950baad3a42019b67da75ca5b38b7'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.14-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 11 Jan 2024 00:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 11 Jan 2024 00:08:05 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:08:06 GMT
CMD ["pypy"]
# Thu, 11 Jan 2024 00:54:16 GMT
ENV HY_VERSION=0.28.0
# Thu, 11 Jan 2024 00:54:17 GMT
ENV HYRULE_VERSION=0.5.0
# Thu, 11 Jan 2024 00:55:14 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 11 Jan 2024 00:55:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2418a8f38e20ccf4377975ee429703f68aff80aee36e5e2a35637fea890c9b`  
		Last Modified: Thu, 11 Jan 2024 00:08:10 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05375f7ca23c9991271dc56db1cca80a3fbe5f92fd82c817929b044af8fd4c7f`  
		Last Modified: Thu, 11 Jan 2024 00:08:10 GMT  
		Size: 490.9 KB (490941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afd36de8ae04636550e4ed0435964e419e98c8903935ee794272377209d685a2`  
		Last Modified: Thu, 11 Jan 2024 00:08:10 GMT  
		Size: 15.5 MB (15541607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26b75b7d02557a957e28b912cf93eb18f6abd11445d2c704855b07007e3d9c63`  
		Last Modified: Thu, 11 Jan 2024 00:08:09 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e187e3bff0ac25f33fc8d3f21005bd4768b7d4f3f055ff4a3f08e383aca7c29e`  
		Last Modified: Thu, 11 Jan 2024 00:08:12 GMT  
		Size: 27.6 MB (27567210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bf5e7e7d91bc79f77ad813aa02e17338f4a47e8aea27089f2fc919d488cccb`  
		Last Modified: Thu, 11 Jan 2024 00:08:08 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e49617482224c75d149b5662ceba48533b6d095f17352ce3442da779dd66f69c`  
		Last Modified: Thu, 11 Jan 2024 00:08:08 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f29b3de4f9bc5ddb3c29a36aac180921677cd9934594cdd858d63a5f506e4b`  
		Last Modified: Thu, 11 Jan 2024 00:08:09 GMT  
		Size: 3.9 MB (3923145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b85b0944d9a09c7a5e21e588b5b80ac3424e89360296d0b1decc4a64c73d085f`  
		Last Modified: Thu, 11 Jan 2024 00:08:08 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc6bc6d87a0cbeda1b4de0ad94e819c9a7bb40c8074686b3de758f4fbc1e68e`  
		Last Modified: Thu, 11 Jan 2024 00:55:19 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:741fe691c100993a9e684fcbc1787684f9959f27c173cd3581ffacd40d1b8686`  
		Last Modified: Thu, 11 Jan 2024 00:55:19 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e3c336e759c81de08376f35272f3264a198f09c703c9a9da7a212c25283ae8`  
		Last Modified: Thu, 11 Jan 2024 00:55:20 GMT  
		Size: 5.1 MB (5145316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df3874abbe76a602fa7b91aa2c1004af9829783115f4089e3eac671dbabf06f`  
		Last Modified: Thu, 11 Jan 2024 00:55:19 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
