## `hylang:1-pypy-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:4fa2225d4913caecbf17b540406a38846dc0d7bf6282c4d82edd53137744ac7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `hylang:1-pypy-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull hylang@sha256:68efb1531a70bd17046327df3a3e01b9f408ea43dc20461107eb0167e7c078ce
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2334112594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3218fd82ba4eb98e70cb25446d8b6d7ea068086b123ff00a2eaad1195b4c07`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Tue, 09 Jun 2026 22:12:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:25:05 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:14 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:14 GMT
ENV PYPY_VERSION=7.3.23
# Tue, 09 Jun 2026 22:25:53 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.23-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '948b8ea58dea5b9917210fe4afd242c788fbfaba1c3f1a25e696a404f703389a'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.23-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:25:53 GMT
CMD ["pypy"]
# Tue, 09 Jun 2026 23:22:51 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 23:22:51 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 23:23:34 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Jun 2026 23:23:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0472773a1127321e8af8a87afc279879bfd4be1914319a9126f4e2bf16d44d10`  
		Last Modified: Tue, 09 Jun 2026 22:13:52 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d897032e05c46268e060a9afec86d9fdde3e573fe8674e74e4c941154084f3a4`  
		Last Modified: Tue, 09 Jun 2026 22:25:58 GMT  
		Size: 373.9 KB (373851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36493fb5374b9cbae7b45554f8f4fdd2e9c533e5b66bcb57d58f4e95e5211bc8`  
		Last Modified: Tue, 09 Jun 2026 22:26:01 GMT  
		Size: 15.6 MB (15555284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e42013d9e8df53d7ce2b50b256c35339e0f8fe1bad73b4151808cabf0a87547`  
		Last Modified: Tue, 09 Jun 2026 22:25:58 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fae9831588d9520ae0589359431bb7a4fc6782b6d313c153e2e5c8f9f3b7929e`  
		Last Modified: Tue, 09 Jun 2026 22:26:02 GMT  
		Size: 30.9 MB (30906900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8ce202232b3f6abbfc94d768dfcb950c496bbbbfc76269f4de5092cd77646c`  
		Last Modified: Tue, 09 Jun 2026 22:25:58 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f962094da3d9e7fd580c02a36a757febf2ac6bff082fcab989087090dd1bed29`  
		Last Modified: Tue, 09 Jun 2026 23:23:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8abe538cdf2e0036c4e198a7720db8508c8b675487cbc360f424b423dee99a7`  
		Last Modified: Tue, 09 Jun 2026 23:23:39 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f6a38e92e072af0586e0d0c54a27de71e4e05872ff11ca352ed3adcd0aaea6d`  
		Last Modified: Tue, 09 Jun 2026 23:23:41 GMT  
		Size: 8.1 MB (8125815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04b4101c779408c53f71a6d079e22c05b4115cf46ceece20583b5429c9c98ede`  
		Last Modified: Tue, 09 Jun 2026 23:23:39 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
