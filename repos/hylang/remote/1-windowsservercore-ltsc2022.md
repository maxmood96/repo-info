## `hylang:1-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:6cf50490e1b286717a777544774e22f3b4a030398e71d3cdf6fd2082253596d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4294; amd64

### `hylang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.4294; amd64

```console
$ docker pull hylang@sha256:dc2bebd291f87706bc29a325c1b0fa7dcd67edcf3e52df2cb0b21dfa63d9c990
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.6 GB (1558226783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12ae9e5cc1e2a8530d483db656870e4a769d59591be8ea803580ae9bd3054ce6`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:52:13 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Oct 2025 20:52:14 GMT
ENV PYTHON_VERSION=3.14.0
# Tue, 14 Oct 2025 20:52:14 GMT
ENV PYTHON_SHA256=52ceb249f65009d936e6504f97cce42870c11358cb6e48825e893f54e11620aa
# Tue, 14 Oct 2025 20:52:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:52:59 GMT
CMD ["python"]
# Tue, 14 Oct 2025 21:15:24 GMT
ENV HY_VERSION=1.1.0
# Tue, 14 Oct 2025 21:15:25 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 14 Oct 2025 21:15:57 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Oct 2025 21:15:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800e1d3f69793c122ec179934d6ba62874c4636dfa09f29bd4cc31d710eab334`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6630854127e48eff983c9583ba7f439c13165201231652bd8457cc0e75980cf8`  
		Last Modified: Tue, 14 Oct 2025 20:53:19 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad47887bf7a4581a5f91db76f9de9deaeee16fc01c8c25874da9ecfac9447fd3`  
		Last Modified: Tue, 14 Oct 2025 20:53:20 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246776fbb336c73671db0b21f27f4d47aedadaa2e0e9664e1ecf6966f4b02817`  
		Last Modified: Tue, 14 Oct 2025 20:53:20 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aa78356ac1b33a08e19d12a3a8f38d4d3b79091aaf92b7785bf8cc6132c2868`  
		Last Modified: Tue, 14 Oct 2025 20:53:23 GMT  
		Size: 60.7 MB (60698618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624c6b4fe7a02f353cdb37a88a94e0a889d0588cbeabc74479a000cbf56df7a8`  
		Last Modified: Tue, 14 Oct 2025 20:53:20 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8537409d645d513b2e085954d80ac8a6ebd15d90b16e694ecdd3de3474c636bb`  
		Last Modified: Tue, 14 Oct 2025 21:16:10 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de34934bb09bcbc80e586d9f5addfd011f47cfef16cf6613734afcc7b6f91a4d`  
		Last Modified: Tue, 14 Oct 2025 21:16:10 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50279fb95a382c6c8bc7010c2f038f4dddcf5fe63d63197f0daff5c6ea858e05`  
		Last Modified: Tue, 14 Oct 2025 21:16:11 GMT  
		Size: 8.5 MB (8498528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2681eca769784b7a9cb545f5b68a9c1a0049c6e4f977e82725777aa8f8405d05`  
		Last Modified: Tue, 14 Oct 2025 21:16:10 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
