## `hylang:1-pypy3.11-windowsservercore`

```console
$ docker pull hylang@sha256:2b4cc46d2972b4a9d2690b5868588b51f85a5c63dddf1afb3bbd9e2604c6f95f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `hylang:1-pypy3.11-windowsservercore` - windows version 10.0.26100.32522; amd64

```console
$ docker pull hylang@sha256:fa23773aad257062e4081f610d094be8b3ab7f18f410cf8f321c2cda75ca752a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2135591361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faac391dd2277421bec287c8bc71fe446a74e348b0b47ed1af7c4bda502f81ea`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 16 Mar 2026 18:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 18:58:16 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:58:33 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:58:34 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 18:59:39 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.21-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a1a2b069533b838f465157025e58933199f311f5f3f58549ccaf9872ee90fa53'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.21-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:59:40 GMT
CMD ["pypy"]
# Mon, 16 Mar 2026 19:11:25 GMT
ENV HY_VERSION=1.2.0
# Mon, 16 Mar 2026 19:11:25 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 16 Mar 2026 19:12:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 16 Mar 2026 19:12:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d94ce603a9b18879fb25ac7cdb4c606fd45b84e2af8c29d3231798cf141b1cc`  
		Last Modified: Mon, 16 Mar 2026 18:59:52 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5837e92aa2de45f44f3d2b3060ffd3490ec0983c202a9bc1f807ad3da1f5e712`  
		Last Modified: Mon, 16 Mar 2026 18:59:51 GMT  
		Size: 380.2 KB (380232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8502be92ec15f0d47b7c6c05b086027d2d313888e0fb5aef31224259146b1c9b`  
		Last Modified: Mon, 16 Mar 2026 18:59:55 GMT  
		Size: 15.6 MB (15556706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2740253ebf914ffc57ea83c438d724c87bb9906ce48db31b3c93300de1bd84`  
		Last Modified: Mon, 16 Mar 2026 18:59:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdbcde8331dc0b77e20809348669030c6d8e2cbd414c5b950bf0abcd0e45d3c`  
		Last Modified: Mon, 16 Mar 2026 18:59:55 GMT  
		Size: 30.5 MB (30475091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f14009f6f960f10b79ba36ab1aacef2176617036365bb656c967c4ebfd730c`  
		Last Modified: Mon, 16 Mar 2026 18:59:51 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec5943fa167460142c1d9acee72b8efc1e9a7a736c5d51780f1d5bd1db3c8db`  
		Last Modified: Mon, 16 Mar 2026 19:12:21 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1692b766be31fabf95778c67c7aa8e6ab1e43fa3168efc25c59082ef333b69`  
		Last Modified: Mon, 16 Mar 2026 19:12:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a1a45d7fa2e8991c11edc5c2357a042183a4585a7e4346c0da7ec4f24e62aa`  
		Last Modified: Mon, 16 Mar 2026 19:12:22 GMT  
		Size: 8.0 MB (7975418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2161145a50cdb267fc61f59cc368e92a66eead0e45a27841c5ee723f34d4ee6`  
		Last Modified: Mon, 16 Mar 2026 19:12:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11-windowsservercore` - windows version 10.0.20348.4893; amd64

```console
$ docker pull hylang@sha256:0e88062085dabd73dc435585e97a4c33393c745223756b6bd97a773c39203e6f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2036755303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2977025fed60aed301c3a89be3a6b6faaa38e425e31f928375efe62a24daae0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 16 Mar 2026 19:04:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 19:04:53 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:05:09 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:05:10 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 19:05:51 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.21-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a1a2b069533b838f465157025e58933199f311f5f3f58549ccaf9872ee90fa53'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.21-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:05:52 GMT
CMD ["pypy"]
# Mon, 16 Mar 2026 20:11:34 GMT
ENV HY_VERSION=1.2.0
# Mon, 16 Mar 2026 20:11:35 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 16 Mar 2026 20:12:32 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 16 Mar 2026 20:12:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c211fcd999305c4f8a97b951257f3d692b04bec7ed4271da15f6476df81c2`  
		Last Modified: Mon, 16 Mar 2026 19:05:59 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973b8980fc320096181b3ba375e3732b07cc6cc9d28b246c086f917be93acc1a`  
		Last Modified: Mon, 16 Mar 2026 19:05:58 GMT  
		Size: 502.2 KB (502199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35178cd89d97626ea7dd8e156aa93e5d1a3cf33ba17a4fc9f25ffc6e1108e9b3`  
		Last Modified: Mon, 16 Mar 2026 19:06:01 GMT  
		Size: 15.5 MB (15542789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b716dc9c30275013b0d59f080fa7c328c1fdb1e62626bb721d8f13d30701e43b`  
		Last Modified: Mon, 16 Mar 2026 19:05:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03487f5371c4c2070c72e870c88b29a6f55912c21095458d6abe8c2fb41f29c1`  
		Last Modified: Mon, 16 Mar 2026 19:06:02 GMT  
		Size: 30.5 MB (30461339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5b2bb6148d2fa9adabc824647dbf60486d7b53ad24da9ff0a00652dcf8c2f6`  
		Last Modified: Mon, 16 Mar 2026 19:05:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec05b5f5e9359f05105a691d346bd479573e04e48d6155539619c04587ce13b`  
		Last Modified: Mon, 16 Mar 2026 20:12:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bdfb7fd0810d7d4d7061f1eeff583f9ef3556f3a7bb12d9761595cc5f3f69c`  
		Last Modified: Mon, 16 Mar 2026 20:12:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0bb56161a33711bad86201ca1d4cf5d6b6607064c42a33cfcb6d0f0af26e29`  
		Last Modified: Mon, 16 Mar 2026 20:12:38 GMT  
		Size: 8.0 MB (7959803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc0170ceafeae64cc3d3789f3f84232b5c0a2762beac609f8291ff8c6e39c0b`  
		Last Modified: Mon, 16 Mar 2026 20:12:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
