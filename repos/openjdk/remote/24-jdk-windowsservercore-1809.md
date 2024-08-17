## `openjdk:24-jdk-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:bff8d02651700a455e29030016399033f734db11b45344ac0987dbbb06c02224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.6189; amd64

### `openjdk:24-jdk-windowsservercore-1809` - windows version 10.0.17763.6189; amd64

```console
$ docker pull openjdk@sha256:6b62abb3cfe281137ebff9a86a9235e84e3ee7763c424a4922672de2fcf44062
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2453974553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65de2250d32227b878fd7574a6a3c9ecd9b39ebef946a81ebc0eace90ab867d6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sun, 11 Aug 2024 07:11:31 GMT
RUN Install update 10.0.17763.6189
# Fri, 16 Aug 2024 22:02:15 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 16 Aug 2024 22:02:38 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:02:39 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 16 Aug 2024 22:02:56 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:02:57 GMT
ENV JAVA_VERSION=24-ea+11
# Fri, 16 Aug 2024 22:02:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/11/GPL/openjdk-24-ea+11_windows-x64_bin.zip
# Fri, 16 Aug 2024 22:02:58 GMT
ENV JAVA_SHA256=7a69063e699bfa886323d4d41aebe553be53c68819b952fb7342fd73cc735697
# Fri, 16 Aug 2024 22:03:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 16 Aug 2024 22:03:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:579bd4d5f7fd8737f66e40b29aafedee32d589107027d75796993c8898e3e7dd`  
		Last Modified: Tue, 13 Aug 2024 17:57:48 GMT  
		Size: 594.6 MB (594582880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9d25b119927bcfe5d32e85c7c17a6226207ca07b071d14beb6dc05db6850ba8`  
		Last Modified: Fri, 16 Aug 2024 22:03:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1266b3d9b99476f2dd66849d966507de5a78efea31bc1d7a39894608f037dc4`  
		Last Modified: Fri, 16 Aug 2024 22:03:39 GMT  
		Size: 488.7 KB (488749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfebf4a8c1c09851868e8172d616595590024210e407ca97ba45c12d5fdd235b`  
		Last Modified: Fri, 16 Aug 2024 22:03:38 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f967beb5c367d05757412c7c7b58a425a522df56e58f9d47080400dc7ad5c8af`  
		Last Modified: Fri, 16 Aug 2024 22:03:38 GMT  
		Size: 335.8 KB (335840 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71c9d4c72f740a9eb61107afa23b15d8885494cd7eab927e56b42b7c1bfb0da`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:162edac2a55bb4b6ba7587b17c17dfe214324f0ba53f9b0b8c1a32e14592a70c`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca708901375b06abb7391c6ba4e3b6e579b836482ea3dbf167aaedb182d6db8a`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c30263b3af1d6e9c4d62d0b8c26b8043d2ac248020bab4ac7e3e3616c5f229`  
		Last Modified: Fri, 16 Aug 2024 22:03:47 GMT  
		Size: 207.9 MB (207938921 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7a1ca3570c5dfc9e7efd943bc836f42761c244617ce344d1be0d7b2b06aa7b`  
		Last Modified: Fri, 16 Aug 2024 22:03:36 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
