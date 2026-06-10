## `hylang:1-python3.14-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:04bc829d0d708d8915f1fb6210ba58c57446ae28476fca8857cd908dc46b40a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `hylang:1-python3.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull hylang@sha256:fe2cf7938f26291e7df44e77bd26e4b99f4d92bee6c2e03a69d3739af9c26e72
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2201691481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1124cbbd71ebc3222b4c5df2f184743b9288acc2450769b8e4424887e15dfc00`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Tue, 09 Jun 2026 22:19:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2026 22:25:44 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Jun 2026 22:25:44 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 09 Jun 2026 22:25:45 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 09 Jun 2026 22:26:30 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2026 22:26:31 GMT
CMD ["python"]
# Tue, 09 Jun 2026 23:27:00 GMT
ENV HY_VERSION=1.3.0
# Tue, 09 Jun 2026 23:27:01 GMT
ENV HYRULE_VERSION=1.1.0
# Tue, 09 Jun 2026 23:27:44 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Jun 2026 23:27:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89a031fbbd9fc892ef9346929f87c3acb83aa1453c7e42f79e7f8a2c465848d9`  
		Last Modified: Tue, 09 Jun 2026 22:20:15 GMT  
		Size: 1.3 KB (1335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc1403ff79d352831c57624ed6b7e9e9e9a241112611349f0a547a998a29093a`  
		Last Modified: Tue, 09 Jun 2026 22:26:35 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac82d4b9d9044e56cf7a9712d2886864294887c3d8c0cb44350d406504d57201`  
		Last Modified: Tue, 09 Jun 2026 22:26:35 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34c1ba018f2739c0ef9fa31a1e47fc23d780e7485aad6ce67465a3aa9bd10567`  
		Last Modified: Tue, 09 Jun 2026 22:26:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4b93b8cfd1ec5d7ca34a8bca1a8463237b94ade54d6f25cc211b6364dc40bdb`  
		Last Modified: Tue, 09 Jun 2026 22:26:40 GMT  
		Size: 61.3 MB (61276657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62171d2d1327487253a3b59fbb3035ddc4a83e239e4b1ae7a443fb36cc5b57f7`  
		Last Modified: Tue, 09 Jun 2026 22:26:35 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bbd198b70e8a8c925859e947302f5551e5c73033626751ba4fa0c2c69c0454`  
		Last Modified: Tue, 09 Jun 2026 23:27:49 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c467ecc63d3efe807d7794ba4d2fadece183d7c6008b6fdd83afd145f327b0b`  
		Last Modified: Tue, 09 Jun 2026 23:27:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fde9ab80ca8203e8a0f27cf344f073e91f34529f36c2bdf822d98fa0b90894b`  
		Last Modified: Tue, 09 Jun 2026 23:27:51 GMT  
		Size: 8.3 MB (8278784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9581919e3d6997509abec0e036b6d04a26e51114d8211ca08010b38c85f2fe`  
		Last Modified: Tue, 09 Jun 2026 23:27:49 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
