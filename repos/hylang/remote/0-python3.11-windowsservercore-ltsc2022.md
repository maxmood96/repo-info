## `hylang:0-python3.11-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:6034082f6fb7bc5913340a04d15b6e4ff219a032f954d17e69068ddeb8cef99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `hylang:0-python3.11-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull hylang@sha256:a5f7836469d8f375d8de605d982d7d70c7f0b14d53f7342d17aa1f09aaf37735
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2206860580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86be4ef3e63477c92be9bf88feb516e245acb6e451e71592b70b3a49dc72f4ac`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Tue, 13 Aug 2024 20:15:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 13 Aug 2024 20:15:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 13 Aug 2024 20:15:50 GMT
ENV PYTHON_VERSION=3.11.9
# Tue, 13 Aug 2024 20:16:30 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:16:30 GMT
ENV PYTHON_PIP_VERSION=24.0
# Tue, 13 Aug 2024 20:16:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Tue, 13 Aug 2024 20:16:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/66d8a0f637083e2c3ddffc0cb1e65ce126afb856/public/get-pip.py
# Tue, 13 Aug 2024 20:16:32 GMT
ENV PYTHON_GET_PIP_SHA256=6fb7b781206356f45ad79efbb19322caa6c2a5ad39092d0d44d0fec94117e118
# Tue, 13 Aug 2024 20:16:47 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 13 Aug 2024 20:16:47 GMT
CMD ["python"]
# Thu, 29 Aug 2024 19:58:34 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:58:35 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 20:00:18 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 29 Aug 2024 20:00:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c07c22fbe28a178236f9f50c815dae28d9895001b7334abb792da07838815f`  
		Last Modified: Tue, 13 Aug 2024 20:16:52 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35fb3127fd7edd5fee7128b7e60134614d78e3003d056854a67783b4e2e7103`  
		Last Modified: Tue, 13 Aug 2024 20:16:51 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76870beb6a8c5d5b5e61efeade5d81707e0e13a4527a8a0df470013833f09af0`  
		Last Modified: Tue, 13 Aug 2024 20:16:51 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c682f099aefa325f01e5847aac8d15128a58a40fa7ccad07aa49bde0d5917b2f`  
		Last Modified: Tue, 13 Aug 2024 20:16:54 GMT  
		Size: 52.5 MB (52537994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35837e593c0038085b6d3606d2b9d90ccfcf5bffdae1bff33b58203c680d7f79`  
		Last Modified: Tue, 13 Aug 2024 20:16:50 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06ff1439acafaf4e6c0275010fcf94ea23da56f4201b81d905c1463984cbd289`  
		Last Modified: Tue, 13 Aug 2024 20:16:50 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45b11833877ca794e8e0939cd66b444b225a3d83f80db1f49d46a160fdf793cc`  
		Last Modified: Tue, 13 Aug 2024 20:16:50 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1052c369d9516103d5816feee43d1bbbade9417f643603424300d93941a0fb89`  
		Last Modified: Tue, 13 Aug 2024 20:16:50 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dadb1609bd38a6b6c0b49badc71179ab9003a2ab9e15710df1c198afeff18f`  
		Last Modified: Tue, 13 Aug 2024 20:16:50 GMT  
		Size: 5.5 MB (5518059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d78d9062b71049818491e7ef55f7e9a05ffb5c240d8f99981889821685c1885`  
		Last Modified: Tue, 13 Aug 2024 20:16:50 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7915cdfda106dc3bc5e2636b211848af68178355792a17c4c8019d8fb2b6701`  
		Last Modified: Thu, 29 Aug 2024 20:00:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42bc47d1862d7d5e9ac9e8b7038d9a8fe260bcc2e3a961773d0c720c1fe412eb`  
		Last Modified: Thu, 29 Aug 2024 20:00:23 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5614c569b4f5f11ade08f23a1a6968370c34ba0edd375bb593293e1c1dcaa25`  
		Last Modified: Thu, 29 Aug 2024 20:00:24 GMT  
		Size: 7.0 MB (7025374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ce3aa64577752bf5c2aa06a8a4af1f2364a2b8ac848ac79acd73cce89debc8`  
		Last Modified: Thu, 29 Aug 2024 20:00:23 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
