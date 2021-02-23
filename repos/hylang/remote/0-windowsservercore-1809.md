## `hylang:0-windowsservercore-1809`

```console
$ docker pull hylang@sha256:1f3df707be4341c720005900a741191d1a9419640f89bbd85bf91ac30ab7c3a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `hylang:0-windowsservercore-1809` - windows version 10.0.17763.1757; amd64

```console
$ docker pull hylang@sha256:39ea9f63c9e94d479434ad85e45e81b01ae4ca7e402c4c730e1561123095b087
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2513496215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e134216ad662a15da146be4aa21715cc7c13fe47f8cca70c69c42f90a3017341`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 06 Feb 2021 05:03:14 GMT
RUN Install update 1809-amd64
# Wed, 10 Feb 2021 13:14:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Feb 2021 16:07:47 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 19 Feb 2021 17:15:12 GMT
ENV PYTHON_VERSION=3.8.8
# Fri, 19 Feb 2021 17:15:13 GMT
ENV PYTHON_RELEASE=3.8.8
# Fri, 19 Feb 2021 17:16:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Fri, 19 Feb 2021 17:16:48 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Mon, 22 Feb 2021 23:36:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Mon, 22 Feb 2021 23:36:24 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Mon, 22 Feb 2021 23:37:15 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 22 Feb 2021 23:37:16 GMT
CMD ["python"]
# Tue, 23 Feb 2021 00:00:18 GMT
ENV HY_VERSION=0.20.0
# Tue, 23 Feb 2021 00:00:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Tue, 23 Feb 2021 00:00:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:db4edcf0861ff3fdc41851a5a218965ecb2ab6cf4ec9448fb80cc4b6792fd46c`  
		Size: 720.9 MB (720933935 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:433d24156d44dde3b3c6c0094ba5824a315286ae537c68f272e464fc426510f6`  
		Last Modified: Wed, 10 Feb 2021 13:40:44 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b84e06535ce9db874df389992b93e0bd5a992e8067ba9fc73059f40ef8966dd`  
		Last Modified: Wed, 10 Feb 2021 16:34:31 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8570537397cc82fc5105f8a51a7be0d1839eac7c0a3f9cd85f5a5eb53e7b5675`  
		Last Modified: Fri, 19 Feb 2021 17:24:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4110edbb8d1a7fdf8163c2f8170b9a984b78f430a39c6a387ce06c11a53d6e`  
		Last Modified: Fri, 19 Feb 2021 17:24:26 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17836fdac3fedcdb8f751737777097ee892c7d022a224c314dc11a8a334a195e`  
		Last Modified: Fri, 19 Feb 2021 17:25:33 GMT  
		Size: 58.4 MB (58370707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e21f55a40d7e8b4223794dbb255a092d48a849410544177e0438a61306c63381`  
		Last Modified: Fri, 19 Feb 2021 17:24:23 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74cc44b2069cd912c1657c6d2b7a3f91fdb42f5f809f61c624299955ee979b61`  
		Last Modified: Mon, 22 Feb 2021 23:43:07 GMT  
		Size: 1.4 KB (1433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49eb9677f9946957a0c9d7eba346674018a3c65b534a280e094fb3b56837e675`  
		Last Modified: Mon, 22 Feb 2021 23:43:07 GMT  
		Size: 1.4 KB (1437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dadfe76a756e424ca6da70b491fd8e5b4fa75c2496a8b98e46b1ee105a6f48c6`  
		Last Modified: Mon, 22 Feb 2021 23:43:11 GMT  
		Size: 10.3 MB (10269613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa703cc785ad8eadf0f0b5024fe64ac41799aec40698ddd82ed0b81bc9c2956`  
		Last Modified: Mon, 22 Feb 2021 23:43:07 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe51c184af98c30e486b8fa5705b721b60d29ae38b558eac4bce9490f9f7d01f`  
		Last Modified: Tue, 23 Feb 2021 00:02:24 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4f60d8003adce11df10bcde3bac1f3a55c1847b1e522592aa244056174de38`  
		Last Modified: Tue, 23 Feb 2021 00:02:31 GMT  
		Size: 5.6 MB (5574972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7cb20693447ee2bba313ad2d83d901b8516efa9888cb74290946e644bd71649`  
		Last Modified: Tue, 23 Feb 2021 00:02:24 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
