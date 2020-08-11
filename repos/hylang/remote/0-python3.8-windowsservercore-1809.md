## `hylang:0-python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:99e6c44e6ef1c48f140c7414ee7c1b2268131f6187367628667aa8af00599ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `hylang:0-python3.8-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull hylang@sha256:8ff5de60c4dd2820a64fd4ff09cecc16d567ae8f397fca489d0bac3a8c4157d8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2408839954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d869b95d77c263f12583647905b8dc72a01e6a2edd0e84ce5be29e57a53361`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Aug 2020 20:43:42 GMT
ENV PYTHON_VERSION=3.8.5
# Tue, 11 Aug 2020 20:43:43 GMT
ENV PYTHON_RELEASE=3.8.5
# Tue, 11 Aug 2020 20:45:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 11 Aug 2020 20:45:18 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Tue, 11 Aug 2020 20:45:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Tue, 11 Aug 2020 20:45:21 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Tue, 11 Aug 2020 20:46:10 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Aug 2020 20:46:11 GMT
CMD ["python"]
# Tue, 11 Aug 2020 21:13:23 GMT
ENV HY_VERSION=0.19.0
# Tue, 11 Aug 2020 21:14:02 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 11 Aug 2020 21:14:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e12c5735b42b9e59003f5656cc247f8d927c46202297c44a214d6702f3f29b93`  
		Last Modified: Tue, 11 Aug 2020 20:55:48 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63be850fd17b123345c8362ca26eaaf8c2b1964f7a5a9435c69d9048cb0e923c`  
		Last Modified: Tue, 11 Aug 2020 20:55:48 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02c8a3b0ca5dbcfdbb48b0fde0e4739c979514b3b3c12032aeb2753b407ef7d2`  
		Last Modified: Tue, 11 Aug 2020 20:55:57 GMT  
		Size: 57.2 MB (57206334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705e9a7374e61a918ce2349a5ca1a2f8ed77804d70aaac8a7fb5dea608900c9`  
		Last Modified: Tue, 11 Aug 2020 20:55:46 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9f017b85929517975356c79ab8f797afd85e798cdaec98afb1ca6584a9015d`  
		Last Modified: Tue, 11 Aug 2020 20:55:45 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ee17edd0f0193e52631f3e2fd8ea30ac06685e8752aa4dc7350fc10db47c4e`  
		Last Modified: Tue, 11 Aug 2020 20:55:45 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2944ab07f764fa0cd2cdb9d52469d70e249c580e099af73b54c4cee0db766f7e`  
		Last Modified: Tue, 11 Aug 2020 20:55:48 GMT  
		Size: 10.3 MB (10251587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b18e333853daf0c1c48fea49bdc787e9b01d860df4d54966da2a0609450a0ef0`  
		Last Modified: Tue, 11 Aug 2020 20:55:45 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ed4cdad91da0c1c53416bf88a7ce7f28a742bcdb36a402602f0e3963807b78`  
		Last Modified: Tue, 11 Aug 2020 21:19:38 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db02a8b8d50a746cc3bcff1fad65f903e04e33ac8904d31018bceeac589e6288`  
		Last Modified: Tue, 11 Aug 2020 21:19:40 GMT  
		Size: 5.5 MB (5504770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668317902d14de8c1fa23be7cf7d274c6e16f64177750e39180d1d115d6d4270`  
		Last Modified: Tue, 11 Aug 2020 21:19:38 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
