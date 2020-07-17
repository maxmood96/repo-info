## `openjdk:15-windowsservercore`

```console
$ docker pull openjdk@sha256:b403026683e58d436b708e87e97171daa598371f2d33696069634f5b71295494
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1339; amd64

### `openjdk:15-windowsservercore` - windows version 10.0.17763.1339; amd64

```console
$ docker pull openjdk@sha256:eb07e262086c8bc620b0128cba38915186cd5a81feac74cb7f2277ebc4f1b9a9
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2515695824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edbc8450f3ad0992e8531d40668f4fe0f9d561c23808fecd7264bb56a78d0e5b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Wed, 08 Jul 2020 04:26:49 GMT
RUN Install update 1809-amd64
# Tue, 14 Jul 2020 18:41:51 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Jul 2020 01:45:44 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force
# Wed, 15 Jul 2020 01:56:24 GMT
ENV JAVA_HOME=C:\openjdk-15
# Wed, 15 Jul 2020 01:56:52 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath
# Thu, 16 Jul 2020 23:01:24 GMT
ENV JAVA_VERSION=15-ea+32
# Thu, 16 Jul 2020 23:01:24 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk15/32/GPL/openjdk-15-ea+32_windows-x64_bin.zip
# Thu, 16 Jul 2020 23:01:25 GMT
ENV JAVA_SHA256=b6234e651de32b418b6f1b7119761e5b576a2474b937e764ed543b0c73ddb521
# Thu, 16 Jul 2020 23:03:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 16 Jul 2020 23:03:24 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fc1b9e59edad2bf789457b52138acc367e86072b73bf862eaf96be70f4d4edbb`  
		Size: 591.9 MB (591859374 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:25edfecb5915de420000d722dc47ef9b13bc344a8330c4300e36a4ec8ca73033`  
		Last Modified: Tue, 14 Jul 2020 19:42:57 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca5cb7caf11332b67bae426682385af17fa897c718adce9713b111340eb0d71`  
		Last Modified: Wed, 15 Jul 2020 02:42:28 GMT  
		Size: 9.1 MB (9136637 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d284b2483b2f168e3ba6ac5972ceaa54db6f335b7cea2a7ba976ec79bceab7`  
		Last Modified: Wed, 15 Jul 2020 02:44:41 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9df741ee75c4cf331249ca7555639e3d621263ed2b077eabfcb7e526e62959`  
		Last Modified: Wed, 15 Jul 2020 02:44:41 GMT  
		Size: 293.0 KB (293037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854f156fe948208d22698346e4948c07faf3849242090cc8bad8f1aa70213339`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:265def16c6816003c143432b9310634f9d184fb134a50ef8954390627a76b42e`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b0c42b6c22bda3949c8bb8c3446f180aaf3da1048eb4e85d4b6add5753d082`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531c6f15fe07017e96d7753878366436e7b4bc55550daff431cdaa985f00d5f6`  
		Last Modified: Fri, 17 Jul 2020 00:21:04 GMT  
		Size: 196.1 MB (196067208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:024e886f87bb5417e3b02dc021eead5da9630e3312c10a9c87265edfba56eb90`  
		Last Modified: Fri, 17 Jul 2020 00:20:44 GMT  
		Size: 1.1 KB (1111 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
