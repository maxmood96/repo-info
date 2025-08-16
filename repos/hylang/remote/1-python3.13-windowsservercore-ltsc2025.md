## `hylang:1-python3.13-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:1fdbb7717e5ffb3e5309c13806d3c109cf2903459147ec08dcc74d26b8e80857
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4946; amd64

### `hylang:1-python3.13-windowsservercore-ltsc2025` - windows version 10.0.26100.4946; amd64

```console
$ docker pull hylang@sha256:200d8f018201160fe4d1b77814533756c411a5699efaadd982982665cddcca66
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3566046703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd47ecf2888d35ca84ee95c577378ee39a149384555295b7a3ad4432409be1b`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 10 Aug 2025 03:12:45 GMT
RUN Install update 10.0.26100.4946
# Fri, 15 Aug 2025 22:07:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 15 Aug 2025 22:07:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 15 Aug 2025 22:07:49 GMT
ENV PYTHON_VERSION=3.13.7
# Fri, 15 Aug 2025 22:07:49 GMT
ENV PYTHON_SHA256=b12e2e82461ac8e51fc43289050bc8eb937a32d84ce4d242e2c88258c37cf2bb
# Fri, 15 Aug 2025 22:08:24 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 15 Aug 2025 22:08:24 GMT
CMD ["python"]
# Fri, 15 Aug 2025 23:12:19 GMT
ENV HY_VERSION=1.1.0
# Fri, 15 Aug 2025 23:12:19 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 15 Aug 2025 23:12:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 15 Aug 2025 23:12:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:203c144449ed67b479a4424fa1d1138f1c8909f1e47a45a6500d4d7f7d058549`  
		Last Modified: Tue, 12 Aug 2025 20:45:36 GMT  
		Size: 1.3 GB (1283523307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d8c8b88701ea0d995113e23039ff24150e3d75e88bc093436cca65341c936a`  
		Last Modified: Fri, 15 Aug 2025 22:11:48 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd323cbf4de778cf2d038caad259c69c67981a63d30301bbbacc4ff81e4e1f77`  
		Last Modified: Fri, 15 Aug 2025 22:11:48 GMT  
		Size: 1.3 KB (1343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77e8b2ffeabbede2932a47f4892859f91bd8df2087d2706ffc4e2bb8c87d6db`  
		Last Modified: Fri, 15 Aug 2025 22:11:47 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe7da1108ec1f6bdbc425c19696023b33affde2fb5189653452a3314495228c`  
		Last Modified: Fri, 15 Aug 2025 22:11:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f2eaec8d515e7c1067415d037cd614cfa633efb47f89abebefbac8ef7b3d45d`  
		Last Modified: Fri, 15 Aug 2025 22:11:53 GMT  
		Size: 58.7 MB (58685213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d2fd4b045b5d48fade36b9f0dd7343fa7ffa9c1c9b16c0c44d63213c690460`  
		Last Modified: Fri, 15 Aug 2025 22:11:47 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:737ac486667b2c6607ba9f5b6a9b50e2285d5b78921745c3c17b29633bab6209`  
		Last Modified: Fri, 15 Aug 2025 23:13:03 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb24bb89465d1c8524ceb122d78a2d289048c7b552bcb43e0b2aa454f649540`  
		Last Modified: Fri, 15 Aug 2025 23:13:03 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f59e6afbbcc7939cf154e487b71442465f095fd19bb2ff004b11b7b6fa0f0747`  
		Last Modified: Fri, 15 Aug 2025 23:13:03 GMT  
		Size: 8.5 MB (8520521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ebf3f298f5572e985462748439632e7bd8c87417156b6a08da7d8928d9dea2`  
		Last Modified: Fri, 15 Aug 2025 23:13:02 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
