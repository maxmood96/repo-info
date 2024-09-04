## `hylang:0-windowsservercore-1809`

```console
$ docker pull hylang@sha256:4b11a24f8664d925a9c1c01530641ea8490d7f27121f9664ab711918ff68a1cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `hylang:0-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull hylang@sha256:0cffaa140b6a747a760a94458f2cd8c22994ae695fcbb73ad17b888408afddaa
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2312074267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14c702c7bd1453fb6a359d0eca6ea6b2ea4de91f499b531956b4e747f271595`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Wed, 04 Sep 2024 05:58:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 04 Sep 2024 05:58:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 04 Sep 2024 05:58:11 GMT
ENV PYTHON_VERSION=3.12.5
# Wed, 04 Sep 2024 06:01:05 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 04 Sep 2024 06:01:06 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 04 Sep 2024 06:01:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 04 Sep 2024 06:01:07 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 04 Sep 2024 06:01:37 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		--no-setuptools 		--no-wheel 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 04 Sep 2024 06:01:38 GMT
CMD ["python"]
# Wed, 04 Sep 2024 06:54:29 GMT
ENV HY_VERSION=0.29.0
# Wed, 04 Sep 2024 06:54:31 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 04 Sep 2024 06:56:31 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 04 Sep 2024 06:56:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3287ed6269f13ebeb31204931c5219204c2bd56c14d3b133a2332d5b7269f6`  
		Last Modified: Wed, 04 Sep 2024 06:01:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cef1b820f123ab4999af3e5a2dc04a1e6a290b22651a843deae7fe4b044959a9`  
		Last Modified: Wed, 04 Sep 2024 06:01:44 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0b14b92a0538bf4202abff0f9e94ecf4930e2a2dd01ce0e218fce3ead3a36e`  
		Last Modified: Wed, 04 Sep 2024 06:01:44 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8a4f69a09bb11252ba4bb70dfbd7317b1ebc47aee7394ac02d432338dcd01c`  
		Last Modified: Wed, 04 Sep 2024 06:01:48 GMT  
		Size: 47.9 MB (47906946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e8040e7d3bde2c55fe0435fffd592c5a3424b996b1eed0d0f2661681b331e65`  
		Last Modified: Wed, 04 Sep 2024 06:01:42 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11562c8f2db8f88a77ac41d40c96cdabd7986eeb1903c08bd5a1b20a19913f08`  
		Last Modified: Wed, 04 Sep 2024 06:01:42 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61aac0e131afcf1d1c29d467ab95e05a7e41449a64624ef4035403c16f66576f`  
		Last Modified: Wed, 04 Sep 2024 06:01:42 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d85c9aec2119077b620b12edb7bf755759d27d7bf5bea1de59ecf4d36e1507a3`  
		Last Modified: Wed, 04 Sep 2024 06:01:43 GMT  
		Size: 8.4 MB (8360221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a2f6befa54ea1d82955518a79be29103c1c21a6f1174b2102ac62141e45b0a0`  
		Last Modified: Wed, 04 Sep 2024 06:01:42 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02b61be2a37b0b9f64634b339753210d4493b3e327acb26781eabbba7910cc10`  
		Last Modified: Wed, 04 Sep 2024 06:56:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73f52806d8e95279722258eff2a24956174b4f604f6045daeea7446d84e6324`  
		Last Modified: Wed, 04 Sep 2024 06:56:35 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ecac89750d2a878a39c087bb1f9a63bb5703f7f9b08f621c2bad1b8f07da39c`  
		Last Modified: Wed, 04 Sep 2024 06:56:37 GMT  
		Size: 10.6 MB (10590917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:489af9d423bed1e07df3be214da4485b4274dac3da2fc2598dd8ee9104749259`  
		Last Modified: Wed, 04 Sep 2024 06:56:35 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
