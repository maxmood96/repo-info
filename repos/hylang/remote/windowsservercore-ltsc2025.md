## `hylang:windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:ac1e418a10291048a935ad9049b5f260bb663875145d34fc02ccd67b600106b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `hylang:windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull hylang@sha256:a92a35d1c758bd835a5f2c8bcc495373c0ec1e2c92647c78930977d09f4f64b3
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2884451382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b4a0a99fdd1253aab4ef3755f426ff253a737d798a635659d6530f08150bfc`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:19:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:19:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 27 Feb 2025 18:19:50 GMT
ENV PYTHON_VERSION=3.13.2
# Thu, 27 Feb 2025 18:19:50 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Thu, 27 Feb 2025 18:20:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:27 GMT
CMD ["python"]
# Thu, 27 Feb 2025 19:13:45 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 19:13:46 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 19:14:20 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 27 Feb 2025 19:14:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df28dcdc00fff5e99740ba7e116fd991b4ad366e98d116b3893e7ccf8a9fb6f6`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942607b9332f30100c205e615ce719e5e2f316294749fd1a2eb7d06d9eb9d456`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716858a622feb9a682026644e4fbe8087e5aa6cff761775ce0193343643f576d`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccde2c33c608b17afd3771acecc785a5dde123c2be40db7741bd17a6972f4da`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4426c8487343a55a451137d3d67494764bcc8e7c18324178ffdba51aaa71797e`  
		Last Modified: Thu, 27 Feb 2025 18:20:36 GMT  
		Size: 59.2 MB (59229467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cbfd1782739db32db8bab3fc9f46aab21a33db63aa3529a527bf489b4262d8`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a50a6ed998386c7e6ab69a6ae0edc9e35bb3a01dc15ef192764c5b48fbe8e462`  
		Last Modified: Thu, 27 Feb 2025 19:14:25 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2618d751e6ea1fa165bd46d304b7b5cca5a2c266b9c779ccb0ada89baf0023a0`  
		Last Modified: Thu, 27 Feb 2025 19:14:25 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea04414d74d9498e6668006c3e443d26b89ad43dffdb00273f99971bfadb0d3`  
		Last Modified: Thu, 27 Feb 2025 19:14:27 GMT  
		Size: 8.6 MB (8623915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e491ab1a095e06b5d8ba79e303a4bf411f3d410adb1c4aae247d2d52346aff28`  
		Last Modified: Thu, 27 Feb 2025 19:14:25 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
