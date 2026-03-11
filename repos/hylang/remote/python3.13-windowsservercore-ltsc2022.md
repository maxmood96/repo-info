## `hylang:python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:2918f300c4a218ce8f62da8ca9488921660de1fbe790f263e9516986f49209c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `hylang:python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull hylang@sha256:01b396ed441eb63b14b47f7dd7f7aafca0bf67336e46845bee72709767262c9d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2049409961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4170f1f6c934618b369b122fc6e3e37958cf501cdb66ae3282b6948e9249cb5`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Tue, 10 Mar 2026 21:57:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Mar 2026 22:16:16 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 10 Mar 2026 22:16:16 GMT
ENV PYTHON_VERSION=3.13.12
# Tue, 10 Mar 2026 22:16:17 GMT
ENV PYTHON_SHA256=96159fcb523ae404b707186a75b4104ee23851e476a5e838e14584cf1e03f981
# Tue, 10 Mar 2026 22:17:00 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 10 Mar 2026 22:17:00 GMT
CMD ["python"]
# Tue, 10 Mar 2026 22:42:11 GMT
ENV HY_VERSION=1.2.0
# Tue, 10 Mar 2026 22:42:12 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 10 Mar 2026 22:42:44 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 10 Mar 2026 22:42:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6527849939a95bf8fe1da92d44d97fc937b8003df8ba3d4c2cf1ff70f58cbe3a`  
		Last Modified: Tue, 10 Mar 2026 22:00:50 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:389bdf5ddae8202e7290b8c756570695af855cc7a61d1f0c9ed97d819485ec8e`  
		Last Modified: Tue, 10 Mar 2026 22:17:04 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f92341997a4c5cb0709ee9775a53b197e16699518d93127ae75601989e1fcb2`  
		Last Modified: Tue, 10 Mar 2026 22:17:04 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f1d07a59359c1174ec6c3cc9c590efb4a8f8aeb5bc9483914edd75d350c2c6`  
		Last Modified: Tue, 10 Mar 2026 22:17:04 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2d74ed1c57f583fbadc9351e54554e4c4329fd06a057f8afee9752d7325d5c`  
		Last Modified: Tue, 10 Mar 2026 22:17:10 GMT  
		Size: 58.9 MB (58869045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6df113a64bd3ce59902b240ad971ceb0d6e278f52baec7f7c639a248131df837`  
		Last Modified: Tue, 10 Mar 2026 22:17:04 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ef67ec8d6e03f3dbbd483028aae165c31deffcc054f936b6d8cfd5c3c719b3`  
		Last Modified: Tue, 10 Mar 2026 22:42:48 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6813ed94a05e20fb00de90e47f99e9c28f822590d82c282222bd3e169db0cca`  
		Last Modified: Tue, 10 Mar 2026 22:42:48 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91cbd840f962870c2f129bf81e2d8a425f373d4341fe7c6bf763f1c1fa834448`  
		Last Modified: Tue, 10 Mar 2026 22:42:50 GMT  
		Size: 8.2 MB (8248971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b227d8b2d900bd5a2b0f5eb6278be2fb562660bd99d18d1acf8c1f919b9c22a0`  
		Last Modified: Tue, 10 Mar 2026 22:42:48 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
