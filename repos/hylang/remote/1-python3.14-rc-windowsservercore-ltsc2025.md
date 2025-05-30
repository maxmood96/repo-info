## `hylang:1-python3.14-rc-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:45ba01812443eb013607a2c25618e5b07fa4ea428199902a2c8d2683ec9931a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `hylang:1-python3.14-rc-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:c9e80cb5264fbd2c2f1cc189a6d4aeb3e2570da1c3ff593bca06f115b7a9f07d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3500537718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e83246e6c418aa6e24ba82665e5303add3ad8111fbdb95d422058e80b138bf3`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Tue, 27 May 2025 19:08:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 27 May 2025 19:08:02 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 27 May 2025 19:08:05 GMT
ENV PYTHON_VERSION=3.14.0b2
# Tue, 27 May 2025 19:08:08 GMT
ENV PYTHON_SHA256=279b1d0e2b1b6cece6f03e49218aacccfd10367e07b785edeb1d4135507434c1
# Tue, 27 May 2025 19:08:49 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 27 May 2025 19:08:50 GMT
CMD ["python"]
# Fri, 30 May 2025 18:07:15 GMT
ENV HY_VERSION=1.1.0
# Fri, 30 May 2025 18:07:16 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 30 May 2025 18:07:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 30 May 2025 18:07:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a2eaa54494d5af27696a142815c48433664878387c27512aa22a5f5bae41225`  
		Last Modified: Tue, 27 May 2025 19:08:53 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ce19014fa410f682b36e6c1c3c1804466ba0fa303c9a484b6635f992771e9e`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9e22507b0baff33137a06738f1c7bbb09b045287e7db623d4657cb8b9f9cb1`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5266167b69f48a40f038142528167aea3a9ebb92cd0ea5d5dd7d598fddba4871`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99e8f764a1d0e6db4652e12ea237080f07a6557594321fe50b7717dcef975961`  
		Last Modified: Tue, 27 May 2025 19:08:58 GMT  
		Size: 61.1 MB (61136052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7437defd922a03b279c0e42940c94e0d019f4786d2221650300c05e088ebf3`  
		Last Modified: Tue, 27 May 2025 19:08:52 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e7d147700273e2caa5f8fb07a135924e903c30b8d816b680b486672e86fb46`  
		Last Modified: Fri, 30 May 2025 18:07:51 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910a530b63b4d6c67e1e0f0d83424e98da3dd31fba86767a92c20b2782810e38`  
		Last Modified: Fri, 30 May 2025 18:07:51 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c44ec3c0dc37f46bf514d042f99467b77bd2990e25d78ed0b5812f51bc7e1f60`  
		Last Modified: Fri, 30 May 2025 18:07:52 GMT  
		Size: 8.6 MB (8625351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f07ec24d4d2544ea839421e72828d08a8ed4454189b734ced40e6897785066`  
		Last Modified: Fri, 30 May 2025 18:07:51 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
