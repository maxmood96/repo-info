## `python:3-windowsservercore-1809`

```console
$ docker pull python@sha256:da00bc601c2db4a0b92d8ac80f49fe28dffdd5d08903588c23671f54b66aac8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1518; amd64

### `python:3-windowsservercore-1809` - windows version 10.0.17763.1518; amd64

```console
$ docker pull python@sha256:d2e902d141ca88d8467bbf2f0b113a998697935aed0315d5b9f17f276a05e8f2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2444529277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28be85e32628c80d634d28c55566b33f037a2765b93475d2f657ee4581abea2`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:27:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Oct 2020 16:44:27 GMT
ENV PYTHON_VERSION=3.9.0
# Wed, 14 Oct 2020 16:44:28 GMT
ENV PYTHON_RELEASE=3.9.0
# Wed, 14 Oct 2020 17:16:20 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 20 Oct 2020 17:28:36 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Tue, 20 Oct 2020 17:28:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/8283828b8fd6f1783daf55a765384e6d8d2c5014/get-pip.py
# Tue, 20 Oct 2020 17:28:37 GMT
ENV PYTHON_GET_PIP_SHA256=2250ab0a7e70f6fd22b955493f7f5cf1ea53e70b584a84a32573644a045b4bfb
# Tue, 20 Oct 2020 17:29:29 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 20 Oct 2020 17:29:30 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5e61fff845eda39f31bdf5d797254fdf656ee79d8c294c1713007864bc4c2535`  
		Last Modified: Wed, 14 Oct 2020 12:50:32 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01bf26201555634128dbff07ca16472d6ffecc9bce994529192f241fc171bdd8`  
		Last Modified: Wed, 14 Oct 2020 17:33:40 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca5a116668f6f6d9d670c8c6e9ba46f4e6130cf63349bec627d951dce6cb24e`  
		Last Modified: Wed, 14 Oct 2020 17:33:40 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70a815831367b274b441ed78c18af422ab36dd8ec67da2600b43adbb4f55116f`  
		Last Modified: Wed, 14 Oct 2020 17:33:50 GMT  
		Size: 60.1 MB (60102852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c19e7d177dfa26b85566aaba3e521fd18310675e9a459c617f56704b090b2c9`  
		Last Modified: Tue, 20 Oct 2020 17:38:08 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79db2f1678e800c9ffdd951ba5bd3a9636abb16ebab9e15d4f7ef4d3ae4d0065`  
		Last Modified: Tue, 20 Oct 2020 17:38:08 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ba4c2c3868d288b90c660e3899a0a1e789f1966c5d8f7a7f3d3d7d8a46dba8`  
		Last Modified: Tue, 20 Oct 2020 17:38:09 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3570f3dfc2e9d0f0a21aa725e7b5e5a346b577b889b6912534db96ccba7c01e4`  
		Last Modified: Tue, 20 Oct 2020 17:38:21 GMT  
		Size: 10.3 MB (10328337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fe70736ec94676217607da4756a4b29023d6791dc095183520038337e3527f2`  
		Last Modified: Tue, 20 Oct 2020 17:38:08 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
