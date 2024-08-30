## `hylang:python3.11-windowsservercore-1809`

```console
$ docker pull hylang@sha256:26da44c7274b9e1bafe6d9c86c50865ba363f9c9062c80601fcd9f5e583a256c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `hylang:python3.11-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull hylang@sha256:aaba6d46aa306d8dca2ed7d66633ca60d2af61ed8b178b5873b3c7ed121b1b35
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2310501830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a6a1cf5e4443a4ea337cc7cd88e0b7f915e3744e18aa9d5fd4e769a65ddcef`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Tue, 13 Aug 2024 20:19:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:19:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Aug 2024 20:19:28 GMT
ENV PYTHON_VERSION=3.11.9
# Tue, 13 Aug 2024 20:20:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:20:49 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 13 Aug 2024 20:20:50 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Tue, 13 Aug 2024 20:20:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Tue, 13 Aug 2024 20:20:52 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Tue, 13 Aug 2024 20:21:19 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:21:20 GMT
CMD ["python"]
# Thu, 29 Aug 2024 19:58:46 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:58:48 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 20:01:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 29 Aug 2024 20:01:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbb996959ce114977d0a3609c872c203b7d5d7d980623de8fbc70d80c8b3e08f`  
		Last Modified: Tue, 13 Aug 2024 20:21:24 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3f06a3d3240cf2d3fb7c9b3cb6cd5fdb274e1d3cb3b9a1de952de4be211fc28`  
		Last Modified: Tue, 13 Aug 2024 20:21:23 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeb5fbba65dc21650549c9a8889f763a6ec4d7f55a9251305587fd9a4f179ec`  
		Last Modified: Tue, 13 Aug 2024 20:21:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65c7a88b4e594ec4b89fc02126d82ec10c1a1eb5043ff065b4511241a68434cf`  
		Last Modified: Tue, 13 Aug 2024 20:21:27 GMT  
		Size: 52.7 MB (52713479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14392b6d707c2b848a91c526798984b6eea94446a3b9771690306cbd084be7d4`  
		Last Modified: Tue, 13 Aug 2024 20:21:23 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c3858fec1f7326a4710203b300dc586daba20c66c6a4c3a35b2643495a8a6c`  
		Last Modified: Tue, 13 Aug 2024 20:21:22 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41819db27c94ab41029f8effce9fb6d4460042aab985469bd145cca855002436`  
		Last Modified: Tue, 13 Aug 2024 20:21:22 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e5e86e0132e0a87b9ee340b5fec093e08f0e7f4daa7520492b294d87fb137f`  
		Last Modified: Tue, 13 Aug 2024 20:21:22 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9832e068f3926c7b7359139f3e8cee1d431f052353e29e7962931c2a8a254d5d`  
		Last Modified: Tue, 13 Aug 2024 20:21:23 GMT  
		Size: 5.5 MB (5529165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea9877886ffb8d68aefa32c329a880025b7b0cedb3fbd227e2831098f3369cb`  
		Last Modified: Tue, 13 Aug 2024 20:21:22 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2fd0734f329a6ae88b81f3c87ed4b33e31a396c8ca6d8dbae550699af2b76eb`  
		Last Modified: Thu, 29 Aug 2024 20:01:20 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c490d3278d7be7dc38a8d8b91211a8c8c158cf6d7b971bbb9d6396a4f1021a10`  
		Last Modified: Thu, 29 Aug 2024 20:01:20 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92d4935b58aa9ec6d4980059408393935efbc09288b0bbd1da00e6618f50b641`  
		Last Modified: Thu, 29 Aug 2024 20:01:21 GMT  
		Size: 7.0 MB (7041655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ce19c9f16c91ba025651ccc74ea9437a0fb71ee667aa5e54e23c84f1e2c313`  
		Last Modified: Thu, 29 Aug 2024 20:01:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
