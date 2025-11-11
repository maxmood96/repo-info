## `hylang:python3.13-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:627529f323b9dd41a2394a886ebc18b79d8a88760c5e4f2172824b01bac0474b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `hylang:python3.13-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:91b6321c1ad860425ff78649591ce73c12d3e78b43df73b612824d0b8869e380
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1837268718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d79db2387b173be271b9b3ca45cc4ce3d92e410d71d070d5219534b2afb718`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 11 Nov 2025 19:11:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 11 Nov 2025 19:28:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 11 Nov 2025 19:29:23 GMT
ENV PYTHON_VERSION=3.13.9
# Tue, 11 Nov 2025 19:29:23 GMT
ENV PYTHON_SHA256=200ddff856bbff949d2cc1be42e8807c07538abd6b6966d5113a094cf628c5c5
# Tue, 11 Nov 2025 19:30:10 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 11 Nov 2025 19:30:10 GMT
CMD ["python"]
# Tue, 11 Nov 2025 20:17:43 GMT
ENV HY_VERSION=1.1.0
# Tue, 11 Nov 2025 20:17:43 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 11 Nov 2025 20:18:12 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 11 Nov 2025 20:18:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b29d7d66d7f4ac3f8cb78bc5a6de4c14e194db152f15ca5ab40a5eff0480557`  
		Last Modified: Tue, 11 Nov 2025 19:22:14 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73838e40e1af50d120f4cf2803f8806778c9e9cb15dea399e878d946d8cdebe1`  
		Last Modified: Tue, 11 Nov 2025 19:29:16 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3147ed04d813eb6f3c62d5e92135e080d3d3f9dce9f81677b1b28bb897fa4d67`  
		Last Modified: Tue, 11 Nov 2025 19:30:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca8fc1a94602ac2d78bac4c005d611a158fe3e03f95a8d58cc526c3aec78bd2`  
		Last Modified: Tue, 11 Nov 2025 19:30:33 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6279a00ead958027dae89528a16a4df27f1bacc61cd65248bcb7fc3363446b48`  
		Last Modified: Tue, 11 Nov 2025 19:30:38 GMT  
		Size: 58.8 MB (58799899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162de7bf198c74b1dc61454d3c69c0c31a8ce59d974c525e2d3b8467af5be9d1`  
		Last Modified: Tue, 11 Nov 2025 19:30:34 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc75b4246b38079d686f0e6427459a7739dc16926abf3d56ebb5bffcad79bcbd`  
		Last Modified: Tue, 11 Nov 2025 20:18:27 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91a7cef6cfa67d1c2a9435b9266bbce87f019bf51e29db8b1e7887e2608c336d`  
		Last Modified: Tue, 11 Nov 2025 20:18:26 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d12e6704f9227aa57419cfe64380e3ae84d151ae65aaea7bd0a97b103c2a80f`  
		Last Modified: Tue, 11 Nov 2025 20:18:27 GMT  
		Size: 8.5 MB (8496835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b7b48d9eddbc69db79fc09c4ae29593e1ea2950c736a9c985feba08265a4d9`  
		Last Modified: Tue, 11 Nov 2025 20:18:27 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
