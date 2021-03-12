## `hylang:python3.8-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:b61dda4ae21e74f404f99f8e79e87385f765cf78aae32dd18c1eadc81a6f8e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4283; amd64

### `hylang:python3.8-windowsservercore-ltsc2016` - windows version 10.0.14393.4283; amd64

```console
$ docker pull hylang@sha256:f397a8f02c0a1b82423588ef90b544c2e2086b018a872f811245a28c48f159da
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5882627683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91ebc6374483dc071be976aee327ec87a5949051e1a4234009a2c7576ab869a4`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Mar 2021 18:02:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Mar 2021 13:42:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 17:06:22 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Mar 2021 17:21:47 GMT
ENV PYTHON_VERSION=3.8.8
# Wed, 10 Mar 2021 17:21:48 GMT
ENV PYTHON_RELEASE=3.8.8
# Wed, 10 Mar 2021 17:24:07 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:24:08 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Wed, 10 Mar 2021 17:24:09 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Wed, 10 Mar 2021 17:24:11 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Wed, 10 Mar 2021 17:25:55 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:25:56 GMT
CMD ["python"]
# Wed, 10 Mar 2021 17:33:11 GMT
ENV HY_VERSION=0.20.0
# Wed, 10 Mar 2021 17:34:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 10 Mar 2021 17:34:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:30bda99601c5cbd3b2118409f401852ea648e2319bd81518723e476b28d764c5`  
		Size: 1.7 GB (1726924885 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:76680da9dc6db108ddf2e353c494b45e8486a6751619a13ed8fb3ad64b9a16e9`  
		Last Modified: Wed, 10 Mar 2021 14:06:08 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d125fe0eea998b84d015b04287600700e6c6b273702461066209a3d1b9df51d0`  
		Last Modified: Wed, 10 Mar 2021 17:27:40 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41e65bb274cbdfd322aa9df86531b6cc8aff5b2d04c44b8c8d8dff71eaabee9d`  
		Last Modified: Wed, 10 Mar 2021 17:30:47 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e72f352a4265268d73c44026a1c196a4199af85f3d4ff239fc413eba921be1b`  
		Last Modified: Wed, 10 Mar 2021 17:30:49 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3702843593d5eaaf94252e4c9a2026665edfe1f5ed2bca2269d643e1f3c6424`  
		Last Modified: Wed, 10 Mar 2021 17:30:58 GMT  
		Size: 59.1 MB (59072689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c01dc9eab55008dd1140f6dac099f75a9c1fb0b22a80edb69c2c32e92cb22965`  
		Last Modified: Wed, 10 Mar 2021 17:30:43 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb40e196ee9db38d353166bba577207d18317eaac23c64d4770d8b866bd1c8fe`  
		Last Modified: Wed, 10 Mar 2021 17:30:43 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec48e8ddc4313226d54609680f0a2e8100946449ae24a6acc585244724958d48`  
		Last Modified: Wed, 10 Mar 2021 17:30:43 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fa3f6adce83f29a8a6dd2b9c3eaa7755f6fcd9f4fe2e50f91f8b19856e4831f`  
		Last Modified: Wed, 10 Mar 2021 17:31:01 GMT  
		Size: 15.7 MB (15664482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd843e7e5463e09156eb306a861cb415ed6128ded03ce3cc67f9697cbeff17fe`  
		Last Modified: Wed, 10 Mar 2021 17:30:43 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94bf0dbe25ba7c2fabc86a15b55407756f2de4743285ba98b682ac24f787b774`  
		Last Modified: Wed, 10 Mar 2021 17:39:33 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ba5045b9ee7c266a08f47999d28fd5f3221d882939f3b56130be11fd6635df`  
		Last Modified: Wed, 10 Mar 2021 17:39:36 GMT  
		Size: 11.0 MB (10966203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba833a1faa82975a16f64c5788ed3a44a49c9aba16390c455627365705a0bae8`  
		Last Modified: Wed, 10 Mar 2021 17:39:33 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
