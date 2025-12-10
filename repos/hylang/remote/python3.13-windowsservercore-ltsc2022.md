## `hylang:python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:b5a7290371a727ed7e3c1654b6f30325d71460b9dcf1a08c8cb7012890e6c5a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4529; amd64

### `hylang:python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.4529; amd64

```console
$ docker pull hylang@sha256:ce6d7ae349e7e5b932e1aa21d3a52bb8f624e83ce4dd25bfdc25034ec38feece
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1847153115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23258ebd13218f65b5c9b6a97f1932048dcb8c1f44d3b1c3924352f57bf1306a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 05 Dec 2025 18:19:35 GMT
RUN Install update 10.0.20348.4529
# Tue, 09 Dec 2025 20:32:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Dec 2025 20:46:17 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 09 Dec 2025 20:47:24 GMT
ENV PYTHON_VERSION=3.13.11
# Tue, 09 Dec 2025 20:47:25 GMT
ENV PYTHON_SHA256=30d4654b3eac7ddfdf2682db4c8dcb490f3055f4f33c6906d6b828f680152101
# Tue, 09 Dec 2025 20:48:03 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Dec 2025 20:48:03 GMT
CMD ["python"]
# Tue, 09 Dec 2025 21:18:09 GMT
ENV HY_VERSION=1.1.0
# Tue, 09 Dec 2025 21:18:09 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 09 Dec 2025 21:18:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 09 Dec 2025 21:18:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc19ec18c41e4c8edf1a76eecae2be22e29445f11ee586523f59e36de40aebb`  
		Last Modified: Tue, 09 Dec 2025 19:51:50 GMT  
		Size: 290.9 MB (290860200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4337b0b452250939272a24a7d25392c5f6351fbf9da067a0d397cefbb4266c7a`  
		Last Modified: Tue, 09 Dec 2025 20:40:35 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cb76f9c857371dc211aa10e19e3a121d4b7dd689c73c15474d0cba3583190ba`  
		Last Modified: Tue, 09 Dec 2025 20:47:16 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8071bd409c058180095ca911cbeb4e4ed8953ca01d34e4a8290842fea5d3f534`  
		Last Modified: Tue, 09 Dec 2025 20:48:28 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:360f0317d9b088931eec903d8c0ffbef6697e7e8c7ac42476d9d09e08615066d`  
		Last Modified: Tue, 09 Dec 2025 20:48:28 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f5bca479208072e16107bce161077d9c38fa7d81cc8375b849727cc2230b21e`  
		Last Modified: Tue, 09 Dec 2025 20:48:32 GMT  
		Size: 58.8 MB (58831862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c1c897dde87d3e623259dc384a2a8b89f3869b15c8103d1e75378aaec552113`  
		Last Modified: Tue, 09 Dec 2025 20:48:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23e9ea8fea92e370929d948c1d0f7c7faab0e28d21ed1066507c4f7157343a46`  
		Last Modified: Tue, 09 Dec 2025 21:18:52 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac1a00d08fa2dde47e9c667ba9e32f28e0d8994f248d91a9ced8a4ac0c1feb01`  
		Last Modified: Tue, 09 Dec 2025 21:18:52 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e22fe753615882ac91f52fa18d18f174eaf1aa14a81afe3cb9da25f9246f232e`  
		Last Modified: Tue, 09 Dec 2025 21:18:55 GMT  
		Size: 8.4 MB (8431523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0534ba92a58884e050de27463f57943888f72e2192040a725d798d243c791267`  
		Last Modified: Tue, 09 Dec 2025 21:18:52 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
