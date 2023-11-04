## `openjdk:22-ea-22-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:173095f9081a437c5582224bfbc3043da2bba1fa357c3982c470b36a622a98c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `openjdk:22-ea-22-windowsservercore-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull openjdk@sha256:b17e5840720bfbb9fbec94e1a70b6e943505f02ca52a4e4835d615d84f1256de
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2060392094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81b3f90a9e58914a8525c424eeb2e70d1a36346120619475dbf4a30cb593af3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 06 Oct 2023 21:59:31 GMT
RUN Install update 10.0.20348.2031
# Wed, 11 Oct 2023 01:35:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Oct 2023 03:48:56 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 11 Oct 2023 03:48:57 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 11 Oct 2023 03:49:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 04 Nov 2023 00:19:58 GMT
ENV JAVA_VERSION=22-ea+22
# Sat, 04 Nov 2023 00:19:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk22/22/GPL/openjdk-22-ea+22_windows-x64_bin.zip
# Sat, 04 Nov 2023 00:19:59 GMT
ENV JAVA_SHA256=0372b2b4ac120b8b7b3cdf4a890449348d97633a699d14ea769a9a31de6de19d
# Sat, 04 Nov 2023 00:20:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 04 Nov 2023 00:20:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d2471a50c8ec3ea61c16dd871f7b9167bf779faad2b6e5a6f72a18b88b846b`  
		Last Modified: Tue, 10 Oct 2023 17:55:23 GMT  
		Size: 471.2 MB (471244358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a73b90f34f44bbbb354af4f3d4cc6cde597d2f5183641e139f7ca8b76ec3bb9`  
		Last Modified: Wed, 11 Oct 2023 02:45:06 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71221770428be33fb112dc7596eb2857d0a894b9444c8ac1e070fb2713cf0cef`  
		Last Modified: Wed, 11 Oct 2023 03:55:46 GMT  
		Size: 438.1 KB (438050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7edf8e3cbf42462ac6609acad01b5456938cdcc07b096dfebda103810e262f`  
		Last Modified: Wed, 11 Oct 2023 03:55:45 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:935ab285e7bf5c8a65c15bf37e24c811dc80f14c18753ee554d67b2924e05265`  
		Last Modified: Wed, 11 Oct 2023 03:55:45 GMT  
		Size: 251.8 KB (251804 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0c2fc39cb13e3a7969857324cecf7f98cd507cce35ac2fb243990873ae47e80`  
		Last Modified: Sat, 04 Nov 2023 00:24:26 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b5152376e179cb4f6b0d6fbdec51068ab70bea0abe909bb1e063b1383311f32`  
		Last Modified: Sat, 04 Nov 2023 00:24:25 GMT  
		Size: 1.4 KB (1429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66742267690e53fac706f52331f7c962126d814667823ceaed9aa7eced16b478`  
		Last Modified: Sat, 04 Nov 2023 00:24:25 GMT  
		Size: 1.4 KB (1383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6ff467865797690499ee29919899159835737e790682b7e7348251632abcebe`  
		Last Modified: Sat, 04 Nov 2023 00:24:43 GMT  
		Size: 199.9 MB (199850708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee188eb9ecbba10df9aa5b2ca7cec36f73944e5c44facf5e77addacdcb370cc8`  
		Last Modified: Sat, 04 Nov 2023 00:24:25 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
