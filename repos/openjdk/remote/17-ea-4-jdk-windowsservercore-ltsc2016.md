## `openjdk:17-ea-4-jdk-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:30a64e345aa493b8e63035b1ced03e9e597bbe88c41aeab79e8422c944c639b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `openjdk:17-ea-4-jdk-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull openjdk@sha256:73761f55107176b5fad10c0347b8a07b9f3a8c4bb6e1fe65e5aa2072724c4872
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6000959981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0821a2b36993804bcfbc213fbf24c64ef532c927f925c5cbf56688733a8c32c`
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
# Wed, 13 Jan 2021 19:52:42 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 13 Jan 2021 19:54:02 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 13 Jan 2021 19:54:03 GMT
ENV JAVA_VERSION=17-ea+4
# Wed, 13 Jan 2021 19:54:04 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk17/4/GPL/openjdk-17-ea+4_windows-x64_bin.zip
# Wed, 13 Jan 2021 19:54:05 GMT
ENV JAVA_SHA256=254b3209c8eadedb0c4db73232dc4707a92582e332fd63f3a14d4c0b9253562d
# Wed, 13 Jan 2021 19:56:37 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 13 Jan 2021 19:56:38 GMT
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
	-	`sha256:c01c27c5f704d1dfadcfd923e0c1590954781300b7f37cf4807d34319dfc8b26`  
		Last Modified: Wed, 13 Jan 2021 21:12:31 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df715839603d2056052edc0649acfa54345dc273c8bfaefc41fae0966a68fba0`  
		Last Modified: Wed, 13 Jan 2021 21:12:31 GMT  
		Size: 5.6 MB (5595399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3617b74911f53695f9398b35b5deae6ffc1e647efd8dcc06167f73260f71fe6`  
		Last Modified: Wed, 13 Jan 2021 21:12:29 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99bf0701c017e60bf5a85ba9f4987d14e349fa8139082c0af92b719f6c266b6`  
		Last Modified: Wed, 13 Jan 2021 21:12:27 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eea37bb2894387ac32debfbaa62de10d4046e70ea460a545623e686a8355749`  
		Last Modified: Wed, 13 Jan 2021 21:12:28 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b721d67ab9a705a2d6336312949d83d6af5540bdbf53cb6c31fab00faf42207`  
		Last Modified: Wed, 13 Jan 2021 21:16:15 GMT  
		Size: 191.3 MB (191313460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:393fc46c9e46efef9897bd1077b3e147da517b7a39cd8734b39d5265536ac58b`  
		Last Modified: Wed, 13 Jan 2021 21:12:26 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
