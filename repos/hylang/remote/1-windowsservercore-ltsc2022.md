## `hylang:1-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:f2ed68759d918bfc1e736f673012cd8800b2ecd785e66e212e23f8be52f6b2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `hylang:1-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:23c822784c9eb1e1087bf7d77a21337d95e9a322e1d250055f93b04547d687c8
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2139797641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde495f9e1abe747af47db2eedd488b55dde6e229b6c24f41cf20de35d2295a9`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 12 May 2026 00:15:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 00:15:19 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 00:15:20 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 00:15:21 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 00:17:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 00:17:48 GMT
CMD ["python"]
# Tue, 12 May 2026 01:15:37 GMT
ENV HY_VERSION=1.2.0
# Tue, 12 May 2026 01:15:37 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 12 May 2026 01:16:59 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 12 May 2026 01:17:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa492a5535facf20fd9ea86ddfd2827b386ca74f28e0073a7b036eb7144c3259`  
		Last Modified: Tue, 12 May 2026 00:17:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c110293bde293f107cb8e63a12efd4de91f702d40bddc927558968f01bd2ffe4`  
		Last Modified: Tue, 12 May 2026 00:17:53 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b916de7d92cdc52e03b9503f4acec9aa8c497860fcf21d2a7d2a6adb0ca6c0`  
		Last Modified: Tue, 12 May 2026 00:17:53 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cac99f356ae10d3f434c17cd2e258f390e30b2bbf3722a0591f2ef21d97667a3`  
		Last Modified: Tue, 12 May 2026 00:17:53 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e660438cf2d4f2a517361b8279fa61a6f6ed46d6294a0ef5ac1b8598fcce7236`  
		Last Modified: Tue, 12 May 2026 00:17:59 GMT  
		Size: 61.3 MB (61321806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e6c6a52371b72354c19fc38b8dd0f7566e224e8962b85f068ba6f5612c3296`  
		Last Modified: Tue, 12 May 2026 00:17:53 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71e987a3a026c688f03e233a20585ae5987e9abec34036c41e02f3e7f1c16373`  
		Last Modified: Tue, 12 May 2026 01:17:04 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3510eca65223f6f7890381a5c5ef03abeb9620bed6e491865907842f122a5d`  
		Last Modified: Tue, 12 May 2026 01:17:04 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72e42de5f1c22dec39852db8161e4d193359f99ee0c175ddf3832af3c5dae2ec`  
		Last Modified: Tue, 12 May 2026 01:17:05 GMT  
		Size: 8.3 MB (8254090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac71e1effa7e5312992d32ff341f02b63ed4cae6c94ec26d2c73030eab4d778`  
		Last Modified: Tue, 12 May 2026 01:17:04 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
