## `openjdk:16-ea-27-windowsservercore-ltsc2016`

```console
$ docker pull openjdk@sha256:be604448edd792c780b86daf7abcc8adae37844dcc28d18f30b274aa070ac29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4046; amd64

### `openjdk:16-ea-27-windowsservercore-ltsc2016` - windows version 10.0.14393.4046; amd64

```console
$ docker pull openjdk@sha256:479b1dd1cc1aa874d940cbcbadd7dc95f85ec26b71fb4808bb477b0ee6548b0c
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 GB (5976225102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a6fbbb7acb7e0e0176515250c526ede974c9e092551ce6eb93a839b44b0b1f5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 28 Oct 2020 18:03:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Nov 2020 13:23:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Nov 2020 17:49:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 11 Nov 2020 17:49:02 GMT
ENV JAVA_HOME=C:\openjdk-16
# Wed, 11 Nov 2020 17:50:15 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 03 Dec 2020 22:16:12 GMT
ENV JAVA_VERSION=16-ea+27
# Thu, 03 Dec 2020 22:16:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk16/27/GPL/openjdk-16-ea+27_windows-x64_bin.zip
# Thu, 03 Dec 2020 22:16:13 GMT
ENV JAVA_SHA256=b2d10f066df03f1b3e5a6f4c319bda1169deb346ebe4b8a98852dbbf678e2f8b
# Thu, 03 Dec 2020 22:18:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 03 Dec 2020 22:18:30 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4830fb08bc2df7ae80548c349b880c263ea87a7b93e13ecbc77c862b6e179558`  
		Size: 1.7 GB (1700572904 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:126d9a92c0cb7b68c56dec2dd5ba118de9dde3ec6368db734c5135fdf1528a33`  
		Last Modified: Wed, 11 Nov 2020 13:34:53 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1222181efe25bb0d500f320707eb7dc24e576749c0897042ae1f3b8116e87990`  
		Last Modified: Wed, 11 Nov 2020 18:26:42 GMT  
		Size: 10.1 MB (10078764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:715e1a3de99f869c8010907852bce9306cb6693a16fc9fad69ea0bb744446cdc`  
		Last Modified: Wed, 11 Nov 2020 18:26:29 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd970ee1e99b8801c2230b471ed6d4dc79d30324c882f32ae8efb05d8be0d34d`  
		Last Modified: Wed, 11 Nov 2020 18:26:31 GMT  
		Size: 5.5 MB (5511761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b8ad45f08c6dbb9dca7c7a46ea829f542661f94cf3ad38bc2d892d36044a51a`  
		Last Modified: Thu, 03 Dec 2020 22:24:11 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6c73681b8da99033884f933c1fe07820ecde5a52deb1aebc9519c1862ecb4ff`  
		Last Modified: Thu, 03 Dec 2020 22:24:11 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61db9fd956c0a873fed0e9c9d7aba82d8f0d22c5537da77fb34e48696062b71f`  
		Last Modified: Thu, 03 Dec 2020 22:24:11 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f78c04329d7323c885564a48631f14bfac6f0983f8b1c503e26c0bfd38df315`  
		Last Modified: Thu, 03 Dec 2020 22:27:53 GMT  
		Size: 190.1 MB (190068883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71dc5c58f2a4ea4d153f5af5eae7c1b185e21c3965979e8034e7cdb60eafe391`  
		Last Modified: Thu, 03 Dec 2020 22:24:11 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
