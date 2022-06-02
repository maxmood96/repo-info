## `hylang:python3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:cd3e10143594f6a44b5720a1b0aad54f612c53bdea6536ebfb89be488f55efe6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `hylang:python3.9-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull hylang@sha256:e45833c5c3d5087d110e34a484034406500afc510f52e7d61e64ad873a97dd6e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2563088031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c0cba6cec638bbe377f83abc92f9c05a0b78682c42251a367346977a410833`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Tue, 10 May 2022 17:40:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 May 2022 17:40:48 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 18 May 2022 01:38:13 GMT
ENV PYTHON_VERSION=3.9.13
# Wed, 18 May 2022 01:39:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 18 May 2022 01:39:50 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 18 May 2022 01:39:51 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Thu, 02 Jun 2022 19:07:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/6ce3639da143c5d79b44f94b04080abf2531fd6e/public/get-pip.py
# Thu, 02 Jun 2022 19:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=ba3ab8267d91fd41c58dbce08f76db99f747f716d85ce1865813842bb035524d
# Thu, 02 Jun 2022 19:08:29 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 02 Jun 2022 19:08:30 GMT
CMD ["python"]
# Thu, 02 Jun 2022 19:30:19 GMT
ENV HY_VERSION=1.0a4
# Thu, 02 Jun 2022 19:30:20 GMT
ENV HYRULE_VERSION=0.1
# Thu, 02 Jun 2022 19:31:21 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 02 Jun 2022 19:31:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c8a0a0d5642a312541382f8fd8cc5463eea7b9c29d4f71cd1c2592aa0e22160e`  
		Last Modified: Tue, 10 May 2022 18:17:19 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5a6a55a6348099a5a40b34d2ce942923f98a1d0c86819360798099a36eacd35`  
		Last Modified: Tue, 10 May 2022 18:17:17 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379287160e90be0a589f018b8a734ea476166ce90894cfc16d49f86df2e131d1`  
		Last Modified: Wed, 18 May 2022 01:43:07 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952ccfa828cf32dd178ce7fc774b1c340da2727f8f26005369eb83e689f1ddd7`  
		Last Modified: Wed, 18 May 2022 01:44:02 GMT  
		Size: 51.9 MB (51858043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b286bd38bbb2ae11a4ef83909a1c2eb6fc2e53daf7de8355d391ab8dc5cc6003`  
		Last Modified: Wed, 18 May 2022 01:43:07 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ce674cdf4e1bbe72afbef16b52cdd6f7d8c26060c0f276f520d29dc5c382064`  
		Last Modified: Wed, 18 May 2022 01:43:05 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e1da633e2a73723432b87510a31de9545c63e7d0b2011d183d748686e75eb7c`  
		Last Modified: Thu, 02 Jun 2022 19:10:52 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47d0421347c37d2bdb3c513c8df85d38074779c6481ce3ba7e5bd6c9bcb38c`  
		Last Modified: Thu, 02 Jun 2022 19:10:52 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b3cc172d81adead144e20e1ba5e19f819a8fba7ab4375705a63b72b5b48c3a`  
		Last Modified: Thu, 02 Jun 2022 19:10:53 GMT  
		Size: 3.5 MB (3506400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2613ee57b1c01b0959eee802518699217e7c681e741bea76f3dc643161015465`  
		Last Modified: Thu, 02 Jun 2022 19:10:52 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46c60bf8c8ec3ae3457bc4421bd536495af35d1631e3aedde730709f9a12171b`  
		Last Modified: Thu, 02 Jun 2022 19:33:00 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:661c7b37147ffa6737f95de86296f7dacc3df3c89920f543c00868b42fe305a0`  
		Last Modified: Thu, 02 Jun 2022 19:33:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3011f0d80741f26969a20aa2df1f5d1f4880e935a81e8d82ba08af6b57693f78`  
		Last Modified: Thu, 02 Jun 2022 19:33:04 GMT  
		Size: 3.7 MB (3652585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1636d598d1f8414942ab0962cf012bdda84b2605812650430381aaa637430936`  
		Last Modified: Thu, 02 Jun 2022 19:33:00 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
