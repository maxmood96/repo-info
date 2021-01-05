## `python:rc-windowsservercore-1809`

```console
$ docker pull python@sha256:74abbae2ce11aa6fa64f34ed898b5360acece7ba9973e83f19f1e45e9ac9ab64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `python:rc-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull python@sha256:c910fce944f1f16548cd2f8abe6a64ea3bab55c65e95a8376a19f398ae75a756
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2461262426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9918b118bbf05a96e66f74658b74549110f3a50a3a8290483915b9ea4c05b753`
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
# Tue, 05 Jan 2021 01:15:12 GMT
ENV PYTHON_VERSION=3.10.0a4
# Tue, 05 Jan 2021 01:15:13 GMT
ENV PYTHON_RELEASE=3.10.0
# Tue, 05 Jan 2021 01:16:54 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 05 Jan 2021 01:16:55 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Tue, 05 Jan 2021 01:16:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Tue, 05 Jan 2021 01:16:56 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Tue, 05 Jan 2021 01:17:45 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 05 Jan 2021 01:17:46 GMT
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
	-	`sha256:1cd59626499d946c5f6dc41fbf10417c42c0abf03e563a1095d7116773deb136`  
		Last Modified: Tue, 05 Jan 2021 01:23:38 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ed7e58febd8f4eea1a27d94a984e94975e2bd10d2f0f984c5389412bed9d51`  
		Last Modified: Tue, 05 Jan 2021 01:23:38 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253c16613675ca3dd1429c784b6f07150a93299bf99782bf2c1b50c9202ea42c`  
		Last Modified: Tue, 05 Jan 2021 01:23:46 GMT  
		Size: 58.5 MB (58540781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f04c3d260d95bb6b1fb4482ac59149cd6b4644a5ce18eebeabb322ffa7b33a`  
		Last Modified: Tue, 05 Jan 2021 01:23:34 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de442772f798eea9b0ca120769461e725ef59906c403654ad0615436550bf0e8`  
		Last Modified: Tue, 05 Jan 2021 01:23:34 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c89678f8ccca0ae781218bc1ae4f24ecb9e8244bf0376f7e78ef014aa12efb4`  
		Last Modified: Tue, 05 Jan 2021 01:23:35 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a799d60c70c1ad2033f921fedf3bb4109c284016acd949d1ef659ba324de6817`  
		Last Modified: Tue, 05 Jan 2021 01:23:38 GMT  
		Size: 11.8 MB (11838082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e16be4906b59f7c44fe7f5aabcc93a9b7429fbc32e3a05893dc1869c9387af19`  
		Last Modified: Tue, 05 Jan 2021 01:23:34 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
