## `hylang:0-python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:0e01b0c1ad214b87f96430be3041f58cc709bec0a7440337a50783badb072e9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1637; amd64

### `hylang:0-python3.8-windowsservercore-1809` - windows version 10.0.17763.1637; amd64

```console
$ docker pull hylang@sha256:262ea500fc82f113e8b813b1183baa8af3ec5332a0bd3a64727867d5bbe179e7
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2466355662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a8a83c03e614802454e960f28c440d98afa68c497b90c2b0f352946b1adf68`
-	Default Command: `["hy"]`
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
# Tue, 22 Dec 2020 18:15:33 GMT
ENV PYTHON_VERSION=3.8.7
# Tue, 22 Dec 2020 18:15:34 GMT
ENV PYTHON_RELEASE=3.8.7
# Tue, 22 Dec 2020 18:17:08 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 22 Dec 2020 18:17:09 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Tue, 22 Dec 2020 18:17:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Tue, 22 Dec 2020 18:17:11 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Tue, 22 Dec 2020 18:17:56 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 22 Dec 2020 18:17:57 GMT
CMD ["python"]
# Tue, 22 Dec 2020 18:41:05 GMT
ENV HY_VERSION=0.19.0
# Tue, 22 Dec 2020 18:41:38 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 22 Dec 2020 18:41:39 GMT
CMD ["hy"]
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
	-	`sha256:89d8e165c64b8ba2882beabbb4733152b74b8bce765440da9e02661fc4866a04`  
		Last Modified: Tue, 22 Dec 2020 18:23:47 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99286cd17130cee03fedb52e07dcece80f8adc0bfb7c3370018c30fce77ae260`  
		Last Modified: Tue, 22 Dec 2020 18:23:47 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee7ac6691183cb12b2470a14eef77820cb491d8706d1d4c5ff65ae26e98c8e3`  
		Last Modified: Tue, 22 Dec 2020 18:23:56 GMT  
		Size: 58.2 MB (58180293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0936d936f65dbec950af7df1910686a819e02ccbefe2ac0605afafdad73373a8`  
		Last Modified: Tue, 22 Dec 2020 18:23:44 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc331d0b9f414bcd9c646f2ab65d08d7e7a6428b71d503a619b564f9a48ad6cd`  
		Last Modified: Tue, 22 Dec 2020 18:23:44 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cd539ff5adf97ea8f083f53b862ae028e94431d92b9d2085ab2a70cc8e73ef5`  
		Last Modified: Tue, 22 Dec 2020 18:23:44 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abc49aecb9e7fad3115bc09be14973b8c1573e485d5006a40c1ac72b130cb60b`  
		Last Modified: Tue, 22 Dec 2020 18:23:47 GMT  
		Size: 11.7 MB (11738723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7d08af4cea21903a8c4c41ae7d0025ce9156364146f2b5a8818f385e2b3d1a8`  
		Last Modified: Tue, 22 Dec 2020 18:23:44 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e5412e67b444be7b89017bfb8f785c7b01aeef5cfa2704ecf2f8f96419ad033`  
		Last Modified: Tue, 22 Dec 2020 18:44:25 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:936f1f5366e94f797bbcabcb171ba2680ce5704f3d1c4a6dca8901a4e51bff68`  
		Last Modified: Tue, 22 Dec 2020 18:44:30 GMT  
		Size: 5.6 MB (5550754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238d2ee06e4e83b2954d00ee59e5b749819c3494c422f4cd2fd95768c294de3d`  
		Last Modified: Tue, 22 Dec 2020 18:44:24 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
