## `openjdk:27-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:63833f44867c622e460d68c179534a66000d6728c2046eef40c011aa9411e36c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.7462; amd64

### `openjdk:27-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.7462; amd64

```console
$ docker pull openjdk@sha256:75d7dd33e0c15af79bfbf29e16275c36872739212ee4cbf149002b35277c2fda
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3478256408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:480f763219ed032bb8b63c43bcda78eabe7566572e3a4af4062d05c327a8010f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Dec 2025 21:49:56 GMT
RUN Install update 10.0.26100.7462
# Wed, 24 Dec 2025 05:18:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 24 Dec 2025 05:19:09 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:19:10 GMT
ENV JAVA_HOME=C:\openjdk-27
# Wed, 24 Dec 2025 05:19:16 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:19:17 GMT
ENV JAVA_VERSION=27-ea+3
# Wed, 24 Dec 2025 05:19:18 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/3/GPL/openjdk-27-ea+3_windows-x64_bin.zip
# Wed, 24 Dec 2025 05:19:19 GMT
ENV JAVA_SHA256=b40619c93cd4c56c31387444551cdaf5d2fe61ff5e8a10cc43ac1159ad3a69a6
# Wed, 24 Dec 2025 05:19:43 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 24 Dec 2025 05:19:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890b21ccebaeedf053c6c32fb4fe8d98ab2c60496b12e6b730ac67df9096fc5b`  
		Last Modified: Tue, 09 Dec 2025 19:44:14 GMT  
		Size: 1.0 GB (1037813290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f3d525d0293f0c6ec260ea3e548281f51d5e75db31202d01297a9c362bf896e`  
		Last Modified: Wed, 24 Dec 2025 05:33:10 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d2de42b0e26bf29ce180659081408d6efafecac8fc74e3b769e0a25f14a7f6`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 405.6 KB (405604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc385c79ad1d5d394e02ebc84c382c2010ce9f9cfdd664bcde9d313af8ee498`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7024ce36b5bff6ea629ffdb5bcd235d5e707886d23e246780381c19897be80e`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 387.2 KB (387214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4a3424f1b1b2634a0636c20b97edec7c390cb1da7830dee058bc1cf9a212cdb`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0cb6d43787f5b5dda903158b020a94bac36626bf2de0b11a0fb4b52e8452412`  
		Last Modified: Wed, 24 Dec 2025 05:33:03 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c951029cf95fd470e2363e345977e723cc49c977ac95f4cd78ba2b859a8c813`  
		Last Modified: Wed, 24 Dec 2025 05:33:03 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14d52241fbd08444b22df3aa7c9326a8edf81076d67b17498a9e0c9d501681ad`  
		Last Modified: Wed, 24 Dec 2025 05:33:21 GMT  
		Size: 224.3 MB (224335349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a8710de7998d6dc3459bb43780761e3888b6638c78207e33acfefcf4252172b`  
		Last Modified: Wed, 24 Dec 2025 05:33:04 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
