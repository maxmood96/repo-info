## `openjdk:24-ea-32-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:866c79feabdd36e82144df0b87d1fa90332a5ab2aa77f2c1f426374317e4e4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6775; amd64

### `openjdk:24-ea-32-jdk-windowsservercore-1809` - windows version 10.0.17763.6775; amd64

```console
$ docker pull openjdk@sha256:32d7cb48e87a6210b8db34fe05e98f03daca56ab21686a4f70c10f399d2631b8
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2331753827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc462c140d4dc9449837b2e88ec28e12e3a30612b8c8476377877233f121bd7a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Thu, 23 Jan 2025 22:26:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 23 Jan 2025 22:28:08 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:09 GMT
ENV JAVA_HOME=C:\openjdk-24
# Thu, 23 Jan 2025 22:28:18 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:28:19 GMT
ENV JAVA_VERSION=24-ea+32
# Thu, 23 Jan 2025 22:28:19 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/32/GPL/openjdk-24-ea+32_windows-x64_bin.zip
# Thu, 23 Jan 2025 22:28:20 GMT
ENV JAVA_SHA256=e5f13b2b408e1c98310b5fac3025ff52a576a8ca77ad40ec8a1e90d8d1ca3094
# Thu, 23 Jan 2025 22:28:58 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 23 Jan 2025 22:29:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb6c7809faf79f45e23fc488e33706477f780769406b3106d23357077f067f`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4b929e4dab1a122d348aa4f3c4d0092f4fd70243ea211b281e586e5c58346c`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 340.8 KB (340761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624b02ecaf0494301ef1e9530dea35e7e09dda72b87ec20a0bc1983cc01cafe2`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c897560bc646820cbfc297b6c8efc67dd75c87058c5c3468e94b178883119a8`  
		Last Modified: Thu, 23 Jan 2025 22:29:07 GMT  
		Size: 331.2 KB (331164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:736e8d53eeac021cec00f2b244dc11c89db3b3865311c8419e3d2ccff818d8c2`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:129807b7a42cd8ace2168a47bc666b1aaa922fab8694c4ea3c45f9950866722f`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2a3f350f71ecbaec116a8832c004d363e376befcb8cd46ddee0bda5be1d9558`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.4 KB (1370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f12864af61bff541919258a0f8bfdeb5fbba115ab25384828535d9fb3d2a871`  
		Last Modified: Thu, 23 Jan 2025 22:29:16 GMT  
		Size: 208.9 MB (208861857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02772b89adebe158575d790638b54d65fbf6db4ad463e69a9feb24fc469c3a22`  
		Last Modified: Thu, 23 Jan 2025 22:29:05 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
