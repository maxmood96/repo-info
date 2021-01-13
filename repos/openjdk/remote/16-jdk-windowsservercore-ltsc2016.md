## `openjdk:16-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:271bb72c98a79ed62b256002a98498da3ef7d7aa9219a5ed8bcd3d863d9f9165
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `openjdk:16-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull openjdk@sha256:021614d859d27a8794e6ef12a4e41c23ed203fc1c60110f84d6a76a4bad1791e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5999845440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c37fe56dab075f9aab269101e9bf47925999d13b791252a18582af59d81aec6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 19:52:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 13 Jan 2021 20:31:02 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 13 Jan 2021 20:32:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 13 Jan 2021 20:32:19 GMT
ENV JAVA_VERSION=16-ea+31
# Wed, 13 Jan 2021 20:32:20 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/31/GPL/openjdk-16-ea+31_windows-x64_bin.zip
# Wed, 13 Jan 2021 20:32:21 GMT
ENV JAVA_SHA256=a5211830844d29a686c10bdddc1c531cda144098c50afbd57cd6cae168c6f248
# Wed, 13 Jan 2021 20:34:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 13 Jan 2021 20:34:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a3afa197466836cbf2dcd19b07fdfb19c5f03ff2404cfa9d86d8fdfe6f2b29`  
		Last Modified: Wed, 13 Jan 2021 21:12:35 GMT  
		Size: 10.2 MB (10150234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59879d417b9b1b9a58535f0f28c7b5d9e9fa6c75796091c68fd147c561193725`  
		Last Modified: Wed, 13 Jan 2021 21:18:29 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27fc426a8537d53e5e7d765f77354bc432c30f9aa214f8eec295c27c72ce5870`  
		Last Modified: Wed, 13 Jan 2021 21:18:30 GMT  
		Size: 5.6 MB (5591005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a4160168bef4f6941735f0a5aee276d362994a2bafcbdeda4fd71ecd6e0a92`  
		Last Modified: Wed, 13 Jan 2021 21:18:26 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea1ccc399627524ef1c528e2a6ca3afba2256de1c028509545e9aed631eff878`  
		Last Modified: Wed, 13 Jan 2021 21:18:25 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1355245f9cfdb85f64813d46b958404fac04acb283faabebaecce88d0b100b4f`  
		Last Modified: Wed, 13 Jan 2021 21:18:26 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f1ec46cc3fa72d0a8c23ee72eb0bd2e225eefc47778035d0e08fa754d37ef1`  
		Last Modified: Wed, 13 Jan 2021 21:18:46 GMT  
		Size: 190.2 MB (190203301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956d32002662d2670af52ddc81290efa699b99c7184a7b0e3dab2f3b118532dc`  
		Last Modified: Wed, 13 Jan 2021 21:18:25 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
