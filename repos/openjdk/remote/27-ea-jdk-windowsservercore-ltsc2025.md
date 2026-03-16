## `openjdk:27-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:3a911bfa2ed81952312390d4d76a029a1e20bf7d31e0d168b4309951677b2d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:d88d6743e8d29dc0c94c8c11be2966e986d3a09c3f407721cb081db92a1da1b3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2306670912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3034e9f562fc8bc103dd78ef7ef991e355275294246e92581fc735cb0c93cf0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 16 Mar 2026 17:17:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 17:18:53 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 17:18:54 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 16 Mar 2026 17:19:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 17:19:02 GMT
ENV JAVA_VERSION=27-ea+13
# Mon, 16 Mar 2026 17:19:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/13/GPL/openjdk-27-ea+13_windows-x64_bin.zip
# Mon, 16 Mar 2026 17:19:04 GMT
ENV JAVA_SHA256=f5a1c2aa25b826ecdaf3c6614f16bc91e871d38839bf0e01e4e2531bbe590cd0
# Mon, 16 Mar 2026 17:19:32 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 17:19:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6de82b7e7c1f35dde6b4118fb6aebaa42afcb877810f3599bdcd1b4589aaebd`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150d874657d39efabf1e837a905c283aff78878f22caa45276f591804aa1d45b`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 372.8 KB (372821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41a1a86483f3927a61012f342a7f3a4c40bad7ce19dc61e2a084bfc87c1ee658`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee4aedf713ed51271319bc0e2e93c50a5a781212693c09f0e182daa3bcb849f`  
		Last Modified: Mon, 16 Mar 2026 17:19:39 GMT  
		Size: 354.9 KB (354871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5623a08f76051a810affcf3626bbdf7e262cf46b5409de42f9445d165443b4b7`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2bdbbe743d63a3bd0479c3a83f48b2d59b833f8cad494acd2d15e4156f4d499`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9215b3dbc1340d738bd4abec5684d230737b9170dd076e21d39cc637af70dc61`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c059aaeab605e916850f3b272fbbb514a1181ae0bbafc41c3c6a7bb4aa87182`  
		Last Modified: Mon, 16 Mar 2026 17:19:52 GMT  
		Size: 224.7 MB (224739402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cf9a17eb23461987ac05549c412d1c12d57af97f774e182c7020011c1dfa62d`  
		Last Modified: Mon, 16 Mar 2026 17:19:37 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
