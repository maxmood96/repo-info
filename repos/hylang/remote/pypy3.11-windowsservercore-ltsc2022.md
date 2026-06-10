## `hylang:pypy3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:78a5446f4e03985eb5892c2563bc5dfed3796221806954784536ae21f6472a46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `hylang:pypy3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull hylang@sha256:600c3a78eae8de8649f6e7c73e05eb1ae3f2faddc00981d2902bf147a595fb19
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2187069091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a224d1efac8664142a426f07293904888b6095eef25a44c0c95cf191600f5838`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:19:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:24:33 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:43 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:24:43 GMT
ENV PYPY_VERSION=7.3.23
# Tue, 09 Jun 2026 22:25:20 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.23-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '948b8ea58dea5b9917210fe4afd242c788fbfaba1c3f1a25e696a404f703389a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.23-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:20 GMT
CMD ["pypy"]
# Tue, 09 Jun 2026 23:27:06 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 23:27:07 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 23:27:55 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Jun 2026 23:27:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a031fbbd9fc892ef9346929f87c3acb83aa1453c7e42f79e7f8a2c465848d9`  
		Last Modified: Tue, 09 Jun 2026 22:20:15 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a2c242a0311379ed81c8dabc136917848170f682041e2aac96fb1c8474a81a`  
		Last Modified: Tue, 09 Jun 2026 22:25:25 GMT  
		Size: 474.6 KB (474550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9041b816d9ffa961c141e579dc781f317e03b8359c5b938e2624cd55171fe7e`  
		Last Modified: Tue, 09 Jun 2026 22:25:28 GMT  
		Size: 15.5 MB (15518749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c5436773812d2a084f9431efe448d25f67f63ecf4ba4bdb31272f081472d865`  
		Last Modified: Tue, 09 Jun 2026 22:25:25 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7dc41efe1fd58593ac6ac256eeb83e8b12785945cc46b9632fa86de17188a1b`  
		Last Modified: Tue, 09 Jun 2026 22:25:29 GMT  
		Size: 30.9 MB (30856301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e8eaa121a4d4b61d1a2f0f5cf39138beafb532f4ae22879b3a748e578b0feb1`  
		Last Modified: Tue, 09 Jun 2026 22:25:25 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6b79cdf0a98a036b2b19f8051103eec2324cbea9243d555b977a77e97f6fc4`  
		Last Modified: Tue, 09 Jun 2026 23:28:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bf12373efb663f96c3a6c0fc51c133764f4e027806d7bd61595ec579b9ed336`  
		Last Modified: Tue, 09 Jun 2026 23:28:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42e1ceeedfa33f40ba8a94136ac231ba38d1e3c9b04ec4e61735f43668c9375`  
		Last Modified: Tue, 09 Jun 2026 23:28:01 GMT  
		Size: 8.1 MB (8086144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078b15e3394d2f0c4e5cc88987a9ac2329767f9de04be7c9cee507abda64f3ef`  
		Last Modified: Tue, 09 Jun 2026 23:28:00 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
