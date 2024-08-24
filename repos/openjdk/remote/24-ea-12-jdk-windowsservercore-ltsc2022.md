## `openjdk:24-ea-12-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9090012ae54cc7e549725f3b145240344ea88ac52e88bb84b36b5f4589a243e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2655; amd64

### `openjdk:24-ea-12-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2655; amd64

```console
$ docker pull openjdk@sha256:f5482b80a5abb724c18d79488d997729436306d98633b8c368604e097c138dd4
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2350499528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bfd83af8bea3ba4ae160e3735e2f46ee1e14ab48e3bd6782c4bc260a2448859`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Sat, 10 Aug 2024 19:49:59 GMT
RUN Install update 10.0.20348.2655
# Fri, 23 Aug 2024 21:17:55 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 23 Aug 2024 21:18:07 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 23 Aug 2024 21:18:08 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 23 Aug 2024 21:18:13 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 23 Aug 2024 21:18:14 GMT
ENV JAVA_VERSION=24-ea+12
# Fri, 23 Aug 2024 21:18:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/12/GPL/openjdk-24-ea+12_windows-x64_bin.zip
# Fri, 23 Aug 2024 21:18:15 GMT
ENV JAVA_SHA256=4e795033e522ad8a7dcff604368b71de74b1481f8d8878b4cda5a7996fec6352
# Fri, 23 Aug 2024 21:18:34 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 23 Aug 2024 21:18:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd649075383e8df03ea713dfe59e1205716fbaa14450c10ef0d0a24a7b63669`  
		Last Modified: Tue, 13 Aug 2024 17:49:18 GMT  
		Size: 753.2 MB (753166182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b951e8b26661a958d61f5754f91f036f0c65a7fb9667f9e14ed4296c2ec39c`  
		Last Modified: Fri, 23 Aug 2024 21:18:41 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7febc61d946ae0018d08d1c5211f47c0b8a3fbc81f94940d5b1e09bc0164b74`  
		Last Modified: Fri, 23 Aug 2024 21:18:41 GMT  
		Size: 372.1 KB (372097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78b3ca3d4a651775973bd92b2a221db36b23c076d445dfab3d665aa03fd17b20`  
		Last Modified: Fri, 23 Aug 2024 21:18:41 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edd5777dbdfb236cab26261af6d550c8f53c7202d99b06adc2ff5e44d05feaa3`  
		Last Modified: Fri, 23 Aug 2024 21:18:41 GMT  
		Size: 351.9 KB (351931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e436dddb83f988a91fdd1f19d391d0894db232c49c5497ccd4c4e519b17563e8`  
		Last Modified: Fri, 23 Aug 2024 21:18:39 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c44ed4ddb3d6b96ab143fc2fdc2db8420f60e92786a1d8b3dddfd80cc1ec096`  
		Last Modified: Fri, 23 Aug 2024 21:18:39 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3540558e51add98cab9db688c6233d4d8dbfb0de65670c50eaccd56664e1306f`  
		Last Modified: Fri, 23 Aug 2024 21:18:39 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3562d02dc1e17c9238660efbdcd5850d5248929dcf8fe4be64f658725d32d03`  
		Last Modified: Fri, 23 Aug 2024 21:18:50 GMT  
		Size: 208.0 MB (208002745 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb40024dedd2784f07ca8e68dac9f7fb3f6f20cb827f7553ec57453523fad738`  
		Last Modified: Fri, 23 Aug 2024 21:18:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
