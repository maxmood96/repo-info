## `hylang:pypy3.11-windowsservercore`

```console
$ docker pull hylang@sha256:63c184cf2a97ec3a993666884aeaa35599a07c45123bdf83aa95e230159c9281
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `hylang:pypy3.11-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull hylang@sha256:4e23d1c2d72638ba7711c50293563af48d69bcb4a8d91e0aeece3a89c28bf107
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2019980789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:437d0743d4f9da709c30a8acba15883f2ee80d3ab0e8839d1b4953141f0da270`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Tue, 10 Feb 2026 22:53:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:00:13 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:00:22 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:00:23 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 10 Feb 2026 23:01:00 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.20-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a8d36f6ceb1d9be6cf24a73b0ba103e7567e396b2f7a33426b05e4a06330755b'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.20-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:01:01 GMT
CMD ["pypy"]
# Tue, 10 Feb 2026 23:39:20 GMT
ENV HY_VERSION=1.2.0
# Tue, 10 Feb 2026 23:39:20 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 10 Feb 2026 23:40:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 10 Feb 2026 23:40:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ebde3c20a30d0a7e244d6ad5a9fdd16b51d9c1eeb80e49dcb2ea2da6340dff`  
		Last Modified: Tue, 10 Feb 2026 22:53:49 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97284595ba4880a726b49952669ab3df732c97d156a397c071f899e08c32d891`  
		Last Modified: Tue, 10 Feb 2026 23:01:06 GMT  
		Size: 362.3 KB (362253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f9e7770948b22be5521fc7564f316bd3e53feaee5074aa0c07505295bd8d4bb`  
		Last Modified: Tue, 10 Feb 2026 23:01:09 GMT  
		Size: 15.5 MB (15540726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36dfb0963d7461a8dbfe83f437c08b9546233d52887af694d00961feb99e4f3`  
		Last Modified: Tue, 10 Feb 2026 23:01:06 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52e5b49e81a9101a8961c4f841435039b268f282c9009a3d3ba1240c31b45c02`  
		Last Modified: Tue, 10 Feb 2026 23:01:11 GMT  
		Size: 30.7 MB (30673251 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bb2f6ed877783685dd2e5b855f9746d355d27e914dc6381ae70056f7dcb6f04`  
		Last Modified: Tue, 10 Feb 2026 23:01:07 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0df45cacc11d9c39cfc338c88bb3bb179e9833107d082a0553c7bf0c8062a501`  
		Last Modified: Tue, 10 Feb 2026 23:40:06 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03c48cff8fa41f38bd05aab4c99a2c9ff080370d4a7b4f51e95779734af44924`  
		Last Modified: Tue, 10 Feb 2026 23:40:06 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3a4ff610f600b1ff23da54d92bb39439f60c09ac47d7a994285607502b1ed54`  
		Last Modified: Tue, 10 Feb 2026 23:40:08 GMT  
		Size: 8.6 MB (8636720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f1d9e217aa148ac84777cfcde49dec7185b08c7bfb636e62e4fd058a76fc31`  
		Last Modified: Tue, 10 Feb 2026 23:40:06 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
