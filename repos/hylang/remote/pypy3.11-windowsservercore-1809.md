## `hylang:pypy3.11-windowsservercore-1809`

```console
$ docker pull hylang@sha256:8207a28993883848a9b0218cd6701a87de21506475cc4875acbb81b9fa94607b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7136; amd64

### `hylang:pypy3.11-windowsservercore-1809` - windows version 10.0.17763.7136; amd64

```console
$ docker pull hylang@sha256:d13f0a543c4d0a0d7e2ccb5fc3984eaeed0dc22524ed6d1def31f4d6d914806c
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2216530787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dabed0f945b81955b2a7718459805f09b4b9c56d9a76bc597e618077018a0c6`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Sat, 05 Apr 2025 01:48:05 GMT
RUN Install update 10.0.17763.7136
# Thu, 10 Apr 2025 21:50:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 10 Apr 2025 21:51:06 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Thu, 10 Apr 2025 21:51:22 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Thu, 10 Apr 2025 21:51:23 GMT
ENV PYPY_VERSION=7.3.19
# Thu, 10 Apr 2025 21:52:01 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 10 Apr 2025 21:52:01 GMT
CMD ["pypy"]
# Thu, 10 Apr 2025 22:14:37 GMT
ENV HY_VERSION=1.0.0
# Thu, 10 Apr 2025 22:14:39 GMT
ENV HYRULE_VERSION=1.0.0
# Thu, 10 Apr 2025 22:16:12 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 10 Apr 2025 22:16:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8d949f82a48e7c53af792160596b10005419fbc7ecfed6bc45bbeee3a5a2f07`  
		Last Modified: Tue, 08 Apr 2025 19:58:26 GMT  
		Size: 442.5 MB (442457492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345ac6258ee2eea907a51bf27b1d6e5837991046fe09e82a0a6750d58775be2b`  
		Last Modified: Thu, 10 Apr 2025 21:52:07 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7c0c79e1812e78a303befd65f0b2cb1877857efb3c33c39a6d2856c7a13338`  
		Last Modified: Thu, 10 Apr 2025 21:52:06 GMT  
		Size: 330.7 KB (330709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c01dac1bdcf67c878cafbb1a17c3ea2fec1a9b8f19f2728120a6c1ab437c56f`  
		Last Modified: Thu, 10 Apr 2025 21:52:07 GMT  
		Size: 15.5 MB (15497742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97f26c661a5b6ef6a3090b0bf984c505e9472f6640fa17c909fd806391e5746`  
		Last Modified: Thu, 10 Apr 2025 21:52:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162e60439357a87fa9f7a65ba8dd436abdac6942a43dbf05ee14b7f715197f17`  
		Last Modified: Thu, 10 Apr 2025 21:52:10 GMT  
		Size: 30.6 MB (30613444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bd7db8bbc05219bbd04b1fd5e16649276c6a3a7a045f350ba4285fdc3b19f0`  
		Last Modified: Thu, 10 Apr 2025 21:52:05 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cfacd051e610e47d85a5b86b63d95fba2e2692861ba08c59663fbb164a2ce1b`  
		Last Modified: Thu, 10 Apr 2025 22:16:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dd6d9eea7e9c5c82d4ce77e27f8b79ab6ede19c477b32c971dde22baa28ffb5`  
		Last Modified: Thu, 10 Apr 2025 22:16:15 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:196d1815e34649fc648c042f9249efd567a1ea66da3502ab057e451e2c86d6b7`  
		Last Modified: Thu, 10 Apr 2025 22:16:16 GMT  
		Size: 7.4 MB (7355308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7de4907dbf7e0b148e51894fd0e63c8dce44009e7f255a8250ec14922c4bced`  
		Last Modified: Thu, 10 Apr 2025 22:16:15 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
