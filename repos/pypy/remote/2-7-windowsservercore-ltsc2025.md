## `pypy:2-7-windowsservercore-ltsc2025`

```console
$ docker pull pypy@sha256:886a5b3a5b009ffdd7f6c8207bcd3aeb88ff117384ff1722058278b4c4922686
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `pypy:2-7-windowsservercore-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull pypy@sha256:620b23eb536afd383ad2d35886ec4171b9c5bb308cbaccd6a437c30a69d9d762
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3436238635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e9f81b511f91ca09c90e18a2e1bd0858adb1841d89eda6cbc1b3067e6b28b7a`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:24:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:24:55 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 18 Apr 2025 03:25:07 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:25:21 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:25:22 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:25:54 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy2.7-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'fbdcd4fe681981c020a25c1a35225209dc3d651f6117ebe9e4d212b66a2b46ec'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy2.7-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:25:56 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a2ae315ae9f66e2931489df8311f424b834fe90584da71b5da6baf96f54ee46`  
		Last Modified: Fri, 18 Apr 2025 03:26:00 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502a1f41c61a76e7dcfb90dcc566d943cc755b1ff9084fbe12bbf78979f5b784`  
		Last Modified: Fri, 18 Apr 2025 03:26:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832795bc9c7f516d18f0b370f59654d97def898ac5a028ed578bbf36dab9989`  
		Last Modified: Fri, 18 Apr 2025 03:25:59 GMT  
		Size: 355.8 KB (355756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d53295f458074ede6876dbbb482269d4d5b0dbc341e3c719fa658cb5e6d016`  
		Last Modified: Fri, 18 Apr 2025 03:26:00 GMT  
		Size: 15.5 MB (15539079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919c543ab5cbae628f2df8d5c280f534c4d3b0f11057f5979a2fb1d34f3d31ce`  
		Last Modified: Fri, 18 Apr 2025 03:25:59 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894478713777d4f5c62da4861e4678bf9ce6a2d45cd322ffb0a1685585ad45b7`  
		Last Modified: Fri, 18 Apr 2025 03:26:03 GMT  
		Size: 25.2 MB (25177246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a731fd0a5e8ab74ea7a99edd9bd582751276dab2343681b3014f8773a83b9037`  
		Last Modified: Fri, 18 Apr 2025 03:25:59 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
