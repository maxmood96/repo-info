## `openjdk:23-ea-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:d0dd96f673f7aff6dbfec7f0716fb87072621edd7f41aa0852b409887f6ba942
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5820; amd64

### `openjdk:23-ea-windowsservercore-1809` - windows version 10.0.17763.5820; amd64

```console
$ docker pull openjdk@sha256:8c017c3c315f8f49a0770b635665436cd92b43f8a3b2fed14597b6d894c0dcd2
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2386231171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ff3bb9323d518cbe97d2defa9f63e9b8db187a4ba1eeb8827006cc2df3a53c7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 10 May 2024 20:46:44 GMT
RUN Install update 10.0.17763.5820
# Wed, 29 May 2024 23:01:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 29 May 2024 23:03:29 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 29 May 2024 23:03:30 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 29 May 2024 23:03:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 29 May 2024 23:03:53 GMT
ENV JAVA_VERSION=23-ea+24
# Wed, 29 May 2024 23:03:54 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/24/GPL/openjdk-23-ea+24_windows-x64_bin.zip
# Wed, 29 May 2024 23:03:54 GMT
ENV JAVA_SHA256=d1ca7c4de58322ccecc8598cbfb62a4585ee958e91b66562923df1eac562e816
# Wed, 29 May 2024 23:05:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 29 May 2024 23:05:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00cc2568ad51f25eabe6bb19ba6248a040d7622594b0d09ee77dec571d7280a`  
		Last Modified: Tue, 14 May 2024 17:25:26 GMT  
		Size: 529.1 MB (529091082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5054fe443dd3d07a548040c8a936861e37c50ec15a285912c2f859e622324c8`  
		Last Modified: Wed, 29 May 2024 23:05:10 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd88b3df751d2bc8f677623be1569e69ca1e5fdf6f70b37ba191df06df8cb2f4`  
		Last Modified: Wed, 29 May 2024 23:05:10 GMT  
		Size: 489.4 KB (489374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941c23c8b9bb6d0fa1971e653d6ec619aaf47a12ec661d093bd34cd93eda439`  
		Last Modified: Wed, 29 May 2024 23:05:10 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493b92853aca2c3b8702bd99e184b9f9f686fcd32309a1c5c7bf0e5518e0e1db`  
		Last Modified: Wed, 29 May 2024 23:05:10 GMT  
		Size: 335.7 KB (335689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba85c46430c849931942a491f878a62c1553e82e790ff33a80dcb547484ade6`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33158b06fb7bc592ae809893b51d4e62836573cf160ca823152e738bec31f541`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56941aa5d5ae0647bbc208b6396c39acfeebfa87d0c5f4b219c3256350e3395c`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12dfc63756da491c442fa515f8b09b67c5aa63987d89c8191c54d3aea18fe8f8`  
		Last Modified: Wed, 29 May 2024 23:05:20 GMT  
		Size: 205.7 MB (205686869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56d204ff39182c0c246df972b2030a92cbd8c6195a5a3ec5fdab379837b3f556`  
		Last Modified: Wed, 29 May 2024 23:05:09 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
