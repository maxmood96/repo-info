## `openjdk:26-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:1c8f74e24c74c67166f7f2768aa59babb396696faf17518cb7a7e538d53244e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4405; amd64

### `openjdk:26-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4405; amd64

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
