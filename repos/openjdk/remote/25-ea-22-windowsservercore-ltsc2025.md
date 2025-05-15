## `openjdk:25-ea-22-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:dadcd5cafd8a90eaa4d7e675bbfac3cc589f44a90e8024dc9e11a7803c2bb3b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4061; amd64

### `openjdk:25-ea-22-windowsservercore-ltsc2025` - windows version 10.0.26100.4061; amd64

```console
$ docker pull openjdk@sha256:587472361bb2ee68c4558464a96341febda353305e3693114f9aab87382cf52a
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3640303761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:653fa3553cc2abfc30d29fb6d63e6e3f2224d60e6d1e624480665cbc868016b8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:01:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:01:25 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:01:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 21:01:32 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:01:33 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 21:01:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/22/GPL/openjdk-25-ea+22_windows-x64_bin.zip
# Wed, 14 May 2025 21:01:34 GMT
ENV JAVA_SHA256=8b16ab02467967b98cf7d8743da9c9688d3ff39b4a693b66b6d9fe84cc0bb55a
# Wed, 14 May 2025 21:01:51 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:01:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Thu, 15 May 2025 19:25:03 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7c1850a8784e02078a30e50c0167a4076b3d45752fecdc9f76592876425e8`  
		Last Modified: Wed, 14 May 2025 21:01:56 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5515d76afc4c4c2618b70aa4c1675559cd80d3f850f37d6be6e7d6f89048dc32`  
		Last Modified: Wed, 14 May 2025 21:01:56 GMT  
		Size: 388.4 KB (388376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9498da14c7242052534886933cb167ef1e6ee657c162a2a624530f32b4cd0c8`  
		Last Modified: Wed, 14 May 2025 21:01:56 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce73249f17f0b6fd01347526543f478f1a69dc29390dc4fbdc74d295519b3ecb`  
		Last Modified: Wed, 14 May 2025 21:01:56 GMT  
		Size: 371.0 KB (370958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9f8eed7a806dfe9a893b0e954c946ed0ba3c0dfc92fef989659e08a57fa91aa`  
		Last Modified: Wed, 14 May 2025 21:01:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e2efb6b6c34db4aab222e8ed7a82b4bb3b1f3465dfc10a5be15042c4b5c963`  
		Last Modified: Wed, 14 May 2025 21:01:55 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c5ef9e2fdb35cdeae7ad95ccdddf31b2896dd9d3cc30b4bdbbf118bbd9152f`  
		Last Modified: Wed, 14 May 2025 21:01:55 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f438fda6fe429610dd5f1aa58e0c609341cb08198bbc2c321e8ced13f75c53b`  
		Last Modified: Wed, 14 May 2025 21:02:07 GMT  
		Size: 208.8 MB (208770836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae940eea42ed87c5166ba3fe155cd8c815172a61e5717fb4e8dad39684392d95`  
		Last Modified: Wed, 14 May 2025 21:01:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
