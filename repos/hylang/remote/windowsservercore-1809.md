## `hylang:windowsservercore-1809`

```console
$ docker pull hylang@sha256:1a90e212c45947a3d39624360c897abc923a2bad4b2d0295661d05ae7d00687a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.973; amd64

### `hylang:windowsservercore-1809` - windows version 10.0.17763.973; amd64

```console
$ docker pull hylang@sha256:091b7f66b54fb614c93fa5d6e9f62f9328da43df0ac5f33ff7f70baaeb56662a
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2274928126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e632c53afb07d6c9f7e42134e268b97123934d2d0247a2d1f6415adb54dea0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 11 Jan 2020 05:23:25 GMT
RUN Install update 1809-amd64
# Tue, 14 Jan 2020 23:46:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jan 2020 18:21:20 GMT
ENV PYTHON_VERSION=3.7.6
# Wed, 15 Jan 2020 18:21:21 GMT
ENV PYTHON_RELEASE=3.7.6
# Wed, 15 Jan 2020 18:23:56 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Thu, 23 Jan 2020 22:30:57 GMT
ENV PYTHON_PIP_VERSION=20.0.1
# Thu, 23 Jan 2020 22:30:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 23 Jan 2020 22:30:59 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 23 Jan 2020 22:32:04 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2020 22:32:06 GMT
CMD ["python"]
# Thu, 23 Jan 2020 23:04:44 GMT
ENV HY_VERSION=0.17.0
# Thu, 23 Jan 2020 23:05:23 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Thu, 23 Jan 2020 23:05:24 GMT
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
	-	`sha256:ea0075ddccbb615fbc85871d2a0a68a914e7ac78aca3ed104814afa389bca3fa`  
		Last Modified: Wed, 15 Jan 2020 18:42:25 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e2afa1ef6bd2b3c4303f55af9bc56895a7ed0d99c30466abd4612acaeb8938`  
		Last Modified: Wed, 15 Jan 2020 18:42:25 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fad19f450e99e076a79708f4a96049ddd1e98b7aebe71dfc9d91a93dcee9b72`  
		Last Modified: Wed, 15 Jan 2020 18:42:51 GMT  
		Size: 50.9 MB (50855255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace898abb181cd8eec70d5f2a6c007e6ed43f8cd67d34c93a236847d047a2202`  
		Last Modified: Thu, 23 Jan 2020 22:42:23 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4cbce2b2648e73d3bc2b3584309cf69f1fc3edbf3db686c7b589f0c5a62e42`  
		Last Modified: Thu, 23 Jan 2020 22:42:23 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a6760ba799e50055dc498b50e88516a85768df3d335b4f833375327611171d9`  
		Last Modified: Thu, 23 Jan 2020 22:42:22 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa95b773ebd3903d972332516820ceac216c05b33ea74eb39f9d0a8fbb876fc5`  
		Last Modified: Thu, 23 Jan 2020 22:42:30 GMT  
		Size: 5.5 MB (5464067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207c6707a251d70c6dcba7444e9992b9267de4adb26fc2c881f8509e41d808c6`  
		Last Modified: Thu, 23 Jan 2020 22:42:22 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20056dd7724059496f2fd51fe04d902db59e9fb6ff71ce6388bec281ff89445b`  
		Last Modified: Thu, 23 Jan 2020 23:10:13 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b19fc0719aa4900b31180c77d2f14b62a83e0dcf5edd08ffa1d0916d89b7be7`  
		Last Modified: Thu, 23 Jan 2020 23:10:15 GMT  
		Size: 1.2 MB (1186943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b2c100f756d9bc20c674eaca5fc1e92e1f8af247f48961aff08bc2a8ab81dfb`  
		Last Modified: Thu, 23 Jan 2020 23:10:13 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
