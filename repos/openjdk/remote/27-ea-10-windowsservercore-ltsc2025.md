## `openjdk:27-ea-10-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:416f0322c9aadd7692a5da4f5756e9db25d903d2e7e81b55be9b8866e26aeef3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:27-ea-10-windowsservercore-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:6a6abfadfd4389d19bcc7f0e90bb946c0b3b0ff88ee10e26e341d6a0bb5a5a9b
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190344306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f9e12410c5095c7c9f16421dbf1e75f952dea803fc307167e255909847a1573`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Sat, 21 Feb 2026 01:29:28 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Feb 2026 01:30:30 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:30:31 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 21 Feb 2026 01:30:37 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:30:38 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:30:38 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_windows-x64_bin.zip
# Sat, 21 Feb 2026 01:30:40 GMT
ENV JAVA_SHA256=243b7c1e79f8514af5765815d8b878c7362cacf8a9c4312c5c9c9e7a1eeee3e9
# Sat, 21 Feb 2026 01:31:05 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:31:05 GMT
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
	-	`sha256:ed279eb0342bef67902cea078249b3d8f293221bbabe9fd782807ef367d2f9ce`  
		Last Modified: Sat, 21 Feb 2026 01:31:12 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16ab2e4d9c8b47716dbdfb7620c2b1d3650b8682266886cfbf2c6e2c95d9b264`  
		Last Modified: Sat, 21 Feb 2026 01:31:13 GMT  
		Size: 371.4 KB (371435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b51ac31a6f483f4d42b35504bea2c102969677853332f3ab6f8fc1fec51ca9cd`  
		Last Modified: Sat, 21 Feb 2026 01:31:12 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c9017fa80ba8ffb37007b40cbb36be76e39204c35d6f9b1330a800bf6a370d7`  
		Last Modified: Sat, 21 Feb 2026 01:31:13 GMT  
		Size: 354.4 KB (354358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09eb8f1107344fcd54e30c4296415a0e84287490d895c2f97337799f5a986856`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7bc8d211a9b01c1bf008a396006e3d5a7b8af6bf596b9776589f177ad2c2b04`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8762a6e4fd07791a5f5d92e4f66238558e86b787a98de110287a285a5d72003`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1e29faceb09e635a69e197f1c2569e5018fbe0e462079f0c3b1df43a968254`  
		Last Modified: Sat, 21 Feb 2026 01:31:26 GMT  
		Size: 224.9 MB (224850811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e3906a273f1ac9add148f64b77396e404c3cfdc5017bb684362c69fc8e0343b`  
		Last Modified: Sat, 21 Feb 2026 01:31:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
