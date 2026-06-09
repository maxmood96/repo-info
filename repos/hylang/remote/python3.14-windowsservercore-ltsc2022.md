## `hylang:python3.14-windowsservercore-ltsc2022`

```console
$ docker pull hylang@sha256:24c9297d92e65cfd50ea3ee7b86d28bc5165681fcc81238ce399744762edcfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `hylang:python3.14-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull hylang@sha256:facb9281051e85d0afd72abb131dddd78cfa26a0b6a26adb0c35df12c52dc02e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2192804559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:490ed5867399b262fb3ee0c446e1c1543488375555afba0470a44e7d80ef8587`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 12 May 2026 23:38:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 12 May 2026 23:58:09 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 12 May 2026 23:58:10 GMT
ENV PYTHON_VERSION=3.14.5
# Tue, 12 May 2026 23:58:11 GMT
ENV PYTHON_SHA256=f9c09f5ed6f796fd1a8bc5ddfa41715a494b453c4781f0e35d5077cf9fa58f6d
# Tue, 12 May 2026 23:58:51 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 12 May 2026 23:58:52 GMT
CMD ["python"]
# Mon, 08 Jun 2026 22:50:20 GMT
ENV HY_VERSION=1.3.0
# Mon, 08 Jun 2026 22:50:21 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 08 Jun 2026 22:51:08 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 08 Jun 2026 22:51:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31cbb80a80947ff97fb5674c26478afa4331c7d4b2fefabd1ea650765bffae78`  
		Last Modified: Tue, 12 May 2026 23:40:06 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f7f3cfa06a6dfb39cc22416a3fe6eff4b710bfeeccf05db45d77158ff23cf7b`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91ad01b1d407414ae266c6d5f8d9c0bb0b2689fe371c38a7571438ad85c0e7f`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74178a30e0303c0c21ed95e5ff390e5b58a1a755bd7d53d4167832a08c74400e`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c55dd5cfe2037fd17b90af958774b3cbfbd7147faa9264d71df2de5ca55808f`  
		Last Modified: Tue, 12 May 2026 23:59:02 GMT  
		Size: 61.7 MB (61678797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:114d0893892b1275f89469f1046c4d8eb67d669829d0ed2b72970a4b73e53803`  
		Last Modified: Tue, 12 May 2026 23:58:56 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac5edde93fa4e79c267ee4299f8419a728124b6156316f3dad5594a086004017`  
		Last Modified: Mon, 08 Jun 2026 22:51:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f4b16880abc3d16155165272e7958f06746e5e640781273d1d428ece67c64b`  
		Last Modified: Mon, 08 Jun 2026 22:51:14 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c34534b63b359b6d91ecb88088a63c1ae1219ac733ea723805beba17d7978d`  
		Last Modified: Mon, 08 Jun 2026 22:51:16 GMT  
		Size: 8.7 MB (8694613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fcbc6c6c27c29c440d81acf7f685d61818bef52b8de9d11008797c65e27d682`  
		Last Modified: Mon, 08 Jun 2026 22:51:14 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
