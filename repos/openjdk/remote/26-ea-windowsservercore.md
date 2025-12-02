## `openjdk:26-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:15050d0c1a1fd6d5b5707f81c696d2827c0fe70bebececddec58699cb0767f0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-windowsservercore` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:1067b62207777465315d8d4c42c53deb65721559e134b03eb3c78557fba7d2ad
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3461678418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41839fadb07d23062536d269e571805902dabc176104d71de4369c79a11b9e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Tue, 02 Dec 2025 01:10:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 01:11:12 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Dec 2025 01:11:13 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Dec 2025 01:11:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Dec 2025 01:11:19 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 01:11:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_windows-x64_bin.zip
# Tue, 02 Dec 2025 01:11:21 GMT
ENV JAVA_SHA256=cb98fecf214c597d44d81bafafe31e5081a89d88a9852df649f5f63eb8d85cce
# Tue, 02 Dec 2025 01:11:49 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Dec 2025 01:11:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9d58270885cc9cb69babe9b14c133e093f4f8f3fbf99a88ed195be46c2c6cf`  
		Last Modified: Tue, 02 Dec 2025 02:11:33 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4dc96d86a907edbde89ff987437525af551d65acfb8d7801957dd5d24333dbf`  
		Last Modified: Tue, 02 Dec 2025 02:11:33 GMT  
		Size: 400.0 KB (399996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84b6d0dc9bc7bea6c0f48b06a0c501aaa4fad184ca9ecdefef6d89ffd39b21e`  
		Last Modified: Tue, 02 Dec 2025 02:11:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf456b51eaa4578ce32bccf00eba0138bf58bdcca43a553f4f07a801f954e96`  
		Last Modified: Tue, 02 Dec 2025 02:11:33 GMT  
		Size: 372.5 KB (372529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ccc5c51420708a3f2750431510faacd250a4def47b5f70588df2e7bc2774e8`  
		Last Modified: Tue, 02 Dec 2025 02:11:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ec9979904260aefd3485d58a77da8c3a22e1d907a8e5e37d88716de962a0070`  
		Last Modified: Tue, 02 Dec 2025 02:11:32 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8010fe7d0e1a7358f370030d9162c7c9ba0407165e32a6db19494420ada0d725`  
		Last Modified: Tue, 02 Dec 2025 02:11:33 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac3942d4e989df74d1360c846cbba79e436ce2d59287b498eb467a00d6f25aa`  
		Last Modified: Tue, 02 Dec 2025 02:16:56 GMT  
		Size: 225.4 MB (225442247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0ae451f4cb6531b7db641970e8e12bea318225c2b65165294e4d6bf760d0b17`  
		Last Modified: Tue, 02 Dec 2025 02:11:33 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-windowsservercore` - windows version 10.0.20348.4405; amd64

```console
$ docker pull openjdk@sha256:5c4691a95b932d29efbfb7295ecdcf42b581b48d83d2092964fe60e9fa0e316f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1996267761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29781d15d9f69830faeeab2b0ff5a4dab210560b6f85ce3f8ddd7e4c82c7f603`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Tue, 02 Dec 2025 01:05:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Dec 2025 01:06:52 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Dec 2025 01:06:52 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 02 Dec 2025 01:07:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Dec 2025 01:07:01 GMT
ENV JAVA_VERSION=26-ea+26
# Tue, 02 Dec 2025 01:07:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/26/GPL/openjdk-26-ea+26_windows-x64_bin.zip
# Tue, 02 Dec 2025 01:07:04 GMT
ENV JAVA_SHA256=cb98fecf214c597d44d81bafafe31e5081a89d88a9852df649f5f63eb8d85cce
# Tue, 02 Dec 2025 01:08:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Dec 2025 01:08:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ab1a9d0de11e92ba5de75a6ac48b90f08b8e1076d4f8af7cd9b07912a4c78d4`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2138fa60b8bc73c17e1de517c4df7dee481f45eef6aa1226e44269dc00c5aa58`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 512.5 KB (512549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b924d52f3392724040d28b9810ce8ce54e5be2b95a63b171960c6784d1eb919`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09382364591506449547bf311814a1a86c7c602a37c9c3523a7d2395b3c451cb`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 348.1 KB (348078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972ff492daf97c6f12f622d8398897a0ab9e601f97918cbc2bffcd01012fb678`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9672298818352fe36c25f21c1d5ec3b8666ccf01264432bf5c36b883368b954`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a95aad5105bdbd1313cd078d9d1397137420d9174f6af7dbfd5979badbd9e77`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a2f2787376218112139eef8084ab5e1ae69ff3d91eb57f929ede31182f0a6c`  
		Last Modified: Tue, 02 Dec 2025 02:14:05 GMT  
		Size: 225.4 MB (225437743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c17c02a963d243c258d54bf037bd3d1820002442ce2759b6110c8d6a123ff5e`  
		Last Modified: Tue, 02 Dec 2025 01:21:31 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
