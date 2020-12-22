## `hylang:python3.8-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:a77ebc70245024ceea362df73245b09066cb50741fde74f5650d16b532f8ca0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4104; amd64

### `hylang:python3.8-windowsservercore-ltsc2016` - windows version 10.0.14393.4104; amd64

```console
$ docker pull hylang@sha256:4c1cc35c2ec3c04bd82fa96260538c9649d751701129e93c65c113fcbcbeb38e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5855653025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceb6b09e2c0202227fb46bc5d046cc11de45a8d02943a5b96d46939279496baf`
-	Default Command: `["hy"]`
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
# Tue, 22 Dec 2020 18:18:15 GMT
ENV PYTHON_VERSION=3.8.7
# Tue, 22 Dec 2020 18:18:15 GMT
ENV PYTHON_RELEASE=3.8.7
# Tue, 22 Dec 2020 18:20:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 22 Dec 2020 18:20:26 GMT
ENV PYTHON_PIP_VERSION=20.3.3
# Tue, 22 Dec 2020 18:20:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5f38681f7f5872e4032860b54e9cc11cf0374932/get-pip.py
# Tue, 22 Dec 2020 18:20:29 GMT
ENV PYTHON_GET_PIP_SHA256=6a0b13826862f33c13b614a921d36253bfa1ae779c5fbf569876f3585057e9d2
# Tue, 22 Dec 2020 18:22:12 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 22 Dec 2020 18:22:14 GMT
CMD ["python"]
# Tue, 22 Dec 2020 18:41:48 GMT
ENV HY_VERSION=0.19.0
# Tue, 22 Dec 2020 18:43:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 22 Dec 2020 18:43:20 GMT
CMD ["hy"]
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
	-	`sha256:f43366dd5c1df9b38076539fc1d8c0529b971d9c86b518e9d6e9dd80a392151a`  
		Last Modified: Tue, 22 Dec 2020 18:24:11 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:088f2ac1d4a660c2f594a275892d1b462eabd66129ec6ce8cba8fc2fdc29679a`  
		Last Modified: Tue, 22 Dec 2020 18:24:11 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36c3aad2b1d6ee57c0e4f2fd377b7c29489afa31b27bfe1ad2da693cb26b7453`  
		Last Modified: Tue, 22 Dec 2020 18:24:20 GMT  
		Size: 58.9 MB (58917432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0093adc3c0379f7a43c0010e1dc891d43e280b434a0c102f1922ddb53167db4`  
		Last Modified: Tue, 22 Dec 2020 18:24:09 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72e92aa490f738c3b6d46858a62d28ab9a50f3f457e537f86c8cb88d0c50530`  
		Last Modified: Tue, 22 Dec 2020 18:24:09 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75cc8c45fc59e74af0d1f7b89b1ed0316c049d4c32e37d990b02561b4c6b756e`  
		Last Modified: Tue, 22 Dec 2020 18:24:08 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33131bb7fd0238adaaa822115b8bac649b3956dba000ea35ca95f48b9246145`  
		Last Modified: Tue, 22 Dec 2020 18:24:30 GMT  
		Size: 17.0 MB (17045465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b084cff15aaee0a960e66880a0a8a8eeb1c283fa5d390e41f858b9834bc23845`  
		Last Modified: Tue, 22 Dec 2020 18:24:08 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c182a1e92040d5de73420dc866b06122b132c9ebe187e7b032ed3035be4f5ed`  
		Last Modified: Tue, 22 Dec 2020 18:45:07 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761cded24279678335c6c278cf8fc8456cb400b91e148642291b54dc14e87525`  
		Last Modified: Tue, 22 Dec 2020 18:45:08 GMT  
		Size: 10.8 MB (10834683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5907a7328339954bb766c70997fda52e1b68d24a3494dff85faa62c661c585`  
		Last Modified: Tue, 22 Dec 2020 18:45:06 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
