## `openjdk:26-rc-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:e4da2b3228560f4a522a05a352b1ab3ac8f3ca9301c8ecf00ab91df2a469d2a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:26-rc-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:e31e725c37f936570caa93525a854accfd7fca3209f2458ea841adc95c02f3f0
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2189708885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf09abd360d048bbfa163639731a8f7992875b401bafab9058f920d85b171f6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Fri, 13 Feb 2026 00:03:36 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Feb 2026 00:03:45 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:03:46 GMT
ENV JAVA_HOME=C:\openjdk-26
# Fri, 13 Feb 2026 00:03:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:03:51 GMT
ENV JAVA_VERSION=26
# Fri, 13 Feb 2026 00:03:52 GMT
ENV JAVA_URL=https://download.java.net/java/GA/jdk26/c3cc523845074aa0af4f5e1e1ed4151d/34/GPL/openjdk-26_windows-x64_bin.zip
# Fri, 13 Feb 2026 00:03:52 GMT
ENV JAVA_SHA256=a2dc3240208c735fe8107f27641987dd1283ad7e896d9aabaccb363fd93673ff
# Fri, 13 Feb 2026 00:04:15 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:04:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:456534216d0c12d9314cda831989d54bb3f542d7d43d9772ba40654db6dbd7bc`  
		Last Modified: Tue, 10 Feb 2026 18:52:01 GMT  
		Size: 441.7 MB (441700471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9e16882a096bd04f1b76ebe3892c4133fd6ac533398acfc77b9580a2617736`  
		Last Modified: Fri, 13 Feb 2026 00:04:22 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:742ae242336bf2eb7207c7586c6cd5ca89f17d93d6c0134cdac671bb96c29969`  
		Last Modified: Fri, 13 Feb 2026 00:04:22 GMT  
		Size: 360.7 KB (360704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a82efae44806e0faf05587690e6aaededdf47a5651d1d37a72e6ed0c12b2fc`  
		Last Modified: Fri, 13 Feb 2026 00:04:21 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6bf9ded93200edd9a0206a40e84be235a311a3c5486db8fd5e9b2c711835658`  
		Last Modified: Fri, 13 Feb 2026 00:04:22 GMT  
		Size: 338.5 KB (338455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dec797ed1306f644f608bee6816424a61849b609a9f99e0ca1aa44547640f8`  
		Last Modified: Fri, 13 Feb 2026 00:04:20 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4cbcc511054c97a0432e2dc66e76a9128ff28ad0d20692e2385c9eb3069ec51a`  
		Last Modified: Fri, 13 Feb 2026 00:04:20 GMT  
		Size: 1.3 KB (1341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44e2104bf2179fb8fc30df8605509d57eb30d45bb0c9e080378e3a1e0bcaa5ba`  
		Last Modified: Fri, 13 Feb 2026 00:04:20 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b82c677c7cee5355bd98d5196a38918e01078db4e37c793c9eaaae46e587e1`  
		Last Modified: Fri, 13 Feb 2026 00:04:35 GMT  
		Size: 224.2 MB (224241928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89b8338da1b00e356391634eba10ce78a33ed6034dd9c25a657b1e48c151a0c`  
		Last Modified: Fri, 13 Feb 2026 00:04:20 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
