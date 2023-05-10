## `openjdk:21-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:866264fcf17c503ff63f178e106c46507821eff0482f086cac2b9f410282f568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4377; amd64

### `openjdk:21-windowsservercore-1809` - windows version 10.0.17763.4377; amd64

```console
$ docker pull openjdk@sha256:feb4666f46b8b3d0ffc31ec40d147ba9d74f5620c6b10b850b3004c771e818c9
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2269577394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25184ce4617b886daada689c722e9208e2e5e97584491dabecfb13370a1db25f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 07 Jan 2023 05:37:58 GMT
RUN Apply image 10.0.17763.3887
# Fri, 05 May 2023 12:05:28 GMT
RUN Install update 10.0.17763.4377
# Wed, 10 May 2023 00:36:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 May 2023 02:54:18 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 May 2023 02:54:19 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 10 May 2023 02:55:54 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 May 2023 02:55:55 GMT
ENV JAVA_VERSION=21-ea+21
# Wed, 10 May 2023 02:55:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk21/21/GPL/openjdk-21-ea+21_windows-x64_bin.zip
# Wed, 10 May 2023 02:55:57 GMT
ENV JAVA_SHA256=956977cb5020e6f7b75a2e06336cf858b8b131d6a57f9b0ca0b7f9b62b4e82be
# Wed, 10 May 2023 02:57:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 May 2023 02:57:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6e222c5ada69382aa2b4fe30b23ae56c7e3ada92712109d20f3edd457a6120b6`  
		Last Modified: Thu, 12 Jan 2023 02:40:02 GMT  
		Size: 1.7 GB (1707943932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e01de39a0c44e24aa1912078d32ee54389b71154e509138cc4f5d1de42e7a32a`  
		Last Modified: Wed, 10 May 2023 01:47:41 GMT  
		Size: 364.1 MB (364091294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a238e462da347b2e29386c9883c0ec93c8dbce311782ea1c5abbec2a31d884`  
		Last Modified: Wed, 10 May 2023 01:46:46 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8712378a27a3538d7991a50dcb72abb565959575008a538c012500547b6acf3a`  
		Last Modified: Wed, 10 May 2023 03:00:47 GMT  
		Size: 441.2 KB (441178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c34b75cb4c34981b4a471f423e801ccecb0e509ef934ebed87377603d134a0b0`  
		Last Modified: Wed, 10 May 2023 03:00:46 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d0267ca94f1356d921f0a3b30e5336c9c1c0604b0f3cb81963ab715ba48ff81`  
		Last Modified: Wed, 10 May 2023 03:00:47 GMT  
		Size: 259.9 KB (259927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b40c011f29565be1b42c2fba7a78f5257eced90c2f6e063d0c95ad26ba3957b`  
		Last Modified: Wed, 10 May 2023 03:00:44 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0215f6e83e161f3474066f4289d32729d4696a3cb1944f6188c5f6410a20ac66`  
		Last Modified: Wed, 10 May 2023 03:00:45 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b479c5bfcdbd346860195696b79e6f97b1aaaacc2a1f855e812290435fe522f`  
		Last Modified: Wed, 10 May 2023 03:00:44 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7114ab5a8380afbc53d28721cb0ebc9d90aa915d8d2f20ec3942f4934425a0`  
		Last Modified: Wed, 10 May 2023 03:01:06 GMT  
		Size: 196.8 MB (196832579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2926b1788552448ce2684d93c4be845fcd1eeca0330074293ba844dd085f356e`  
		Last Modified: Wed, 10 May 2023 03:00:45 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
