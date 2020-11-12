## `hylang:python3.7-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:cca611e6138196a25c23cb314ce59747514ee1231f25717fcd6f2a1b710f26e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `hylang:python3.7-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull hylang@sha256:f447175c4e9cd043c5f7084f26c404b2dda0192d1bd3cdf89d49ee7ac0ac7587
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5853643367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15732f7dac852d3c91608f74b37ab8628318c94ff14373d15095f95c9dc98265`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:09:28 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Nov 2020 17:30:07 GMT
ENV PYTHON_VERSION=3.7.9
# Wed, 11 Nov 2020 17:30:08 GMT
ENV PYTHON_RELEASE=3.7.9
# Wed, 11 Nov 2020 17:32:24 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 17:32:25 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 11 Nov 2020 17:32:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 11 Nov 2020 17:32:27 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 11 Nov 2020 17:34:03 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Nov 2020 17:34:03 GMT
CMD ["python"]
# Thu, 12 Nov 2020 01:00:51 GMT
ENV HY_VERSION=0.19.0
# Thu, 12 Nov 2020 01:02:23 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 12 Nov 2020 01:02:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32d36bd6ec3b70ad877771d7f97cafedd40418fb1bba46babfeda374e5ada5b`  
		Last Modified: Wed, 11 Nov 2020 17:37:45 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2021b0490e902aab422f8843401b5f3abdaa0e93b5da3d9da20531b02056a3`  
		Last Modified: Wed, 11 Nov 2020 17:41:14 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44172a67924cdacd1daaf1f6074b94db1697a39e56bf8fab5949562988a0666c`  
		Last Modified: Wed, 11 Nov 2020 17:41:14 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e559276d983ffa8a61b66e3f766c4e5347410f196330d29ef6578c3fbd9f43d5`  
		Last Modified: Wed, 11 Nov 2020 17:41:22 GMT  
		Size: 56.6 MB (56636759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffed846eb68a13626fc2c364d3758484bb0f2aa6a45b2c90d1563b60b45d0462`  
		Last Modified: Wed, 11 Nov 2020 17:41:10 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022e745381133e01bba81aba7d2801679a51f2e60ba7ac7c5ac18071fef200dd`  
		Last Modified: Wed, 11 Nov 2020 17:41:10 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e2ed2386f3b613780f1a03646be9ec4f2f59be73f74e79a963b2b8bfb507f80`  
		Last Modified: Wed, 11 Nov 2020 17:41:09 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11653d71fb29dd1bfd24b85cb1eedc4f0fa1a9d15b1a8c8157720d230f63b7e`  
		Last Modified: Wed, 11 Nov 2020 17:41:28 GMT  
		Size: 15.6 MB (15578589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26d2da7e0b6c12f007cd3deb7ff04a2dd776934554cfcdfa581aba0984a8bca`  
		Last Modified: Wed, 11 Nov 2020 17:41:10 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b9dc897df849f551c4b7512b6f5816bc295b8f03fd067764c54b69bd569a7d7`  
		Last Modified: Thu, 12 Nov 2020 01:04:56 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022d7f8fc70f42edd02dd84781cc3e8cdc2bc3176a8115d6aa0c054743226ba9`  
		Last Modified: Thu, 12 Nov 2020 01:05:08 GMT  
		Size: 10.9 MB (10857820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e1e805723353bafb28d849e47b1e3b2619ad332aae1e856f854f19380051ccc`  
		Last Modified: Thu, 12 Nov 2020 01:04:55 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
