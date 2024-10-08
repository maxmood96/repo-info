## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:4f162ed5d721315d26f8d674d03f827727f99364c7da48e5f8876a80b8bc9133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2700; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.2700; amd64

```console
$ docker pull python@sha256:f811abccfaecef78d7a891c29950e2dd14dbc41ecd41a6b6846b94476e5f752e
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.5 GB (1521325395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1e8e95a4d818dcff82162a4d8ac41bd4a0a14cd6539fbb1514141f8f47c82a`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Mon, 07 Oct 2024 23:58:14 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 07 Oct 2024 23:58:14 GMT
ENV PYTHONIOENCODING=UTF-8
# Mon, 07 Oct 2024 23:58:15 GMT
ENV PYTHON_VERSION=3.13.0
# Tue, 08 Oct 2024 00:00:48 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 08 Oct 2024 00:00:49 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dacc9cf43ea18ab2e023648b83f29a6fc511a553baad655abaf89574f23ffbd9`  
		Last Modified: Tue, 08 Oct 2024 00:00:51 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f036cc31607ccb3f675a0a26d5925993c032bc81479fbf2ffbe03839dc6d9087`  
		Last Modified: Tue, 08 Oct 2024 00:00:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a892ad50abcbba950c7464f5c2827e2cec1120eace3d0156e9df89c3f2c0a1`  
		Last Modified: Tue, 08 Oct 2024 00:00:51 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d2e0365b52d55cbfe5421afdf53d68d9638bda4d1ed2eaf8d3a222da14064`  
		Last Modified: Tue, 08 Oct 2024 00:00:55 GMT  
		Size: 59.1 MB (59127751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5764b309d6ebf7325ddc95ad15b5594f79843dc921da3c8cc7c374a354bb214d`  
		Last Modified: Tue, 08 Oct 2024 00:00:51 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
