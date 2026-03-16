## `pypy:2-7-windowsservercore-ltsc2022`

```console
$ docker pull pypy@sha256:dc92f31558e72778e6d4ce5902783c749aec92ef374e1b63be63acb045f9377e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `pypy:2-7-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull pypy@sha256:c857559607738148ec164f84d94855868c91277d60fe7b487bf02e6a6d5cca75
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2023584120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4284ee2a947cf28c08ef9b68f4452404495552a51517f93bdf69f33772fdf08`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 16 Mar 2026 19:06:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 19:06:41 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 16 Mar 2026 19:07:44 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:08:12 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:08:12 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 19:09:02 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.21-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '05db49d2ede174e48c8603f7d12c4b64e40c564e273c6f397c45ccf7c85af4ab'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.21-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:09:03 GMT
CMD ["pypy"]
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
	-	`sha256:0d0d604ffae188735d4a9efb7940bd8e4c0204c96e44608d7db4e29909d574f0`  
		Last Modified: Mon, 16 Mar 2026 19:09:12 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7b16068c2b8fc9b3fce6b32fd702077b87bda405f21c2d259d125f08efefa2`  
		Last Modified: Mon, 16 Mar 2026 19:09:12 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af603cd38f87d8ec9fc7a366f4abd9374ba963d124c5c1c79011a9f6c1748b9f`  
		Last Modified: Mon, 16 Mar 2026 19:09:11 GMT  
		Size: 494.9 KB (494854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1061f143832623e40aa227f11b3feb9e500d1c9f7c7a5bd541da079d26ebacb2`  
		Last Modified: Mon, 16 Mar 2026 19:09:16 GMT  
		Size: 15.5 MB (15536718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b78d89d350959fa770411448c001415aa95488953b5e5309c56e015c3c8f6d`  
		Last Modified: Mon, 16 Mar 2026 19:09:10 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1094cb88e97d7ed923ef2fa90ca1cc8ce47932ce38538f7d658c91ae8d1d3dc1`  
		Last Modified: Mon, 16 Mar 2026 19:09:14 GMT  
		Size: 25.3 MB (25265969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53d2290a5edaeef8e30476e5c33d048de1cb4b83c6ee9f1b7fbb5695dd00680`  
		Last Modified: Mon, 16 Mar 2026 19:09:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
