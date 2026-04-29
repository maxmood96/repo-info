## `hylang:1-pypy3.11-windowsservercore`

```console
$ docker pull hylang@sha256:291a0896d575531cbd4d42a755dfddad60b40c9c59650be901e471ede5c81c32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `hylang:1-pypy3.11-windowsservercore` - windows version 10.0.26100.32690; amd64

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

### `hylang:1-pypy3.11-windowsservercore` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:d59ccdc70233dc6e271529ed2123c8eb0b554fd1f067c733385f2a6e87edabbc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125187132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9567d7049e565c4cb09470fcd0ac195b92ef74a1189ea2e05fe85ee57b0a7b`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 23:38:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Apr 2026 23:54:55 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:55:05 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:55:05 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:55:41 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:55:42 GMT
CMD ["pypy"]
# Wed, 29 Apr 2026 00:10:44 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:10:45 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:11:31 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 29 Apr 2026 00:11:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53ca5032646149381c2c20fb699279519e0fd4478538cc8b6a7db546c3309a3c`  
		Last Modified: Tue, 28 Apr 2026 23:40:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f140fab81434cf3ce8bc50228ef9fd44fd7d47f195314d7acadd2b43894af5bc`  
		Last Modified: Tue, 28 Apr 2026 23:55:46 GMT  
		Size: 496.7 KB (496701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2d9b2bf257fcbd014618b444c3442b0c251b46c729cffd7a98a1097906e359`  
		Last Modified: Tue, 28 Apr 2026 23:55:51 GMT  
		Size: 15.5 MB (15541455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4853a6f29f1f0cd23dd4fe9fadcbeec8d729d12994ff836919093c6c0a754b`  
		Last Modified: Tue, 28 Apr 2026 23:55:46 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cab4c1315f8e91d5f3e5b1ebff648e33261bf31a23c2a663ddcb700d8658c0a`  
		Last Modified: Tue, 28 Apr 2026 23:55:50 GMT  
		Size: 30.9 MB (30911073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd96caffc5da425ba4d285fcea86be014b0082cc518a54841b1895ed86c93d0`  
		Last Modified: Tue, 28 Apr 2026 23:55:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581981b30904e6d43cc7e85b5057e1fa5642c9e296fd377a9e5bc0e384dc72c0`  
		Last Modified: Wed, 29 Apr 2026 00:11:36 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59717c2257ceb2229f060e55f612e36b1c969943f0202d5cd2d89f13f50afafb`  
		Last Modified: Wed, 29 Apr 2026 00:11:36 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f760ee82bf7e6b856bdf7ae2564a3b67dcf03a6e1a2123d15b37bd3d57d75d60`  
		Last Modified: Wed, 29 Apr 2026 00:11:37 GMT  
		Size: 8.0 MB (8018732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3beb9b168f98d7b4827dc75f199e4d8e59695c7cbd008bbb523dcd230c8803`  
		Last Modified: Wed, 29 Apr 2026 00:11:36 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
