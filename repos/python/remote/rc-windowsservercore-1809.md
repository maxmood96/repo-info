## `python:rc-windowsservercore-1809`

```console
$ docker pull python@sha256:3b49247819e5a81808cda37235840a4997d7600d0da602d5a1f96c23c43b7a3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `python:rc-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull python@sha256:2b9721366edf1b2c5fa25a7c1b7f81666591ed67172e5782c011fc4e68001bef
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2459610979 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6b3c63436dbd6896371587460dc150523cedf6265b7ecf1bd35d5f7146c36a0`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 04 Dec 2020 02:13:01 GMT
RUN Install update 1809-amd64
# Wed, 09 Dec 2020 13:30:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 17:43:53 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Dec 2020 17:43:53 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 09 Dec 2020 17:43:54 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 09 Dec 2020 17:45:36 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 17:45:36 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Wed, 09 Dec 2020 17:45:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Wed, 09 Dec 2020 17:45:38 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Wed, 09 Dec 2020 17:46:21 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 17:46:22 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:aa4f58cd6da1aaf1a0b44d443bd88e7fbe5b0a6f193995a1a61d6bd63990f314`  
		Size: 672.5 MB (672541583 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a4372d14958dc8a7eaaace9e4774e7f1db524da5eb4474b5e46738848a3a61a5`  
		Last Modified: Wed, 09 Dec 2020 13:54:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e94dd2e25fa016037458dfad84ce68c5f51c1d9a517cbb1d6a9d9037fb27a47b`  
		Last Modified: Wed, 09 Dec 2020 18:12:33 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9592f5cea675151cf1f34f726a4b41f99f847caaa91adfa7cf63c33d15b2ce8f`  
		Last Modified: Wed, 09 Dec 2020 18:12:33 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b6ebb47d65b1feeb4d2e03eca475d031426836d8f0bd23bfe64f6e50b97806`  
		Last Modified: Wed, 09 Dec 2020 18:12:33 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:365dbcc33c2b6b6001c1c9d96afc0ec70f72dfb81820dd2f752a37b0d9195eee`  
		Last Modified: Wed, 09 Dec 2020 18:12:42 GMT  
		Size: 58.4 MB (58380790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b6c38c87fa7b1893ab245fd78a8723c29aa9ed3e30ea9e8c57c1dc4d2c6779`  
		Last Modified: Wed, 09 Dec 2020 18:12:30 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567cd433c1528402cddeef8fe231551ee39809fc473b2078502e3ff2fe0046d5`  
		Last Modified: Wed, 09 Dec 2020 18:12:30 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff04e1625805fed12e7ecd5aab1faaf8924634ced27d2aef193056025ed12ba`  
		Last Modified: Wed, 09 Dec 2020 18:12:30 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a79814a92202063ef853611c7f1686822c6677d0748654bf461199f64c2f77`  
		Last Modified: Wed, 09 Dec 2020 18:12:34 GMT  
		Size: 10.3 MB (10346681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bef753ebf624cb408610a142b45abcfec3e61526009f23ad5df76e86c5561d6`  
		Last Modified: Wed, 09 Dec 2020 18:12:30 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
