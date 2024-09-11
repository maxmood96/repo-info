## `hylang:0-python3.12-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:18c8ecb33caf7b4f13effae66fa8e649afa3c8a3347d66c811047685aa585d94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `hylang:0-python3.12-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull hylang@sha256:cd290e49a6cf07011a1b3a412652e7fa7c9ff862c1cad8ddbcf90b81db405b2e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1532211221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae4ae940a4986b4c85b0cb1066f0fcde5b88c013aaa56d1b44bc4ad82c3cb4df`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 11 Sep 2024 00:01:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:01:12 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Sep 2024 00:01:12 GMT
ENV PYTHON_VERSION=3.12.6
# Wed, 11 Sep 2024 00:01:42 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:01:42 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 11 Sep 2024 00:01:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 11 Sep 2024 00:01:44 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 11 Sep 2024 00:01:59 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		--no-setuptools 		--no-wheel 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:02:00 GMT
CMD ["python"]
# Wed, 11 Sep 2024 02:07:00 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 02:07:00 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 02:07:50 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 11 Sep 2024 02:07:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea5e03a77c587d6d8ea1cd408fb0f877d4cf203cb669a436165ce6edda511797`  
		Last Modified: Wed, 11 Sep 2024 00:02:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6376c3ed5832aa6c535df0b448a606b469031a43e52c368b1faf9096bc9b9cd`  
		Last Modified: Wed, 11 Sep 2024 00:02:06 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c64f585a16b5f60889df8df927e032a7368f3d11327bccf94e229df5ec102f88`  
		Last Modified: Wed, 11 Sep 2024 00:02:06 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2470fedc68dfb36d1c990aa5fd62a13a1ebf0a37f5290b1f98e337801d9c772`  
		Last Modified: Wed, 11 Sep 2024 00:02:10 GMT  
		Size: 47.7 MB (47724026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1795ad506b07b018162c772448984a58e7cd12fc106be889701fa6ca24dd2e`  
		Last Modified: Wed, 11 Sep 2024 00:02:04 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c4e4b902ee033cf5751fdfd9f71e447be606cb1b0400a4ce3fb24288e85cd2`  
		Last Modified: Wed, 11 Sep 2024 00:02:04 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7845d7a0d0d2112790d1d63767dcee3606bcdc7fe2ddff5032bf725cbbe6740`  
		Last Modified: Wed, 11 Sep 2024 00:02:04 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a036a669968a82e5b9697dcba4ebde1c4c5f032c97fb7d03ea2e272506fccf`  
		Last Modified: Wed, 11 Sep 2024 00:02:06 GMT  
		Size: 10.0 MB (10024017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60530d43f48160e6b764dba9bff4a5a51401bb8e2fce21a8cfade83e8b26118`  
		Last Modified: Wed, 11 Sep 2024 00:02:04 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d610f1f5e418720f0a521d2e95f77a6ac3c213d77d457380a59f707d184104d4`  
		Last Modified: Wed, 11 Sep 2024 02:07:53 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbcbf8d221841799f44dae812fdedb6d39f904bfe660ef56d65eae434820a6a`  
		Last Modified: Wed, 11 Sep 2024 02:07:53 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61c21d4168027d046c24050de13a9752187fff6ed7e361fae973da31b800c13d`  
		Last Modified: Wed, 11 Sep 2024 02:07:54 GMT  
		Size: 12.3 MB (12257703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e9fb9e29b379df73c691f3941fb308b512264fb1f35739140c968251aad427`  
		Last Modified: Wed, 11 Sep 2024 02:07:53 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
