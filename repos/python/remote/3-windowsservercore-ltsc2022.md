## `python:3-windowsservercore-ltsc2022`

```console
$ docker pull python@sha256:a0dc97c7903bc0397d4f5d4746aeb45d75f08e98c6e33dcc41e4f517f9290007
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `python:3-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull python@sha256:710689618f9ae9e10c3259255cd7b82fb716d1c3143d719928cc5b288a320922
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2311250135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2eda6deff1e9f9781313a5388f325083ff590583de0e71afb34784aa13e49dd`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Thu, 14 Nov 2024 20:17:12 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 14 Nov 2024 20:17:13 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 14 Nov 2024 20:17:13 GMT
ENV PYTHON_VERSION=3.13.0
# Thu, 14 Nov 2024 20:17:14 GMT
ENV PYTHON_SHA256=78156ad0cf0ec4123bfb5333b40f078596ebf15f2d062a10144863680afbdefc
# Thu, 14 Nov 2024 20:17:55 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 14 Nov 2024 20:17:56 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a81c2266e7829c520aa3c90760450f9de85265d31ef76e07c116d21d86cb9d5`  
		Last Modified: Thu, 14 Nov 2024 20:17:59 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8bf73e26732f051db38c88937e307507b46733de79214bd6526da79565b0467`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84bd722ec005c4b9a8d4ce74d1547245ee36e178a58fbca74ea8a88b83557a2a`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e33fa699c69073e7247ec2d3a42da4118d465f9912cba354ef0845112bcffd`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ee35dfd6d09fa868757d9bc44d68b28573a959fe0a6fe736dc0b05b3a790a5`  
		Last Modified: Thu, 14 Nov 2024 20:18:03 GMT  
		Size: 58.8 MB (58759488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c7965bd14123d662cc223a68643149c706713ffcb3745193c4f5c3c25c928`  
		Last Modified: Thu, 14 Nov 2024 20:17:58 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
