## `openjdk:26-ea-27-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:8d66ab841460400486d08b9a9d38e859b69e3d0d802a9dc9fcfd0c1a6931c4f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7171; amd64

### `openjdk:26-ea-27-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.7171; amd64

```console
$ docker pull openjdk@sha256:6bbb49fb77386a335da6bd43997dc48b378b14f027b656360bd7a396e6927a25
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3461802924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb938c2dd4c78849dbe6376f57f89bfa2a1fcfc327285adad8a8f50098b00355`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Sat, 06 Dec 2025 00:40:29 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 06 Dec 2025 00:41:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:41:39 GMT
ENV JAVA_HOME=C:\openjdk-26
# Sat, 06 Dec 2025 00:41:45 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:41:46 GMT
ENV JAVA_VERSION=26-ea+27
# Sat, 06 Dec 2025 00:41:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/27/GPL/openjdk-26-ea+27_windows-x64_bin.zip
# Sat, 06 Dec 2025 00:41:47 GMT
ENV JAVA_SHA256=5fc8523fafe0bbe81e010d1bd57b12836c42cdd1f017e4492f67d56bde06f86a
# Sat, 06 Dec 2025 00:42:14 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 06 Dec 2025 00:42:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6d491b064d08a64d94dcb03d80d556f4a1ba7a494f3762485661160f954d6ca`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:010d7cdade1e0cb34ee9aff67aa859146fa0787f28c26935e9493391c1a9a9e7`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 392.0 KB (392004 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52d7c1e4d2b4eb18d0de48b2534dc228d0109411789a7ff557d5414f81de7822`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736b240bc5c784f6e99fa25c5cb00b7a003f3f7893816981e33d5fc39c5520b7`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 364.8 KB (364830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3a7d46e547a01cd0cf46ac0dbc7ee148d47ee4b105a68ee550fbf7c1404cff`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46926f79000d266664eb73df67f91260bc080e122af2c0ca7d356a879b822a48`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5f6b09c2b479f9916ad26c427ac992a6555696b15ecfecfa2126a2a00a4513a`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55ea24ab29c5df3e1a421d68afa37b2d5a0bf52ca08065a0e0b2e5fa4bb80a1f`  
		Last Modified: Sat, 06 Dec 2025 01:00:43 GMT  
		Size: 225.6 MB (225582415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:863c0b04b07e1cd4e3fa445ff7f9cbc2cc13e80714b56bb98c8cb91ea3adead0`  
		Last Modified: Sat, 06 Dec 2025 01:00:17 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
