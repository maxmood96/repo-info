## `openjdk:jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:d02f238eae57c64608a573ac4b4724983c5d5074518214e1bda37335f8f01151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3443; amd64

### `openjdk:jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.3443; amd64

```console
$ docker pull openjdk@sha256:56652f469589ec4cfb55b8482f09737cd8e1a4c5e971cd23b0d66d2fa0969470
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5931931086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e81eb8e922d304a1095f4f84e72bce8e4993a692d57c23119a2655a540ccb74`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 02 Jan 2020 15:48:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Jan 2020 23:50:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2020 23:51:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 15 Jan 2020 01:11:14 GMT
ENV JAVA_HOME=C:\openjdk-13
# Wed, 15 Jan 2020 01:12:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 15 Jan 2020 01:12:26 GMT
ENV JAVA_VERSION=13.0.2
# Wed, 15 Jan 2020 01:12:28 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk13.0.2/d4173c853231432d94f001e99d882ca7/8/GPL/openjdk-13.0.2_windows-x64_bin.zip
# Wed, 15 Jan 2020 01:12:29 GMT
ENV JAVA_SHA256=fab29dcfda6ca4af3a9b973ecdde61dafcd9b307cb9237c25d25b2633bb08084
# Wed, 15 Jan 2020 01:15:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 15 Jan 2020 01:15:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:31f9df80631e7b5d379647ee7701ff50e009bd2c03b30a67a0a8e7bba4a26f94`  
		Size: 1.7 GB (1654613376 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f1c8c4c99f36cfcf87884a9382011e93fb05fa4002d8f4eca62a43e744db8e95`  
		Last Modified: Wed, 15 Jan 2020 01:46:47 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59f69707d10b5be4e5c56881ea890fd476325bea3b16b5a7e7c56a1d8b3f056`  
		Last Modified: Wed, 15 Jan 2020 01:46:54 GMT  
		Size: 5.4 MB (5386027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:510d21e1edc23bf2cbacb69556bb393c24e88845058efd04a86ea154f503bc10`  
		Last Modified: Wed, 15 Jan 2020 02:01:27 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:778aedc6b6e869c8ad7637796826b9cdec2be5b4533599ca2a942a4b194f0415`  
		Last Modified: Wed, 15 Jan 2020 02:01:30 GMT  
		Size: 5.4 MB (5367601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd79f52df9a16f24641cf433a350532d2dccc97b0ae51162fd34d10ba5df479`  
		Last Modified: Wed, 15 Jan 2020 02:01:24 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f349bf7adfba0aad0dcab398bd7da688db00ebbea36402e377b114bd10b24b3a`  
		Last Modified: Wed, 15 Jan 2020 02:01:25 GMT  
		Size: 1.2 KB (1205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb54b11e6ca8b5d153ae68438f2b61ac3e4ee4ff25a4c0d9c75454ea40f101a`  
		Last Modified: Wed, 15 Jan 2020 02:01:24 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff097e04fb5cae63b20509db00e06bd5bbe11a6b6a283137e472dc1409bc3b1f`  
		Last Modified: Wed, 15 Jan 2020 02:01:50 GMT  
		Size: 196.6 MB (196571020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7313b6cde37d215fb63db23d6749e8b33c76114aaa52cb3c67241c1b77a71ed7`  
		Last Modified: Wed, 15 Jan 2020 02:01:25 GMT  
		Size: 1.2 KB (1190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
