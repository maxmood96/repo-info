## `hylang:0-windowsservercore-1809`

```console
$ docker pull hylang@sha256:7c64131b1ac8acde8fc60a0dcc116179bd52871e9374fc5548ed8d26bc3f5a91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1040; amd64

### `hylang:0-windowsservercore-1809` - windows version 10.0.17763.1040; amd64

```console
$ docker pull hylang@sha256:4bec80d4ea1c4f9550c3ed6629d96793c17eac236a861db6db1cb34dc1595759
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2288898337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9b989a9fcfda7634228cb3dbe5caa3526135ddb5f18e3b9f3fb3faee2edea88`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 17 Feb 2020 06:57:13 GMT
RUN Install update 1809-amd64
# Thu, 20 Feb 2020 01:13:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 26 Feb 2020 04:16:24 GMT
ENV PYTHON_VERSION=3.8.2
# Wed, 26 Feb 2020 04:16:25 GMT
ENV PYTHON_RELEASE=3.8.2
# Wed, 26 Feb 2020 04:19:10 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 26 Feb 2020 04:19:12 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 04:19:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 04:19:15 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 04:20:31 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 26 Feb 2020 04:20:33 GMT
CMD ["python"]
# Wed, 26 Feb 2020 04:41:46 GMT
ENV HY_VERSION=0.18.0
# Wed, 26 Feb 2020 04:42:28 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 26 Feb 2020 04:42:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b5405b7580792436b60c664b5fa766ea57f5a60c1d9a8c522cf53e99e4813355`  
		Size: 695.8 MB (695818606 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2061e035d6ba931d9f00238104b970d3410f4ef0d9603b4f074c7052858e01e3`  
		Last Modified: Thu, 20 Feb 2020 03:03:21 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c296ad12945ad7ace2f454f60b01be2d564b6d70c9e419288acaeb4355e41982`  
		Last Modified: Wed, 26 Feb 2020 04:23:19 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38150b36b345209936c7579673ac6a1be5bc05642775eaffe06b775aad968f0`  
		Last Modified: Wed, 26 Feb 2020 04:23:19 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:659b837de1571eabef00e486d41950f7f5f2642b58c31230bd6dfd8c1f37b8bb`  
		Last Modified: Wed, 26 Feb 2020 04:23:45 GMT  
		Size: 51.9 MB (51852450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3b8aea50dc22bbc730eea15e590365a64468d1883119fdd48bb80dcf8502413`  
		Last Modified: Wed, 26 Feb 2020 04:23:16 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e40988cd69a570f915473c9b63e528a9955fbf846b8a18994e8d31a193e4007`  
		Last Modified: Wed, 26 Feb 2020 04:23:16 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2374b1e38e02fa5a911b365b5d25e0be45ce0bfa54c85a760563d5421eeb9717`  
		Last Modified: Wed, 26 Feb 2020 04:23:15 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31061f856b8a6bef1c3813f5f209716a8cc9e648986a4d338a64741d99c74108`  
		Last Modified: Wed, 26 Feb 2020 04:23:29 GMT  
		Size: 5.4 MB (5383273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a6e16866ee792be64373e4f0c48ac0f91fe6e7547102ff5c8dc45fe0aa5dc4f`  
		Last Modified: Wed, 26 Feb 2020 04:23:16 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632ed18d5122905e12ede420a4a368bf6ecca2881549b3ba706fbcf5251235c0`  
		Last Modified: Wed, 26 Feb 2020 04:45:24 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eed0492c88b4715ad3a742753db55d773aa123ffc24b457304ee17cf25c5830`  
		Last Modified: Wed, 26 Feb 2020 04:45:26 GMT  
		Size: 1.1 MB (1147936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d485a8058cf96760086985e493eb87f76133761454529adc28ea204d75cb82e6`  
		Last Modified: Wed, 26 Feb 2020 04:45:24 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
