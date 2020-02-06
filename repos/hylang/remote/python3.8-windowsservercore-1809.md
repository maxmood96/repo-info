## `hylang:python3.8-windowsservercore-1809`

```console
$ docker pull hylang@sha256:11a523920692408550d9fea0d5e8851f1f990ace2cdc8d42ecb8143c277c6d46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `hylang:python3.8-windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull hylang@sha256:368c96e4529b181760da4a972c8495d2a749687c5c967bcb8fc658a9bc927508
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2275743218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:109b1b113b6d23dcd712832d1a5524688b439042c3d5577d84ca1da966610e97`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:11:26 GMT
ENV PYTHON_VERSION=3.8.1
# Wed, 15 Jan 2020 18:11:27 GMT
ENV PYTHON_RELEASE=3.8.1
# Wed, 15 Jan 2020 18:14:03 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Sat, 25 Jan 2020 02:29:28 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 02:08:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 02:08:11 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 02:09:15 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 06 Feb 2020 02:09:17 GMT
CMD ["python"]
# Thu, 06 Feb 2020 02:27:21 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:27:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 06 Feb 2020 02:28:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:edbd72df76b46e904108d2f61a63c295b3e3d8092dbd5a03bbeb2fb4d34a3e55`  
		Size: 682.7 MB (682725872 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e9d323e253cb21832421dda4ec57dbd597bd4f934e62c162b9dec8b96e06e818`  
		Last Modified: Wed, 15 Jan 2020 01:45:20 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65000235543c235c2e74f20f8e573cf69307c2ae02b1da87836bd07879db990`  
		Last Modified: Wed, 15 Jan 2020 18:40:16 GMT  
		Size: 1.2 KB (1199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c81bd408e276049f315c96dd7550ba36423eaa23352e455338693de51dbe598`  
		Last Modified: Wed, 15 Jan 2020 18:40:17 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10e442f8dbfac6ca2f8e635e2b255617a0105f41a8b953f6d2194688469b07c`  
		Last Modified: Wed, 15 Jan 2020 18:40:44 GMT  
		Size: 51.8 MB (51770493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27f741971ef01de0e3d720debe60e0d9c40d4d6e7e4ad2044fbfdc58f3322f13`  
		Last Modified: Sat, 25 Jan 2020 03:12:38 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b7ffe247d73f3b6a3e5de4e2dde626a84e96e61cf8db3e63953c1fbd0db98a`  
		Last Modified: Thu, 06 Feb 2020 02:21:04 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b07ca0ab437b95722dcd07a1943251846728cb2e6a51770253465086dbe2763`  
		Last Modified: Thu, 06 Feb 2020 02:21:04 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b803e990865f1f4732254e277cb193e616d68dde9720f43eb53bd77ec0eff512`  
		Last Modified: Thu, 06 Feb 2020 02:21:13 GMT  
		Size: 5.4 MB (5405761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7748eb3b4b42d541ebf8ffd44d4ab55328e7acdee3fab1f6e6f225f4fcaca7f`  
		Last Modified: Thu, 06 Feb 2020 02:21:04 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb5321414e3dbbb3ad27278f637ae88e5a1233471e8cfb52c5e1287bab4e6152`  
		Last Modified: Thu, 06 Feb 2020 02:33:08 GMT  
		Size: 1.2 KB (1204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed21e35c92c21c96c8ff70d832ab3d70c76b3b743f1d0a13a52ac20a6745865`  
		Last Modified: Thu, 06 Feb 2020 02:33:11 GMT  
		Size: 1.1 MB (1145041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d48250d0dbdac0eb8c354f45af497e9aecfe670b29e7687383d764bf5e356e`  
		Last Modified: Thu, 06 Feb 2020 02:33:08 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
