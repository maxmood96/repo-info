## `openjdk:17-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:a97ed7005ffa384b54cd826a4bbe7ed8f74b390ecdcb8dc24202c5f326c145c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1697; amd64

### `openjdk:17-ea-windowsservercore-1809` - windows version 10.0.17763.1697; amd64

```console
$ docker pull openjdk@sha256:0689d85a1833d5ecb0e82c4aefef6f8c5cb8555ab0b854196f25dc62aceb9784
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2631227717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:800d396eb5b6aa7b198ec850b21764f22f2699dfd9cfd263920cee9615afbc62`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 08 Jan 2021 08:50:52 GMT
RUN Install update 1809-amd64
# Wed, 13 Jan 2021 13:13:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 01 Feb 2021 19:15:47 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:15:47 GMT
ENV JAVA_HOME=C:\openjdk-17
# Mon, 01 Feb 2021 19:16:06 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:16:06 GMT
ENV JAVA_VERSION=17-ea+7
# Mon, 01 Feb 2021 19:16:07 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/7/GPL/openjdk-17-ea+7_windows-x64_bin.zip
# Mon, 01 Feb 2021 19:16:08 GMT
ENV JAVA_SHA256=7fa795be0deebf36bbf21b5775a7aae0a671642dd431b0b068a9db3e6f8306e0
# Mon, 01 Feb 2021 19:17:04 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 01 Feb 2021 19:17:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4dcc9a9b9e680514ef3fdfcc2ce08a3768f9e412703faa137f4a7c8297600052`  
		Size: 717.4 MB (717439216 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e00081a98bb2679c3c5f469e09d475980133a20987f9cae4cf4f7aedf59f9d8f`  
		Last Modified: Wed, 13 Jan 2021 13:17:19 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750be76c45d6cac9367b9122b5847700dbb4c36ccf93eceb4ab0a71c8e815e67`  
		Last Modified: Mon, 01 Feb 2021 19:52:54 GMT  
		Size: 9.4 MB (9385366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:662223a8e8b8225632d5378b29c751d503f8dcf00d7c9301a06f2f927752bbc2`  
		Last Modified: Mon, 01 Feb 2021 19:52:52 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8c5e84f5867b1987f252692d77ef0da416f7cc2c16e04642af3e59c1f80fba2`  
		Last Modified: Mon, 01 Feb 2021 19:52:52 GMT  
		Size: 344.1 KB (344056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fd43ffbf67d469edaf4838a19afc5bcf55d15f50d1ea73d625d459dd52d8087`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c4230bdffb2703960a924a8d76d972758f2b8514e296ca7ffae3ee2ac5bef8`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.4 KB (1371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e547e9e52fb352b22c558fdbe58c5d8bab5e5534a94f35b761a9267bd77d04`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18315f54cdd154e94d0830dab94bf96112d66eb25a9384587d1c209cac7991c8`  
		Last Modified: Mon, 01 Feb 2021 19:56:24 GMT  
		Size: 185.7 MB (185718187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddc098763ea180ca9d4ea731aa78ead7332830728ab56cf3cb16f5209afb44d8`  
		Last Modified: Mon, 01 Feb 2021 19:52:49 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
