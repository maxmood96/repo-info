## `hylang:windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:f4a638f61bb055e6c28dd30cb9f75e247b9def1226a498f59c67bffccb0c6d55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `hylang:windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull hylang@sha256:85c4c33c61f82db63e78abda88b57e1891ddc3afda49bc0bcb46e4a29746b836
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1849278774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612f3f589b4ad22120d6bebc31c84d9ff03b0d7f5e9d4737b382d42d2c614882`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:46:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Dec 2025 20:46:50 GMT
ENV PYTHON_VERSION=3.14.2
# Tue, 09 Dec 2025 20:46:51 GMT
ENV PYTHON_SHA256=9db919cefe30a0051658c600a9912acb0cd2b872aaf35842c9ec2bf401efa848
# Tue, 09 Dec 2025 20:47:32 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:47:33 GMT
CMD ["python"]
# Tue, 09 Dec 2025 21:18:07 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 21:18:07 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 21:18:37 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Dec 2025 21:18:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768ea431b13531bd18fa519503dcde235d1371c06640fff6c434a8dc2f78f370`  
		Last Modified: Tue, 09 Dec 2025 20:40:48 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34587e3124c2354fd0c0ebc422da5a49bd90585ddb565123a6a607568a27d77f`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f73959298aa0c72f2ef4c2adaca9c6319ad8f57fb3ad3139a3ffb6f2bcc4a5b3`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6b048b9df31de6a2a4089f32d19b21bd49c1d7b7f74b76ccb3aa9c0bc59fa8`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ee5ca9163acd37c8180f34b414cf06699edfa777c693d18342d5ef32acf65d1`  
		Last Modified: Tue, 09 Dec 2025 20:47:56 GMT  
		Size: 60.9 MB (60925935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00182617a1921b03d51762122e1f5fba52b8fc8b81bb5dce8c52a89e1006f37f`  
		Last Modified: Tue, 09 Dec 2025 20:47:53 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4a90193fde56b94387115cb7a9bb70247f3edc2ad56c4ff21a7f579334ba0f0`  
		Last Modified: Tue, 09 Dec 2025 21:18:50 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00d4a78ee2079fb5985f93c52b3f084eccb212b54c40ba741e5420246382084`  
		Last Modified: Tue, 09 Dec 2025 21:18:49 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee27e8ac372fc8a0aae394d73c7808d9d8e95cb91b4399b0636a296d5b5d5f7`  
		Last Modified: Tue, 09 Dec 2025 21:18:50 GMT  
		Size: 8.5 MB (8463038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d5d0fa7ccdddd9c04be3e2eee5ef7917d4dcd00aad2f373a94f8adbb7168fb8`  
		Last Modified: Tue, 09 Dec 2025 21:18:49 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
