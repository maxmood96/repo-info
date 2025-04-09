## `hylang:1-pypy3.11-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:de339434b0fa2ccebf16acf021c269d17ef6f31d20c4e88048de181756e04632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `hylang:1-pypy3.11-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull hylang@sha256:49cfc24a89ceb782f94774e3a2ef6b15a7c2e1bda82d70f14f8cd1c31b69a0cf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3448757331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5eceed89e5c91f5df947a1ac36ccd8b488e533da5ccb9ed5c0a9981c4a03d99a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Wed, 09 Apr 2025 19:11:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Apr 2025 19:11:56 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 09 Apr 2025 19:12:08 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 19:12:09 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 19:13:00 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 09 Apr 2025 19:13:07 GMT
CMD ["pypy"]
# Wed, 09 Apr 2025 21:13:56 GMT
ENV HY_VERSION=1.0.0
# Wed, 09 Apr 2025 21:13:56 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 09 Apr 2025 21:14:52 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 09 Apr 2025 21:14:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d50d41bfffb28dc77efe4ad8d66d46e5991a810ab2a6836abf44c14bbbc0c0a`  
		Last Modified: Wed, 09 Apr 2025 19:13:18 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f536f1d27db4d935a07a4fdf6ec0f0400e9a314b4118af709b810e5f888264df`  
		Last Modified: Wed, 09 Apr 2025 19:13:17 GMT  
		Size: 386.4 KB (386421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a922098026cf90e88f5e7232b8ecaccca423317755a231113c10b80b97abdb6`  
		Last Modified: Wed, 09 Apr 2025 19:13:18 GMT  
		Size: 15.6 MB (15569383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38c8972829d3eb262d5ca9dce1cca8e3c116b4f64b46d50e9c62e36bcca5169`  
		Last Modified: Wed, 09 Apr 2025 19:13:17 GMT  
		Size: 1.4 KB (1353 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c23a725aec72373bf578f932e22686e812893cbdbe9329d7b20b24059b15df1a`  
		Last Modified: Wed, 09 Apr 2025 19:13:21 GMT  
		Size: 30.7 MB (30706263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c4a8e40b1c537a31c82c7f586e6fe9cd30d0b414e30b1fd85642cce65a753e`  
		Last Modified: Wed, 09 Apr 2025 19:13:17 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ca76ba21e318c12bd574df7a7ed8d6e48e56a5edded3319f1cc68e76d1f9a8`  
		Last Modified: Wed, 09 Apr 2025 21:14:55 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86692b897180ab1e49e2075b1ead8b4e19a1ec351878c5a394273e080189aad`  
		Last Modified: Wed, 09 Apr 2025 21:14:55 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bed08ed76f04565fae15926e0f7bb942ce844a808430b40317db680674335fa`  
		Last Modified: Wed, 09 Apr 2025 21:14:56 GMT  
		Size: 7.4 MB (7407852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52447009be39753ce244033aafa6a697f51323eea71b42f260458bfe01cbd3fd`  
		Last Modified: Wed, 09 Apr 2025 21:14:55 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
