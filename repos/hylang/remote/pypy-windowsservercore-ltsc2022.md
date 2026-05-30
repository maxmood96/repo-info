## `hylang:pypy-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:ecf74f25d04dc27141b760273c074b424d20168819a1fd43439601446b1c85b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `hylang:pypy-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:8a54c6dab06b6ca319bbfbfa11b455ce0f5812b4f863bc0e05ae2534bf58ce29
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2177390533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:593c936d496d2cacd7d231568a33cf03c7bc24c7ba3427523258efe2b83d2577`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Fri, 29 May 2026 20:19:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 29 May 2026 20:20:44 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 29 May 2026 20:21:25 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:21:26 GMT
ENV PYPY_VERSION=7.3.23
# Fri, 29 May 2026 20:22:42 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.23-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '948b8ea58dea5b9917210fe4afd242c788fbfaba1c3f1a25e696a404f703389a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.23-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 29 May 2026 20:22:44 GMT
CMD ["pypy"]
# Fri, 29 May 2026 21:09:25 GMT
ENV HY_VERSION=1.3.0
# Fri, 29 May 2026 21:09:26 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 29 May 2026 21:10:13 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 29 May 2026 21:10:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f2dd162d3f3e27f7ea1228c1d7bcca964042f02e3bcb188c8912751d041a1b8`  
		Last Modified: Fri, 29 May 2026 20:22:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77f98e5a55000a966adda50bd6a691f56b0b498c14206c33d2cef26ec0a3ff1f`  
		Last Modified: Fri, 29 May 2026 20:22:49 GMT  
		Size: 510.0 KB (509983 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e816cefc1a0e414cb98c1b6b66be50ca8d8f70c9b52cd65e8d18f8c7bf4513`  
		Last Modified: Fri, 29 May 2026 20:22:54 GMT  
		Size: 15.5 MB (15514989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f6384b1b5d43cb895a2823253902f38a299fa998d441930b5afc4d4d778008`  
		Last Modified: Fri, 29 May 2026 20:22:48 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f322e2d72b10a5b8b07ab57856f10b80787fdc0ea35db7dc60c64520b079b42f`  
		Last Modified: Fri, 29 May 2026 20:22:53 GMT  
		Size: 30.9 MB (30857888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14529cc5e2e244839a4d8d6263aa58f750074d491d3f3528c6bb48ece13086e7`  
		Last Modified: Fri, 29 May 2026 20:22:48 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57b7f92ad38266ec84b0731e807ba554a21a3635730450170be018812fdc702`  
		Last Modified: Fri, 29 May 2026 21:10:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ec542b46b5387da4a0c8266d54bef94251401f46aec29bb30c5b7bc55a26ce`  
		Last Modified: Fri, 29 May 2026 21:10:18 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e0cf0614d3fd17d736a6fcbd3e8035b2233ee191442285c317f91f8496d1fd`  
		Last Modified: Fri, 29 May 2026 21:10:20 GMT  
		Size: 8.1 MB (8079284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c8311c11bf981081960a747af16d8919f828f7397ae6cad63b16e064d000fe`  
		Last Modified: Fri, 29 May 2026 21:10:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
