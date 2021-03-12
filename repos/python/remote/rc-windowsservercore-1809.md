## `python:rc-windowsservercore-1809`

```console
$ docker pull python@sha256:577736e8e1cc69fb6a284916fc3d4f5c032a80c92defba27e9c104e9c5ba83cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `python:rc-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull python@sha256:e5fa1420b3546fbc1e88adbbd79825d0d336b59457b661cdb5cf1c88f62d4b3b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527834261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5651b88b9841de0e5fd7178491b26c60e4eefc3f9bbee182c4efe5c831841c6`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 13:15:52 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Mar 2021 17:03:24 GMT
ENV PYTHON_VERSION=3.10.0a6
# Wed, 10 Mar 2021 17:03:25 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 10 Mar 2021 17:05:12 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:05:13 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Wed, 10 Mar 2021 17:05:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Wed, 10 Mar 2021 17:05:15 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Wed, 10 Mar 2021 17:06:08 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:06:09 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065958960304cba475fb20d779c909f51b0fd4cd8898b3b32e3a57ff66a4170`  
		Last Modified: Wed, 10 Mar 2021 13:23:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b38229e34b36e5e83834fb28b62f3e1252e8c0ebc9ef18f2feb366f15f76df2`  
		Last Modified: Wed, 10 Mar 2021 17:27:03 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7153a58ee5a66f4518c3bff6edd7ad532b282a3019b0433e0d698b516c7f5406`  
		Last Modified: Wed, 10 Mar 2021 17:27:02 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f32314a1ea162d8296472836194e607713c2c65f46f0061de5957dc98c0280f`  
		Last Modified: Wed, 10 Mar 2021 17:27:16 GMT  
		Size: 55.9 MB (55920582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52a9662b9f7e15848ec18dd4f259d43239e074668a3118a24d32c41ad3bb2391`  
		Last Modified: Wed, 10 Mar 2021 17:26:59 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a228a74ceb55217239b6c7dc721845b3556ee52bdaa186e9099967cd1e0282`  
		Last Modified: Wed, 10 Mar 2021 17:26:59 GMT  
		Size: 1.4 KB (1428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680858beaa43b1803e3db39a7f3f9936c2e55862aa7bc0ee5056a7d6f304ab0c`  
		Last Modified: Wed, 10 Mar 2021 17:26:59 GMT  
		Size: 1.4 KB (1375 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a41f5b4194deefb4ed98f298d637b9213ac4172657a2ccb6a238365bc85fee`  
		Last Modified: Wed, 10 Mar 2021 17:27:03 GMT  
		Size: 10.4 MB (10367835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1be948ad2ac8733508d408885477e8737e849cc74a3cb964ff8ad3bc57334ebd`  
		Last Modified: Wed, 10 Mar 2021 17:26:59 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
