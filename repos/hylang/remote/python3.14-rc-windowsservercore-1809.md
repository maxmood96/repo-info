## `hylang:python3.14-rc-windowsservercore-1809`

```console
$ docker pull hylang@sha256:c9331614aa5543d67ff57e4bef31f7140ed460587fea075b746cd4d78fcb7cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `hylang:python3.14-rc-windowsservercore-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull hylang@sha256:0c99bd5d8a19a94cbeb4fbb4c7dbd9ce170c123ea0b54d58541d44ade67ea301
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2253359200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14202bb9a33ff0e6fe8a58878328fafa1f3f3d83aea586b6ad332d2051d3db22`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 20:58:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 20:58:31 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 May 2025 20:58:32 GMT
ENV PYTHON_VERSION=3.14.0b1
# Wed, 14 May 2025 20:58:32 GMT
ENV PYTHON_SHA256=a878026c12b1a606d02f5bbf3ed65aa780ee8272964b8f95d8348ffa2d6ca096
# Wed, 14 May 2025 20:59:23 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Reinstalling pip to workaround a bug ...'; 	Remove-Item -Recurse C:\Python\Lib\site-packages\pip*; 	python -m ensurepip --default-pip -vvv; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 20:59:24 GMT
CMD ["python"]
# Wed, 14 May 2025 21:11:59 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 21:12:00 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 21:12:41 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 21:12:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Thu, 15 May 2025 19:24:26 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5758a99a633a6b453f305a28f132803fc1cd1a1b9b99d173d8d4469095a7a9ab`  
		Last Modified: Fri, 16 May 2025 15:58:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b0556f1cde44ffeebea76d6442f398cf9ac7eedbff5b140ece7fb322866ec6c`  
		Last Modified: Fri, 16 May 2025 15:58:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c3d71da20dd32128de60dfaa197ff51cfbd03651a239185e45231f7004a461`  
		Last Modified: Fri, 16 May 2025 15:58:14 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85b115367bbee830079c40a199ea35925180d63f20fde6b3895c0a635a353612`  
		Last Modified: Fri, 16 May 2025 15:58:14 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89eab9cd76de133416e8a94273afd5a890e77757f370ae78cc5a6363434292b`  
		Last Modified: Fri, 16 May 2025 23:39:34 GMT  
		Size: 62.5 MB (62464897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:939f2ee22806dd9e626035f1ff9f62df4868b1fdfdecce6c8924afc7bdccfbed`  
		Last Modified: Fri, 16 May 2025 15:58:15 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7858a2c09212cc159a9d2ec8f7f5c5cf170522154f094467be99f126ae9db3bb`  
		Last Modified: Fri, 16 May 2025 15:58:15 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f0fef59a33ab4fc8c9d4cfd43afc9074636549db0973980e7f76dd9b08a1c3`  
		Last Modified: Fri, 16 May 2025 15:58:15 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:218f98372964bc2c85ed671a2e67991619c3515f273cf2d67b95f4b897acf9c0`  
		Last Modified: Wed, 14 May 2025 21:12:47 GMT  
		Size: 7.2 MB (7166490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98140b83fbf006e91b70eb35e13c178baff1af047ca14a2a3208510343e8536b`  
		Last Modified: Fri, 16 May 2025 15:58:15 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
