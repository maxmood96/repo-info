## `python:rc-windowsservercore`

```console
$ docker pull python@sha256:7311325aa1110aa8af61f93161f8ff166d1cf52c00be46ded4239ff80319837a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64
	-	windows version 10.0.14393.4104; amd64

### `python:rc-windowsservercore` - windows version 10.0.17763.1637; amd64

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

### `python:rc-windowsservercore` - windows version 10.0.14393.4104; amd64

```console
$ docker pull python@sha256:eaa3294c39d664a83e407c1e36620c3ef067582b1330d2f7cf9766037f8615cf
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5843639937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62dcd7af263df1a047ec78020f3b9ad9e8eaf09a3f18734ef8993dadece95719`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 02 Dec 2020 17:42:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 09 Dec 2020 13:34:44 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Dec 2020 17:46:34 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Dec 2020 17:46:35 GMT
ENV PYTHON_VERSION=3.10.0a2
# Wed, 09 Dec 2020 17:46:35 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 09 Dec 2020 17:48:55 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 17:48:57 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Wed, 09 Dec 2020 17:48:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Wed, 09 Dec 2020 17:48:59 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Wed, 09 Dec 2020 17:50:40 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Dec 2020 17:50:41 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d2696dc2a40dc121fc5acaa02242817ac416c69d17c113e2ac5136d21a3942d8`  
		Size: 1.7 GB (1698858125 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c6d005eb9e78ad42f77f3dad7e29d954e78f0547f9884fe024a71f4042412970`  
		Last Modified: Wed, 09 Dec 2020 13:55:31 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a18db14afcdaf52f01f53af42090925b5c891dfe60bedf017c011f3a9f08413b`  
		Last Modified: Wed, 09 Dec 2020 18:13:02 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee2aa535b3eda931e6f252610ad25820debac9e603c76de842ead2d0698ac16a`  
		Last Modified: Wed, 09 Dec 2020 18:13:01 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36e181fc5e3bed3ec03beaaec565d04405ef5a27ca26296318f1c336bdb9f4d6`  
		Last Modified: Wed, 09 Dec 2020 18:13:02 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5626a4772dada164866800999c1c6e82913a9e3e27bc4fd037b5a21f3932ec`  
		Last Modified: Wed, 09 Dec 2020 18:13:11 GMT  
		Size: 59.1 MB (59138173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ca1a977b37958e7401f7ced69b980cae4a594617189ac23727c989e8cf2c38`  
		Last Modified: Wed, 09 Dec 2020 18:12:58 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbff9490457c77d1b982ab7de9792c81adc6e92a39504cc97bf3c08df4dbe39a`  
		Last Modified: Wed, 09 Dec 2020 18:12:58 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74df5ff38cb1b7c5e4d395246fe64b66e2f2e8812c822241eb17994ce2a6e31d`  
		Last Modified: Wed, 09 Dec 2020 18:12:58 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791731bba28c04954963df29fdf8b1c148c9493e7abe5b0122ac99a7e3ec6f6f`  
		Last Modified: Wed, 09 Dec 2020 18:13:17 GMT  
		Size: 15.6 MB (15648538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798b7b32b6a332004b3fc92c960a6d64356eb3625d8405a0becc2f01932c8f07`  
		Last Modified: Wed, 09 Dec 2020 18:12:58 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
