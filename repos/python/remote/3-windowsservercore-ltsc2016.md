## `python:3-windowsservercore-ltsc2016`

```console
$ docker pull python@sha256:f9dc83e28668cfa2c63963ca8e4dddbe52f365a16875aa6d9a283d3cef469d85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64

### `python:3-windowsservercore-ltsc2016` - windows version 10.0.14393.3986; amd64

```console
$ docker pull python@sha256:82a1ee68dc5520a258db36ee5e53906f85fcd37f2d679d6ab486060cdcb6f1ba
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5817590746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9f5cbf4126d232cb0cd49f9f70620ca6d87a68735b6c43d4204bb674acc3791`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 12:31:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 16:40:00 GMT
ENV PYTHON_VERSION=3.9.0
# Wed, 14 Oct 2020 16:40:00 GMT
ENV PYTHON_RELEASE=3.9.0
# Wed, 14 Oct 2020 16:42:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 20 Oct 2020 17:26:25 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Tue, 20 Oct 2020 17:26:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/8283828b8fd6f1783daf55a765384e6d8d2c5014/get-pip.py
# Tue, 20 Oct 2020 17:26:26 GMT
ENV PYTHON_GET_PIP_SHA256=2250ab0a7e70f6fd22b955493f7f5cf1ea53e70b584a84a32573644a045b4bfb
# Tue, 20 Oct 2020 17:28:22 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 20 Oct 2020 17:28:23 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e300a13db0fbbf48a676ace9db3b0de292c825dfa01e6d82979d96ebc23d3675`  
		Last Modified: Wed, 14 Oct 2020 12:51:34 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b39f0e0dd839cab434f94ad881a8f23ddd6420916da71bd7c2452bda4dbcf502`  
		Last Modified: Wed, 14 Oct 2020 17:33:02 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ad1b98cb647836903432fbc50613400bf317b383d122c48be8e90f150edf12`  
		Last Modified: Wed, 14 Oct 2020 17:33:02 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a44e161de0be472c754c7a9066e27708c0718f59f0a4d11bfa1881c4ce17662a`  
		Last Modified: Wed, 14 Oct 2020 17:33:13 GMT  
		Size: 60.7 MB (60739140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84f6efa4499d5c4fa3d0096409cdfe6d4191477e5fd06b74874901adc6381f4`  
		Last Modified: Tue, 20 Oct 2020 17:37:41 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a33c1f2407efbfdff2ef4ca53d6c6db5a6997bfb25b58f5b2a5d11f2b807da20`  
		Last Modified: Tue, 20 Oct 2020 17:37:43 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b65aa754d66572a17417c63243e4883f45279edf87e6369d47c117ffd7100d5`  
		Last Modified: Tue, 20 Oct 2020 17:37:42 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cdc840ce9adf39601384af8f4e88e653f4284997ea0b20ae146ce31dba41b7c`  
		Last Modified: Tue, 20 Oct 2020 17:37:46 GMT  
		Size: 15.5 MB (15491976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a1b3ce861c3f880a827f65fc9f385fe4384bc13b7ccf41d195362a9a0382dd6`  
		Last Modified: Tue, 20 Oct 2020 17:37:42 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
