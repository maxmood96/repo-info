## `hylang:1-pypy3.10-windowsservercore-1809`

```console
$ docker pull hylang@sha256:e4e45713f209ea0817ebee55f5e504bdbd5eab67da016f7354a7d4afce17e28a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7249; amd64

### `hylang:1-pypy3.10-windowsservercore-1809` - windows version 10.0.17763.7249; amd64

```console
$ docker pull hylang@sha256:5995c2775268ae9a0af54c58800f43f5902277250b76a3717e9ab7a806363188
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2218921326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0de0d6b7f431eb91f5c10db5b13e174f3373c9fc3aed59be2be016289d7a9ce4`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:24:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:24:36 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:24:51 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:24:52 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:25:33 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:25:34 GMT
CMD ["pypy"]
# Fri, 18 Apr 2025 04:18:40 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:18:42 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:19:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:19:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc4fb98826135d52ce1f95ca92ce2d88a500f54c7fedd6b06a1f8e8e9ed2ad7`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b864fb56703722e675dc8423ab0ba67280fbc11156710d0a61656430848bd48`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 337.1 KB (337110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da84b6bb8e338359fcc14930caba779460ca0ca379685c52effc5d42ce9acd9a`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 15.5 MB (15500109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27800dd143e465243fdce6b4d88d416c5834994610c857d9b8af11c5e9e5cd7f`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150fbea98227e61929bb6e6eba71bf0fc2bee10aeb59878ee3726998a6d6ae8c`  
		Last Modified: Thu, 08 May 2025 23:23:18 GMT  
		Size: 30.3 MB (30281242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33555dbd995478b0b216fffe82e2cf941986c82596e52303b4292e6475e28de6`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16701c9fd3099c53de4b3c0b8f3796a81819fb7772b88d6b51f5a326af40690e`  
		Last Modified: Fri, 18 Apr 2025 04:19:51 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c21491a74c33117a8aa8c37043bf027434225e07ef47f065426e4f460e399a0e`  
		Last Modified: Fri, 18 Apr 2025 04:19:51 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ad8bcaa148d35ace6e5e2c5a900a5bcc75a32ec2fb8a4199c074255495eafb`  
		Last Modified: Fri, 18 Apr 2025 04:19:52 GMT  
		Size: 7.3 MB (7269208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5b6c937a68743cec2b5864b22d5e4c0a49054367a6c81c8a09bb54e28b9f67`  
		Last Modified: Fri, 18 Apr 2025 04:19:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
