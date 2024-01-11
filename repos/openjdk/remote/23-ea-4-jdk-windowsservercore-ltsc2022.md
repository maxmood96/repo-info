## `openjdk:23-ea-4-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9e2952ad6b4d78ca33f6367b82d0bcbb13eede19f30344cf099347c73f5919b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2227; amd64

### `openjdk:23-ea-4-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2227; amd64

```console
$ docker pull openjdk@sha256:6a2da0935a0daa0f903d1e41b762673d7fa4714e2707cd08141d260426a788bd
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2098839473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0278a0a7bdbc19e77bc27b448e0035bfdd7dc22bf05b0c67a161f586a74d461b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:55 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:02:55 GMT
ENV JAVA_HOME=C:\openjdk-23
# Thu, 11 Jan 2024 00:03:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:03:02 GMT
ENV JAVA_VERSION=23-ea+4
# Thu, 11 Jan 2024 00:03:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/4/GPL/openjdk-23-ea+4_windows-x64_bin.zip
# Thu, 11 Jan 2024 00:03:03 GMT
ENV JAVA_SHA256=14230e6d57a3b39a3b5e232e7095fe1821a48197f75b68ae0f09db29e5391216
# Thu, 11 Jan 2024 00:03:28 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:03:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7b270ef0cbd43cfe02dfe996548aeb3ed35598a8c6df5963c866774bc1ff7ca`  
		Last Modified: Thu, 11 Jan 2024 00:03:37 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74654d7815219105b4c690c1af48f749f70a8b7f0e0df00e445b267eb335ff18`  
		Last Modified: Thu, 11 Jan 2024 00:03:37 GMT  
		Size: 485.4 KB (485401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5eb2d0d69d8a8238779a9ff3cf36ebf9de189128df39e0d2238347c8a202b23`  
		Last Modified: Thu, 11 Jan 2024 00:03:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:911a4bfc42e6e002b164c7024a7ad691314fecd49c652ef74754a68792ad087e`  
		Last Modified: Thu, 11 Jan 2024 00:03:37 GMT  
		Size: 337.4 KB (337390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e5c612f2dec5c6e8ead1c65d3cddbc1de8edb9fae74e77327790763a94dc3b`  
		Last Modified: Thu, 11 Jan 2024 00:03:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430633b258fabc4e7ed626908b17a409a833ace669122a46263b74f9c40fa8dc`  
		Last Modified: Thu, 11 Jan 2024 00:03:35 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1768da87785943d0ce05854ac1674719c263728cf52089fdc93d9d2c90b92f5`  
		Last Modified: Thu, 11 Jan 2024 00:03:35 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bf9b07d1916777c40446d9d98821b74848d5de68fcc082dc5d4790617f8a60`  
		Last Modified: Thu, 11 Jan 2024 00:03:46 GMT  
		Size: 197.8 MB (197796260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2c8b77d0665a3a39b32dd5b07296d369e20c9f1f5f2a8e03eff1f56102c4893`  
		Last Modified: Thu, 11 Jan 2024 00:03:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
