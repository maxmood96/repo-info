## `hylang:python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:7d17c3156b703abf573870ecb81ba0813ced14d1ca71883f2b8d8df90c10b5e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `hylang:python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:f628a7418608afad515cb360698f26c2d245c9b4e06f32367a364a5a99317221
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3500537689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec07755e1211a561111e32f392e5067c81264c9c49ac4b897cc1159285cddbb0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Tue, 27 May 2025 19:08:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 19:08:02 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 27 May 2025 19:08:05 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 27 May 2025 19:08:08 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 27 May 2025 19:08:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 May 2025 19:08:50 GMT
CMD ["python"]
# Mon, 02 Jun 2025 17:51:44 GMT
ENV HY_VERSION=1.1.0
# Mon, 02 Jun 2025 17:51:45 GMT
ENV HYRULE_VERSION=1.0.0
# Mon, 02 Jun 2025 17:52:15 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 02 Jun 2025 17:52:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2eaa54494d5af27696a142815c48433664878387c27512aa22a5f5bae41225`  
		Last Modified: Tue, 27 May 2025 19:08:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ce19014fa410f682b36e6c1c3c1804466ba0fa303c9a484b6635f992771e9e`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9e22507b0baff33137a06738f1c7bbb09b045287e7db623d4657cb8b9f9cb1`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5266167b69f48a40f038142528167aea3a9ebb92cd0ea5d5dd7d598fddba4871`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e8f764a1d0e6db4652e12ea237080f07a6557594321fe50b7717dcef975961`  
		Last Modified: Tue, 27 May 2025 19:08:58 GMT  
		Size: 61.1 MB (61136052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7437defd922a03b279c0e42940c94e0d019f4786d2221650300c05e088ebf3`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:133efd304c358f679becd16a951bcc8c47accc6c0f96f710f4403addf9f00075`  
		Last Modified: Mon, 02 Jun 2025 17:52:18 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2212ffc46e9ec9952606dd23b7a801cb65fbfb2d3ae4f7148fe7afd3d91643ce`  
		Last Modified: Mon, 02 Jun 2025 17:52:18 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24cc6a00040254f829a7a7adca2bd5aeb3430eec2c904170761f2a0cfea6f58`  
		Last Modified: Mon, 02 Jun 2025 17:52:19 GMT  
		Size: 8.6 MB (8625278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a93c25552afca43badeda95b16e3adb3888e7cd646b2ea29fb56d781dd24cfc3`  
		Last Modified: Mon, 02 Jun 2025 17:52:18 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
