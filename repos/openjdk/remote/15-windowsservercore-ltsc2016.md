## `openjdk:15-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:afc4c46a84c83c3a06c2bb8353f09ae0cbf66e211c72deb7e494acad695934a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `openjdk:15-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull openjdk@sha256:4898fa2eabde7cca14da71413d49be1b3f1f3d64959e71090a72ebaadd9c7820
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (6011163087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43bf966399e441020c54985fc0c9c88cff7fbf115072d56a133432f3635fb25f`
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
# Wed, 13 Jan 2021 20:38:55 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 13 Jan 2021 20:40:07 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Wed, 13 Jan 2021 20:40:08 GMT
ENV JAVA_VERSION=15.0.1
# Wed, 13 Jan 2021 20:40:09 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk15.0.1/51f4f36ad4ef43e39d0dfdbaf6549e32/9/GPL/openjdk-15.0.1_windows-x64_bin.zip
# Wed, 13 Jan 2021 20:40:10 GMT
ENV JAVA_SHA256=0a27c733fc7ceaaae3856a9c03f5e2304af30a32de6b454b8762ec02447c5464
# Wed, 13 Jan 2021 20:42:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 13 Jan 2021 20:42:46 GMT
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
	-	`sha256:e4a58eca69f1a9d84cc34825fdc899bec22ec469ab355f7350fe25dda4e757c4`  
		Last Modified: Wed, 13 Jan 2021 21:24:38 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795fb185e8937ffdd64e807c36b6153091728068b456396ffcebfc6de84c9b7e`  
		Last Modified: Wed, 13 Jan 2021 21:24:39 GMT  
		Size: 5.6 MB (5595394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdb2bc01b9ca2d1c66c23e523092b3856934bd967f4c1d4f1cccee27d09309bd`  
		Last Modified: Wed, 13 Jan 2021 21:24:32 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ad700303c1e9782c0c20f05d1b4bc1db79a0f48ab2a422b0db568a8dafa9c2`  
		Last Modified: Wed, 13 Jan 2021 21:24:34 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973aec8f049467c221cca1a00c467803b09512bde7eb4fa1f9ffd5d4ab1f686e`  
		Last Modified: Wed, 13 Jan 2021 21:24:34 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d9fe2133fb8b9f91fedf79e3e72a23f15fc22070f4f2a752aaa1f896777e2ec`  
		Last Modified: Wed, 13 Jan 2021 21:24:57 GMT  
		Size: 201.5 MB (201516732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e09efbfa5e2bb0fa2d4a6f83e074c3379614b43064cb9a88569b45ef235f240f`  
		Last Modified: Wed, 13 Jan 2021 21:24:33 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
