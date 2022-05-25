## `hylang:python3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:48f86f7650b1701db08a35503e24008d80035edf4aef0ee0ac384351df82786d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `hylang:python3.9-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull hylang@sha256:42604b5f5bf71634d5959a727ba7256f58bf8ad0eacd145a94ae5f0a709b293e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2563087941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c52c67c524738fab895fbcb8f5b6c8e0736343047fbae93cae5556de93986d4`
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
# Wed, 25 May 2022 19:21:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 19:21:52 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 19:23:00 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 25 May 2022 19:23:01 GMT
CMD ["python"]
# Wed, 25 May 2022 19:43:58 GMT
ENV HY_VERSION=1.0a4
# Wed, 25 May 2022 19:43:59 GMT
ENV HYRULE_VERSION=0.1
# Wed, 25 May 2022 19:45:04 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 25 May 2022 19:45:06 GMT
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
	-	`sha256:98001ff4e67d698af2ec7b260a3a24bc189c899946c174b6e094a3afe2f8e954`  
		Last Modified: Wed, 25 May 2022 19:25:06 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93d32d5f2efd95ad9be2ceb03122ffd8e760f4264fa69725fb256b61673a37b`  
		Last Modified: Wed, 25 May 2022 19:25:06 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f243719632b10537437c959d43bdbfdd06b2d325f4cdb6f116ffafdeefae85e3`  
		Last Modified: Wed, 25 May 2022 19:25:10 GMT  
		Size: 3.5 MB (3506273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11888851ef172d9eac81c0d913df98defdc9c596920be72b4fbbad880e7a69c2`  
		Last Modified: Wed, 25 May 2022 19:25:06 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b18591f07831030fdf9fe7a6aa9ab5b78412c75637317c18105cad9631c8402`  
		Last Modified: Wed, 25 May 2022 19:46:32 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00795124508058c4fef770431daf8868167a2283a37a9450c4c4368810e7404`  
		Last Modified: Wed, 25 May 2022 19:46:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd759a19621a047f172bf0f4fb9ab4d0141c211d69c2eefd8136c4f0a8a1ab91`  
		Last Modified: Wed, 25 May 2022 19:46:33 GMT  
		Size: 3.7 MB (3652185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e356ae3dbdfe4c8d1e45126d5712483bcb3e6a4e4668f8bdf1986c1152aea12`  
		Last Modified: Wed, 25 May 2022 19:46:32 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
