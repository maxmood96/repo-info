## `hylang:windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:bf4a19e46da5746df02aac3bbacfa8ddbac72fd6b908ab48c684e1cd7e19a578
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.2894; amd64

### `hylang:windowsservercore-ltsc2025` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hylang@sha256:221a6ff3564b1331f6dd873a7d42139d7b005aee8a239ee1c13f1a04622940ea
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2567983461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5deffcbff5624e4f7434159bdbe789be01f29e4d6ee8bdb3eeb428221d39d6e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 07 Feb 2025 00:30:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 07 Feb 2025 00:31:00 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 07 Feb 2025 00:31:01 GMT
ENV PYTHON_VERSION=3.13.2
# Fri, 07 Feb 2025 00:31:01 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Fri, 07 Feb 2025 00:31:38 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 00:31:39 GMT
CMD ["python"]
# Fri, 07 Feb 2025 01:32:30 GMT
ENV HY_VERSION=1.0.0
# Fri, 07 Feb 2025 01:32:31 GMT
ENV HYRULE_VERSION=0.8.0
# Fri, 07 Feb 2025 01:33:07 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 07 Feb 2025 01:33:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495d022befc252f16e30d0b28906f6b25bc4d445dafbc41a6870fda1de17620a`  
		Last Modified: Fri, 07 Feb 2025 00:31:43 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca83ef037f2fe51dda91ffaef25b4d63581cf5bc979f3991758dd60fb77c106`  
		Last Modified: Fri, 07 Feb 2025 00:31:42 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52ccb7e4d250586313393724b92aa5fdebb8fb81d76e2d497b1de501515fcf12`  
		Last Modified: Fri, 07 Feb 2025 00:31:42 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc9fd392efa278c1dd899868c36d9da63be94a1be6f475b3ddcaa818ee576a0c`  
		Last Modified: Fri, 07 Feb 2025 00:31:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab22a7f1a28c376fc6e39aa2a5961c2e67d73080dd121b31bc38c663fcddf0b8`  
		Last Modified: Fri, 07 Feb 2025 00:31:47 GMT  
		Size: 59.2 MB (59150828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c659753739a733bf36a30042844244ca436e7471833a1d28be654af65c813cd`  
		Last Modified: Fri, 07 Feb 2025 00:31:42 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c669a9491322f6e533397a2703e04b979ebb740276ee5ad02d959bb3bb335de`  
		Last Modified: Fri, 07 Feb 2025 01:33:13 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65380fdea6d05106f3e4494c106f91316c7f84a0b523ee87160ed69c82c8e81c`  
		Last Modified: Fri, 07 Feb 2025 01:33:13 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6e7c11b278bc937c20be5bcdee30febe413a014fe34aadc79d5356168b233ae`  
		Last Modified: Fri, 07 Feb 2025 01:33:14 GMT  
		Size: 8.5 MB (8544613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15defd2178cc95b450372a50cff5e67d81239a4d814ecec4fa66746013f41622`  
		Last Modified: Fri, 07 Feb 2025 01:33:13 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
