## `hylang:python3.9-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:b67fefc3b73e527ff4f9674164edb8d8e0be6c341146a15305660a5cf44214c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.707; amd64

### `hylang:python3.9-windowsservercore-ltsc2022` - windows version 10.0.20348.707; amd64

```console
$ docker pull hylang@sha256:302349073f76030777c613a79f26dc2a13706cb409493a38983fb6b644fbac2d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2297114748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3589e47ff3fc68dcda75a18f2a20be6354a872a6b2da9c85171f59ae4ee1529`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:12:09 GMT
RUN Apply image 10.0.20348.643
# Thu, 05 May 2022 03:02:27 GMT
RUN Install update 10.0.20348.707
# Tue, 10 May 2022 17:36:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 May 2022 17:36:34 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 18 May 2022 01:36:01 GMT
ENV PYTHON_VERSION=3.9.13
# Wed, 18 May 2022 01:37:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 18 May 2022 01:37:19 GMT
ENV PYTHON_PIP_VERSION=22.0.4
# Wed, 18 May 2022 01:37:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 25 May 2022 19:20:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/a312303dbd516f6a692f2fee59852701bd828dd8/public/get-pip.py
# Wed, 25 May 2022 19:20:59 GMT
ENV PYTHON_GET_PIP_SHA256=8dd03e99645c19f49bbb629ce65c46b665ee92a1d94d246418bad6afade89f8d
# Wed, 25 May 2022 19:21:43 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 25 May 2022 19:21:44 GMT
CMD ["python"]
# Wed, 25 May 2022 19:43:14 GMT
ENV HY_VERSION=1.0a4
# Wed, 25 May 2022 19:43:15 GMT
ENV HYRULE_VERSION=0.1
# Wed, 25 May 2022 19:43:49 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 25 May 2022 19:43:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:97f65a0ec59e643faf84024aa713a9be059322380315fda829756bbbd96d6258`  
		Size: 1.4 GB (1436863614 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:12fb50a031bdc8d2b65d86d694a4ed20e937852ed1bd3c433d8f2f60279cecc7`  
		Size: 800.7 MB (800671635 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e88d40042c6dc2d74dace22d66dfa64aeebe4cd3eec90e5081400debd9281a35`  
		Last Modified: Tue, 10 May 2022 18:16:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ab71824861f5d35e3544a5e827c25cabee07e6b90cc238ea411acd8b33ca431`  
		Last Modified: Tue, 10 May 2022 18:16:11 GMT  
		Size: 1.4 KB (1440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dadbbd8db76257e376c695a9e79c4f3f23a493e9fa9dc4bafaa30b7b2502b3d`  
		Last Modified: Wed, 18 May 2022 01:42:48 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc188c21d29547954b5fd5d12bd869fb4414109ecb329593d14c9b9ce1ec32b0`  
		Last Modified: Wed, 18 May 2022 01:42:55 GMT  
		Size: 52.0 MB (51953523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc1d6564d316d729a9ed7af6d4d7f67211fad20f354203489efe6d8a552f2fb`  
		Last Modified: Wed, 18 May 2022 01:42:48 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a64674d273cdf13933c7dac490f05f05283e34529c969376b217a60a76f5efc`  
		Last Modified: Wed, 18 May 2022 01:42:46 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeeafc18d0ab593f772826e5ce1bf1338dfcbdc40aa7f9b05467030aa6e8e0e3`  
		Last Modified: Wed, 25 May 2022 19:24:55 GMT  
		Size: 1.4 KB (1376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20adef14179c2de68394cf33fe15d32c91d09693aa2cb05f2da53657c8661df`  
		Last Modified: Wed, 25 May 2022 19:24:55 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82bfbda13fc112d479afcdc5db5a77d6a16166b9df4072412ac974bfc71a639`  
		Last Modified: Wed, 25 May 2022 19:24:56 GMT  
		Size: 3.7 MB (3733311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3fda394ce06bcbbe6e1e89fc5a4b77559ed6c9d2165dbdb55dc9801e98f320e`  
		Last Modified: Wed, 25 May 2022 19:24:55 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76125181703f78c091346f04d35b3de9f1366504d22a6ddc8d196c0ab13818ab`  
		Last Modified: Wed, 25 May 2022 19:46:17 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dbc708c89aac65f8eec02c0708251c0706253c89e5e0d31b188226cc13d6d76`  
		Last Modified: Wed, 25 May 2022 19:46:17 GMT  
		Size: 1.4 KB (1379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:563f57d4a1e883bb487cec0e69d73a21c0fb95be95b7a5637a4aeeedd9ce94a7`  
		Last Modified: Wed, 25 May 2022 19:46:22 GMT  
		Size: 3.9 MB (3877228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f69da6cf22537ac61dbcdd9e61371472cc9b9cd95142c1add183e3fca5142f8`  
		Last Modified: Wed, 25 May 2022 19:46:17 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
