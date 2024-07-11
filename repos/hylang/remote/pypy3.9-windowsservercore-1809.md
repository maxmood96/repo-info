## `hylang:pypy3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:60441da8246a8baf104bfbda27b43270afdee859465983e11c40ef12e0a295aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6054; amd64

### `hylang:pypy3.9-windowsservercore-1809` - windows version 10.0.17763.6054; amd64

```console
$ docker pull hylang@sha256:60e2203dc6ae9f30a3849af7a89c60e4c2dcf90f756ee57ee5d4a2823fd4480b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2289524506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8381007718413d8ff25dc4192f8332fed8943d8d459a0b14cf38d05cada26a5`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Wed, 10 Jul 2024 17:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jul 2024 17:15:09 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:15:39 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:15:40 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 10 Jul 2024 17:16:16 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.16-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '06ec12a5e964dc0ad33e6f380185a4d295178dce6d6df512f508e7aee00a1323'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.16-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:16:17 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 10 Jul 2024 17:16:18 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 10 Jul 2024 17:16:55 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 10 Jul 2024 17:16:56 GMT
CMD ["pypy"]
# Thu, 11 Jul 2024 17:10:36 GMT
ENV HY_VERSION=0.29.0
# Thu, 11 Jul 2024 17:10:37 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 11 Jul 2024 17:12:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 11 Jul 2024 17:12:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7481e820679bd5248beb02eaa9c7e75140389efe8c8887f0be0eb72a77bdff5`  
		Last Modified: Wed, 10 Jul 2024 17:17:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1edcfe21c70d069613b367956054fb303be08999fb699a6360d5e4c77d8b8578`  
		Last Modified: Wed, 10 Jul 2024 17:17:00 GMT  
		Size: 509.9 KB (509889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671e64f5833b4264863f884b9ea7c5de896850621d21b6e7a2b9bdea15bde76e`  
		Last Modified: Wed, 10 Jul 2024 17:17:01 GMT  
		Size: 15.5 MB (15548103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21927fe12c119e81fa32a3364fcc8f5ec0ebcb8321e103d0fb578b18cdd8e35f`  
		Last Modified: Wed, 10 Jul 2024 17:16:59 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51e83420cc4653286842bc60864a11b39a351b348e82210fddb9b218e436a7ef`  
		Last Modified: Wed, 10 Jul 2024 17:17:06 GMT  
		Size: 26.8 MB (26785837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afe14c0f8c609f7e3c965334e343f6e0d27283999d612de2827fba78b507350f`  
		Last Modified: Wed, 10 Jul 2024 17:16:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b267d4d916b2784054ac5ac40559759ca8e7a4f310a959bd01e6c3fe2009c8ff`  
		Last Modified: Wed, 10 Jul 2024 17:16:58 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a6fd4a7a32b13844aca8c3cbaa1d68fbdc06fdd8b19b4c0ab8d87c06e11f4a3`  
		Last Modified: Wed, 10 Jul 2024 17:16:59 GMT  
		Size: 3.5 MB (3547164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b4c0bbe934cd87dfa03dff3d3fd8f12026b917bfbe48eb474668bc233784748`  
		Last Modified: Wed, 10 Jul 2024 17:16:58 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b6807af1a4b4aa88ee44394049cfd376310c6b30be0d57cd652751cd285618`  
		Last Modified: Thu, 11 Jul 2024 17:12:10 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbd720cfb48b659349a1c82a4a462cf9e8b1092c42d8ac83b1001da558431c6`  
		Last Modified: Thu, 11 Jul 2024 17:12:10 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f0e68f076e6e15d87ed539c5a191bb521f05e54d48cb9e326aa80b445462d5e`  
		Last Modified: Thu, 11 Jul 2024 17:12:11 GMT  
		Size: 4.7 MB (4693703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6709cca79624b791ba30a9e3967ff1a2fcc1e063f39c98a08ca36183894c046f`  
		Last Modified: Thu, 11 Jul 2024 17:12:10 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
