## `hylang:python3.12-windowsservercore-ltsc2025`

```console
$ docker pull hylang@sha256:15da870d5e73452191263aa13061401aad9ee419b95df15dd1f2bf647d65c06c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `hylang:python3.12-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull hylang@sha256:9bb5fb9715dd549ddc7188553d657a5b3dd9dee3c1f7dbf011003a3b8bf8eefe
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2885315919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32442cf8c0f65a63225496d2f0294809efa228015ce299634aa230ed4f93b32a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:20:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:20:37 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 27 Feb 2025 18:20:37 GMT
ENV PYTHON_VERSION=3.12.9
# Thu, 27 Feb 2025 18:20:38 GMT
ENV PYTHON_SHA256=2a52993092a19cfdffe126e2eeac46a4265e25705614546604ad44988e040c0f
# Thu, 27 Feb 2025 18:21:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Thu, 27 Feb 2025 18:21:17 GMT
CMD ["python"]
# Thu, 27 Feb 2025 19:13:15 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 19:13:16 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 19:13:49 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 27 Feb 2025 19:13:50 GMT
CMD ["hy"]
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
	-	`sha256:57ac51967e9677653e0a81ce4c692751864212960c03237dd270e67cfd913c72`  
		Last Modified: Thu, 27 Feb 2025 18:21:22 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df7982d4cdf54531c76aa4302d4b154e8ed58e845a3fbd3ef3eab1c5838a2c3f`  
		Last Modified: Thu, 27 Feb 2025 18:21:21 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ea703a9cff76ff572fa08236c30334f0d3eb512e01a4ee26ac97d070b2bff5`  
		Last Modified: Thu, 27 Feb 2025 18:21:21 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c6ef6d43bbb33a09ff9c731d327a84b5317ae58307041f14afdd91b2a6789af`  
		Last Modified: Thu, 27 Feb 2025 18:21:21 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ff9363f4ad660b9c0d8015c592527c8cdc811b5739a2a126fedc33377039245`  
		Last Modified: Thu, 27 Feb 2025 18:21:26 GMT  
		Size: 60.1 MB (60099108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e9a69bdbaa4d72a966464ba694c48a8ae48d36e207391859887e8656bd0f76`  
		Last Modified: Thu, 27 Feb 2025 18:21:21 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb9e0cc19b028603e1a1ffd107acfc992a6431d9e4326ed6e4e26ecbe14a7be`  
		Last Modified: Thu, 27 Feb 2025 19:13:52 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4234aecbedb8676ad5b9883c63b32d148b4cbbcfa3c06214bfe7c439b30b62`  
		Last Modified: Thu, 27 Feb 2025 19:13:52 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f321440dc0c0eaf844a53650a2fbe40cb45591621ddd5d0b612ecac6200dced`  
		Last Modified: Thu, 27 Feb 2025 19:13:53 GMT  
		Size: 8.6 MB (8618842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:755840f1403354b70ed3c6b529d284a663a3e569f2855195612e5791fadd5e94`  
		Last Modified: Thu, 27 Feb 2025 19:13:52 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
