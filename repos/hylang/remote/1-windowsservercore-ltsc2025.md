## `hylang:1-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:9bdf0660014a44c577b5d10554edb906dc8a959d988a6efb43370d7549560033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `hylang:1-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:be9156cdd049187247fcb55eb38e26a29cf9d4d20bc156b6de1c4b66039fca61
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3304768572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b30fc1bce43273487ccd9e55af886fdbe5eab1df46dab766380e756f604bebe`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 01:06:05 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 01:06:07 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Dec 2025 01:06:08 GMT
ENV PYTHON_VERSION=3.14.1
# Wed, 03 Dec 2025 01:06:08 GMT
ENV PYTHON_SHA256=74e1516408744190fcc12307c150de30902898444f77f85f4c2ac18f36788a80
# Wed, 03 Dec 2025 01:07:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Dec 2025 01:07:26 GMT
CMD ["python"]
# Wed, 03 Dec 2025 02:12:14 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:12:15 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:13:03 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 03 Dec 2025 02:13:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d45a5687ec46714f68b9dec2efacd73bde08924cc55d3e2f375120fc0027acd`  
		Last Modified: Wed, 03 Dec 2025 01:16:24 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd5ffa566e17e33db847bdf8d07e4d3515cec353c992df60d6052307ad7f3e45`  
		Last Modified: Wed, 03 Dec 2025 01:16:25 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:712641b7f5bedec62fe5a7723f2e6c455f0f715fa4e5dc4ae98ecd798abf7899`  
		Last Modified: Wed, 03 Dec 2025 01:16:25 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:124c3953d95b1f7cce6d5fce7401954249d931109eaf1a6dcae8c135b4d60d66`  
		Last Modified: Wed, 03 Dec 2025 01:16:26 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c791592b2747f84a77351d35acf579b64eb56e3a12d6317302128d10f121f253`  
		Last Modified: Wed, 03 Dec 2025 01:16:30 GMT  
		Size: 60.8 MB (60839158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074a5b8ba2a103f45a4cae30459f014a1e2a668a3c89b8eed01539a42888b4f0`  
		Last Modified: Wed, 03 Dec 2025 01:16:26 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0520fb6fe8b19a90771e795818d82809d7335929cc0ccc94a4e506de9aeb1053`  
		Last Modified: Wed, 03 Dec 2025 02:13:17 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6a9dffa00ce15e207ded35807bebe05510f923d2ca007227095aa1b5aae9fcb`  
		Last Modified: Wed, 03 Dec 2025 02:13:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624ee6e6fe04d1a6457614f86119f68c230e646575916a7723f390d490a6724b`  
		Last Modified: Wed, 03 Dec 2025 02:13:18 GMT  
		Size: 8.5 MB (8463113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6116193d7a63a5d8cc788a141b774e67b7aab0acb96c6b2ee90cba4df250e143`  
		Last Modified: Wed, 03 Dec 2025 02:13:17 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
