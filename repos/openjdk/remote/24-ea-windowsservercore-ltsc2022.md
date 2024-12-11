## `openjdk:24-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:d5a16cce19ea8fa4c82e2b7a2f7aa1d28a4d21cebf68a2d68c62db6e244e7666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2966; amd64

### `openjdk:24-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.2966; amd64

```console
$ docker pull openjdk@sha256:609d675179052acbc474a4bf7d4058ca97bdd170f441da43dc4f2974fd0d4bf4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2463366905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539db919545665edc951b64b63cd67ad76a8c5e0c4b7379ded4f34de105362ce`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 05 Dec 2024 01:36:58 GMT
RUN Install update 10.0.20348.2966
# Wed, 11 Dec 2024 20:41:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2024 20:41:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:41:55 GMT
ENV JAVA_HOME=C:\openjdk-24
# Wed, 11 Dec 2024 20:42:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:01 GMT
ENV JAVA_VERSION=24-ea+27
# Wed, 11 Dec 2024 20:42:02 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/27/GPL/openjdk-24-ea+27_windows-x64_bin.zip
# Wed, 11 Dec 2024 20:42:02 GMT
ENV JAVA_SHA256=d3c4c15520262f2d3de174d973e37053081a8b627a66e8f4939419b4af8b4823
# Wed, 11 Dec 2024 20:42:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2024 20:42:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90641eccc9d7a78ab99d123ca3884acb8ffc002eb44bc5e68f261f0810d5202b`  
		Last Modified: Tue, 10 Dec 2024 18:41:03 GMT  
		Size: 791.7 MB (791681213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85d74e940fc5c564d16836ce79ac9032f9de9b429e607886f8a884fa65282a21`  
		Last Modified: Wed, 11 Dec 2024 20:42:25 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3087335ca7385e68c6c4288a0c0a8e61933e24deffc451ac5bf3a9602b4b1a9a`  
		Last Modified: Wed, 11 Dec 2024 20:42:25 GMT  
		Size: 346.6 KB (346633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f58b5db76e23a40bb6014b521a0b30ca1fc45be61fa67b7bea7baf4566f33104`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11653d8d8ddf22f9a59ccd1373fb768eea13e1ab4425aa780607453858117389`  
		Last Modified: Wed, 11 Dec 2024 20:42:25 GMT  
		Size: 334.2 KB (334225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a1a922bce3d8ed0f3eb41cdac053b27993568fa93822d8b818fab8cc99093f`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2851f4d0d423d7b95515938780361333d80075d0c515a4af02dc1ebc47d09f07`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ed62fc0ef63c50b67bbdf3d6aea957f6b08bd682c40ddc2c0529adb194a0bab`  
		Last Modified: Wed, 11 Dec 2024 20:42:23 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3988f1adfadc5e7ebe2adb8cccae758b2e034006a85f8d86df61907f0d38116c`  
		Last Modified: Wed, 11 Dec 2024 20:42:36 GMT  
		Size: 208.8 MB (208804703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2130ecc335238637eb1727bace20766a37671dff7b9124b09d54e324b3c4b2b`  
		Last Modified: Wed, 11 Dec 2024 20:42:24 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
