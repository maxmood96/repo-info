## `python:windowsservercore-ltsc2025`

```console
$ docker pull python@sha256:a9709de6847620acc316c20ab8a0adc6e83dbd1986c2cb4cfc8dfe4f201751a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `python:windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull python@sha256:f582959a3477a157dee3393006de3310ec06157554e9ac8fa045b769618fb287
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2875823528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881133dbee25d57f34284e66091c42d80f5ed2d5f43ef424a330b5f712caa4dd`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:19:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:19:49 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 27 Feb 2025 18:19:50 GMT
ENV PYTHON_VERSION=3.13.2
# Thu, 27 Feb 2025 18:19:50 GMT
ENV PYTHON_SHA256=9aaa1075d0bd3e8abd0623d2d05de692ff00780579e1b232f259028bac19bb51
# Thu, 27 Feb 2025 18:20:26 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:20:27 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df28dcdc00fff5e99740ba7e116fd991b4ad366e98d116b3893e7ccf8a9fb6f6`  
		Last Modified: Thu, 27 Feb 2025 18:20:32 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942607b9332f30100c205e615ce719e5e2f316294749fd1a2eb7d06d9eb9d456`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:716858a622feb9a682026644e4fbe8087e5aa6cff761775ce0193343643f576d`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ccde2c33c608b17afd3771acecc785a5dde123c2be40db7741bd17a6972f4da`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4426c8487343a55a451137d3d67494764bcc8e7c18324178ffdba51aaa71797e`  
		Last Modified: Thu, 27 Feb 2025 18:20:36 GMT  
		Size: 59.2 MB (59229467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4cbfd1782739db32db8bab3fc9f46aab21a33db63aa3529a527bf489b4262d8`  
		Last Modified: Thu, 27 Feb 2025 18:20:31 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
