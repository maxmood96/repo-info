## `hylang:windowsservercore-1809`

```console
$ docker pull hylang@sha256:ba9c6dc3e80b2fa113dd7a65242e250b7725a17e05b2803e25927aa9ebb3933c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2114; amd64

### `hylang:windowsservercore-1809` - windows version 10.0.17763.2114; amd64

```console
$ docker pull hylang@sha256:7574b88e072efbc444d066b9e7eff368a3d4e20013faf11fcd8c99f46db2af72
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2743680398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373a43f2493945854c063f80238b98cb4d7ad25aeee6764f5d1e86e759576052`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Tue, 24 Aug 2021 23:22:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 25 Aug 2021 12:35:53 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 31 Aug 2021 18:15:17 GMT
ENV PYTHON_VERSION=3.9.7
# Tue, 31 Aug 2021 18:15:18 GMT
ENV PYTHON_RELEASE=3.9.7
# Tue, 31 Aug 2021 18:17:04 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Tue, 31 Aug 2021 18:17:05 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 08 Sep 2021 00:26:29 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 08 Sep 2021 00:26:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/c20b0cfd643cd4a19246ccf204e2997af70f6b21/public/get-pip.py
# Wed, 08 Sep 2021 00:26:32 GMT
ENV PYTHON_GET_PIP_SHA256=fa6f3fb93cce234cd4e8dd2beb54a51ab9c247653b52855a48dd44e6b21ff28b
# Wed, 08 Sep 2021 00:27:55 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 08 Sep 2021 00:27:58 GMT
CMD ["python"]
# Wed, 08 Sep 2021 00:51:03 GMT
ENV HY_VERSION=1.0a3
# Wed, 08 Sep 2021 00:52:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 08 Sep 2021 00:52:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:547a42a22856b8c453f88ea7796b08c15b248d73f09976ca0044162fb9d12390`  
		Last Modified: Tue, 24 Aug 2021 23:25:12 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:723798581711620321543fadca5f5b861c2af4dafbe2c3acdb59945488cf07f9`  
		Last Modified: Wed, 25 Aug 2021 12:42:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b684a127bb8c10cc6f53031849b1087be1beb93e1747099a52b945110c4d95a`  
		Last Modified: Tue, 31 Aug 2021 18:22:20 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e0c0c3e9a11e4a195182a593e149c539e17651a37871060e3917a41bcf734c`  
		Last Modified: Tue, 31 Aug 2021 18:22:20 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99d5745da387ba09f57d52ebe4cb48eb1c09d61362d0394ab22c766c046a7ab1`  
		Last Modified: Tue, 31 Aug 2021 18:23:13 GMT  
		Size: 50.0 MB (50015961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18492fa4e1c8990c50de0f5e3596d9510792058379866818ce1373a52fc32378`  
		Last Modified: Tue, 31 Aug 2021 18:22:17 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8855122529cb80d0cb1b4b72a85cb3bc631e52d693f2b2a188a8b6207d5c11c3`  
		Last Modified: Wed, 08 Sep 2021 00:32:43 GMT  
		Size: 1.4 KB (1447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ac8abc9be3bb358886d47c932c54e584a2533afebdac109dc3380b3562538ab`  
		Last Modified: Wed, 08 Sep 2021 00:32:43 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbb7fa98469cbf79b5a02be9bcdc015c18ded6f2fd5007145b4f8f5db51ac2ac`  
		Last Modified: Wed, 08 Sep 2021 00:32:44 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3758726bba8f150c018946ee18d3ae67157e82dd4578e6a9ff55b2580c7f1d`  
		Last Modified: Wed, 08 Sep 2021 00:32:50 GMT  
		Size: 6.3 MB (6316414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbc89d6e62dde34485724452fcf09532cafd778249cb037de4ea4fd8aaa54288`  
		Last Modified: Wed, 08 Sep 2021 00:32:43 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc8fd7dbd3fd5a82739989e3d2ef5a0d3cb877dd6ff18907ca172be7d01c7f25`  
		Last Modified: Wed, 08 Sep 2021 00:54:21 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e720fa38c02d0d4f8dc269f010cb31bb2c2d5cd60c8d81c3d32681cee4ebc48`  
		Last Modified: Wed, 08 Sep 2021 00:54:21 GMT  
		Size: 1.3 MB (1334901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82c6055f2ba521d292d3bc68f68499e607aab5b436ac790de865177b4a4b1f3f`  
		Last Modified: Wed, 08 Sep 2021 00:54:21 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
