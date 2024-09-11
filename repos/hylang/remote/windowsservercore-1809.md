## `hylang:windowsservercore-1809`

```console
$ docker pull hylang@sha256:010efc1a492a2bb60d79aa11b6bcff86e4a7ef3a65f128ca7efdcf5d293048b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6293; amd64

### `hylang:windowsservercore-1809` - windows version 10.0.17763.6293; amd64

```console
$ docker pull hylang@sha256:740d78376c612af0c0f3ea4ec883f86e3074858a7f9b8033337f3eae6f35a703
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1786973258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:180ae69c5d8ef7296f96f4075dd1985316de6225bd0f9e95871db874a9bf150a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 11 Sep 2024 00:02:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Sep 2024 00:02:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 11 Sep 2024 00:02:38 GMT
ENV PYTHON_VERSION=3.12.6
# Wed, 11 Sep 2024 00:03:16 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:17 GMT
ENV PYTHON_PIP_VERSION=24.2
# Wed, 11 Sep 2024 00:03:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Wed, 11 Sep 2024 00:03:19 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Wed, 11 Sep 2024 00:03:36 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		--no-setuptools 		--no-wheel 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Sep 2024 00:03:37 GMT
CMD ["python"]
# Wed, 11 Sep 2024 02:06:51 GMT
ENV HY_VERSION=0.29.0
# Wed, 11 Sep 2024 02:06:53 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 11 Sep 2024 02:07:40 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 11 Sep 2024 02:07:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f560c83830627c123ff413e55b6de3ee5fbfee6b0cbfdd207f84a0fa5dbabe`  
		Last Modified: Wed, 11 Sep 2024 00:03:43 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f88bf39a9028af5262433453507c59758287c5d851762f11b4241ebc7f73270a`  
		Last Modified: Wed, 11 Sep 2024 00:03:43 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d0bf9724728478c8b391172d613631d2b9d64f19bab4d0ca7c3c72117cae9f`  
		Last Modified: Wed, 11 Sep 2024 00:03:43 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77121c0bf571784cfab197704fbb498e90cd965229a1d0fc2968387271989e65`  
		Last Modified: Wed, 11 Sep 2024 00:03:47 GMT  
		Size: 47.7 MB (47735404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4da23ad3d45bae5016923a27cbf0d6f3c0358b2d286f48bf82fc46d685f8c22`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a19e9c54e8d1f299556f53061dc49ee73d21034f4c2352c7f6dd7e588f25021c`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e29125750ee0139846808fa3992b866b5fe50f440deb4e50c19fd15af19b23c`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0795a182284e72abe76116249a55711a9fb740c00228b9b8f15366a3a7af5c8f`  
		Last Modified: Wed, 11 Sep 2024 00:03:42 GMT  
		Size: 8.4 MB (8361567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329efd8926be934d5fa306a5cff348e1659f96a81a237a8e5d87990967340afe`  
		Last Modified: Wed, 11 Sep 2024 00:03:41 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40082e8bcaeaa982f5c01caf63751b8fb08178314dce47eca0c458fc14f7b7e`  
		Last Modified: Wed, 11 Sep 2024 02:07:45 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02d464700b45e441f008d16b67e9152ecedca5e7faa63de7d668a9e849e1d23`  
		Last Modified: Wed, 11 Sep 2024 02:07:45 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70eb7b4cd0504f18f7bbd3a288e336998419c8707b5bbd61614c95e5cbcc7c18`  
		Last Modified: Wed, 11 Sep 2024 02:07:46 GMT  
		Size: 10.6 MB (10594864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d394e58a17f6e32e352cdb65cdcadc790e7c56e078436a61750bc384c8ad404`  
		Last Modified: Wed, 11 Sep 2024 02:07:45 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
