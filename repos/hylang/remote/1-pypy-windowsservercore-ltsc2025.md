## `hylang:1-pypy-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:c4a646ec3b0f8d4c4b44058fa989f2166ab20b02254bf5d28f74b750aee75536
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `hylang:1-pypy-windowsservercore-ltsc2025` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hylang@sha256:0e89f327b29e31ba9bb726e48c41b48bacd2b5b0e2d388e8ea4566bc07e99a4e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2184937011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0cbd822debc81ec2bc872bd7dbb4b22153332619310ce4981446ed0fd8aa3a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 28 Apr 2026 23:43:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Apr 2026 23:44:10 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:44:41 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:44:42 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:45:25 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:45:25 GMT
CMD ["pypy"]
# Wed, 29 Apr 2026 00:09:14 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:09:14 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:10:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 29 Apr 2026 00:10:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:921d9d8a0d1cbcbd263a6b927a82d6935d5da5fb021c9a4fbfec721f4604a33d`  
		Last Modified: Tue, 28 Apr 2026 23:45:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc1ff47ac99687b5605cc056ef288f23174c6f64bc8d869a652c305c647381c`  
		Last Modified: Tue, 28 Apr 2026 23:45:30 GMT  
		Size: 393.5 KB (393470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aa3b3b9d2b95df2c594d5cdd72f0c160f226760374d3216c10474274c1dee3`  
		Last Modified: Tue, 28 Apr 2026 23:45:34 GMT  
		Size: 15.6 MB (15572165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b747414ce435fc752348a3f85bf0ff1e1b67d79eee476991fa7e9daeccde6e`  
		Last Modified: Tue, 28 Apr 2026 23:45:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ac0f4f46f30056c6539c8140b7ed6f5822972c0ed8b5d99a624e17853d24e`  
		Last Modified: Tue, 28 Apr 2026 23:45:34 GMT  
		Size: 30.9 MB (30934827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d68ee3b414a8d926138b6b15b6e8d15d547490220824a32f41caaaf6768378f`  
		Last Modified: Tue, 28 Apr 2026 23:45:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aae8044d3ec4871484b77332c7041cbd42b9623c458d54190aca4ea421dde5`  
		Last Modified: Wed, 29 Apr 2026 00:10:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36e2d4160ff0509da938cd9e2c904b34a151a336e3fd0ed05479ff69976e04e`  
		Last Modified: Wed, 29 Apr 2026 00:10:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988f0e81109c9fdfca44df17433ed985b0554519a21b72dc9ec9a7f352523e6b`  
		Last Modified: Wed, 29 Apr 2026 00:10:07 GMT  
		Size: 8.0 MB (8042670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d08da71ef120fb6653dae039b340adb2cbe358803a0a8727dec22e45da3ed90`  
		Last Modified: Wed, 29 Apr 2026 00:10:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
