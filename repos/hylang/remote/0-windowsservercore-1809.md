## `hylang:0-windowsservercore-1809`

```console
$ docker pull hylang@sha256:cb0cb0f110fef980c4c8a72f6acc6be0d4fcb4a25c6c5528b1cb4fd70b337278
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `hylang:0-windowsservercore-1809` - windows version 10.0.17763.1817; amd64

```console
$ docker pull hylang@sha256:a3db6aa301efbde55624428a362db0ff1c6e40cd125307c3d90df8da016efa4b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2535782019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:111f0d5ce56b3c3d3b48fdfbdd506e4ab04e17585be33b69cd334efcb0bacb40`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sat, 27 Feb 2021 09:32:06 GMT
RUN Install update 1809-amd64
# Wed, 10 Mar 2021 13:08:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Mar 2021 13:15:52 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 10 Mar 2021 17:18:48 GMT
ENV PYTHON_VERSION=3.8.8
# Wed, 10 Mar 2021 17:18:49 GMT
ENV PYTHON_RELEASE=3.8.8
# Wed, 10 Mar 2021 17:20:38 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:20:39 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Wed, 10 Mar 2021 17:20:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/b60e2320d9e8d02348525bd74e871e466afdf77c/get-pip.py
# Wed, 10 Mar 2021 17:20:41 GMT
ENV PYTHON_GET_PIP_SHA256=c3b81e5d06371e135fb3156dc7d8fd6270735088428c4a9a5ec1f342e2024565
# Wed, 10 Mar 2021 17:21:29 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 10 Mar 2021 17:21:30 GMT
CMD ["python"]
# Wed, 10 Mar 2021 17:32:23 GMT
ENV HY_VERSION=0.20.0
# Wed, 10 Mar 2021 17:33:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 10 Mar 2021 17:33:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5ff1512f88ecd4ff0a91ade34d43733c48834433e35f062f80e6e70d706f8d73`  
		Size: 743.2 MB (743201590 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:ebe61daec6d671bc2c1c6fe61ac9825fb552e9cef3672d0a7dbec719d125ae64`  
		Last Modified: Wed, 10 Mar 2021 13:21:09 GMT  
		Size: 1.4 KB (1430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f065958960304cba475fb20d779c909f51b0fd4cd8898b3b32e3a57ff66a4170`  
		Last Modified: Wed, 10 Mar 2021 13:23:23 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:787a7751bc9a13e0364ef545640f03c4f9002ae20ff643c980b1daccd181691e`  
		Last Modified: Wed, 10 Mar 2021 17:29:22 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5108afddd43a9abc69d23a117a7f8fbddd264727014ab52209042b67dcdb1f2b`  
		Last Modified: Wed, 10 Mar 2021 17:29:22 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5490fece4863272a83a82d6388693e2e4736f716e7285539d6f6b78733cf4362`  
		Last Modified: Wed, 10 Mar 2021 17:30:31 GMT  
		Size: 58.4 MB (58390683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1580f65a73d469df9bedfef70816e24ef5933d75f309d9295334a5d50962eea8`  
		Last Modified: Wed, 10 Mar 2021 17:29:19 GMT  
		Size: 1.3 KB (1304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eba1fbcd06e65d98744e39344921d4c05b9f650c9556b7cdb22c4ae99fc83b`  
		Last Modified: Wed, 10 Mar 2021 17:29:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c967098df1544a0cbcf641f0a6d9f70b5ce3ec47f605a20730d3e30d0ca27c`  
		Last Modified: Wed, 10 Mar 2021 17:29:19 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c14885975a12a1b00a3e91af1ef16c84a1544f616ca09acb467039b2c12f9a3`  
		Last Modified: Wed, 10 Mar 2021 17:29:22 GMT  
		Size: 10.3 MB (10263318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dd054a4f6a2d339c1b95b847d258135fb35164c37febe733bf803e48b5c12e1`  
		Last Modified: Wed, 10 Mar 2021 17:29:19 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:625a8c1f4a773ff8adcca867f62f97b3617556d09db5927489d62691ae4f7b42`  
		Last Modified: Wed, 10 Mar 2021 17:38:27 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d974b1b8b0f4965cec876c240620f8fb32f38ada6492d7e8d2570bc616257feb`  
		Last Modified: Wed, 10 Mar 2021 17:38:29 GMT  
		Size: 5.6 MB (5580057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c7cbb65dc4fc24587a55a36f1a79d4337a17d1fc17052ec8cf7735c9a27cb5`  
		Last Modified: Wed, 10 Mar 2021 17:38:28 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
