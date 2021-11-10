## `openjdk:windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:52ff3ed39f19c0d4f9fb5c5d2ab5e870e8c0ce6f836142edabf42338d451a1ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.14393.4770; amd64

### `openjdk:windowsservercore-ltsc2016` - windows version 10.0.14393.4770; amd64

```console
$ docker pull openjdk@sha256:335996da75b2d3638b792700e93a3e35e1938a4e2b8c6a492d5a8d7ef22b180c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 GB (6456258666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3697acc0af1d51d6aff2c9be6564800bdb11efe14a7037467ad8bb73945aee`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 03 Nov 2021 23:35:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 10 Nov 2021 01:53:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Nov 2021 20:29:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:36:31 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Nov 2021 20:37:28 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:37:29 GMT
ENV JAVA_VERSION=17.0.1
# Wed, 10 Nov 2021 20:37:30 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk17.0.1/2a2082e5a09d4267845be086888add4f/12/GPL/openjdk-17.0.1_windows-x64_bin.zip
# Wed, 10 Nov 2021 20:37:31 GMT
ENV JAVA_SHA256=329900a6673b237b502bdcf77bc334da34bc91355c5fd2d457fc00f53fd71ef1
# Wed, 10 Nov 2021 20:38:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Nov 2021 20:38:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b07c368b7a04669b63c6c86a881be270ee967474a85892003b8695df3d0d5874`  
		Size: 2.2 GB (2203104946 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:68d5dfbca608972a02b334e8d053010ece888346d5ebabfc28c9f91ed2063b15`  
		Last Modified: Wed, 10 Nov 2021 02:10:39 GMT  
		Size: 1.4 KB (1446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f998978d6856e995f1d9c4942941c32a17a4d88aff023bd7b9c78fc2a16c252e`  
		Last Modified: Wed, 10 Nov 2021 21:07:51 GMT  
		Size: 355.7 KB (355709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df00af83d6954d78318f0a3c49e11489b3f9f75536b0ccaf8b79ef99bd8c942`  
		Last Modified: Wed, 10 Nov 2021 21:19:41 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d210d894f69ec555473ee1b2660931eca8c5fe77ea2c3d54f43d02b3ff5e3c6`  
		Last Modified: Wed, 10 Nov 2021 21:19:42 GMT  
		Size: 347.6 KB (347634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90385fd7fd318a766486661e12da9640b595a1f49aa68073cb2453a12996cd33`  
		Last Modified: Wed, 10 Nov 2021 21:19:39 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bfdff653331ba67daa884b65414bb36a70e85652d9e78e5c65f71c8c06f916e`  
		Last Modified: Wed, 10 Nov 2021 21:19:39 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6cdc7754a5ecbb7db1c7c05e02f93e29487a790f740ff3d0ae50f9839f7ff5`  
		Last Modified: Wed, 10 Nov 2021 21:19:39 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1eeba6d01a4e2fcbdb5f12c3bb4a46c742e193f681e6832d0c19b38fc6ea1ee7`  
		Last Modified: Wed, 10 Nov 2021 21:22:59 GMT  
		Size: 182.5 MB (182455966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d82449c2e2a22f7dfa116f1e115648b7d2328a45b37347c1991f6c83eaff626`  
		Last Modified: Wed, 10 Nov 2021 21:19:39 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
