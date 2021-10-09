## `openjdk:18-ea-18-windowsservercore-1809`

```console
$ docker pull openjdk@sha256:ee946a6af9533bfe613aadc1ca212590afce166fecc92705e83c30e23adbb4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2183; amd64

### `openjdk:18-ea-18-windowsservercore-1809` - windows version 10.0.17763.2183; amd64

```console
$ docker pull openjdk@sha256:9caa0ae4db53d98fc5ac9262d57ede028afabc7289cb8433213c0f67752c527b
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2870762545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a7c9a7528def28f0f33ca21937aa0ada17a8bff1488cc3faddf8b380fbc83f8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Mon, 13 Sep 2021 04:08:33 GMT
RUN Install update 1809-amd64
# Wed, 15 Sep 2021 00:29:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Sep 2021 00:31:34 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 15 Sep 2021 00:31:35 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 15 Sep 2021 00:32:58 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 09 Oct 2021 00:15:10 GMT
ENV JAVA_VERSION=18-ea+18
# Sat, 09 Oct 2021 00:15:11 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk18/18/GPL/openjdk-18-ea+18_windows-x64_bin.zip
# Sat, 09 Oct 2021 00:15:12 GMT
ENV JAVA_SHA256=bec524192218eb853263397524b61cb644624cd1694194e1c3d0817d29970537
# Sat, 09 Oct 2021 00:16:47 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 09 Oct 2021 00:16:49 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a0ddf88812f10c7d6edc858aa9784ff5ca9de4a7bb631909c090090343abd059`  
		Size: 968.4 MB (968365008 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92dd43eae724dbe7e9e517c7fded74c5920ae7eb160042055178ceadf1916505`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d714779fd458636d1b2289ae98777c0c8707a28708bffccab0b1314b59d77c`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 356.1 KB (356133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff34aee5a2ca310095a4e04d975fc389917040f43df1b7ab33cefa990b2f5794`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e2a30bd406da0ac5e18d582ad2ebdb0eb00497ff4ace8dc69f07433cb6d5728`  
		Last Modified: Wed, 15 Sep 2021 01:09:40 GMT  
		Size: 315.8 KB (315799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbbfa95e7e0d364f1d9dd36a263e7e7ca2614d8d7885ff55a2d76469f1d14e3`  
		Last Modified: Sat, 09 Oct 2021 00:24:13 GMT  
		Size: 1.4 KB (1414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20b25c491d24c0a989996636c387cf10a2f8b73a1330ed4490bef6aacd4ae1a5`  
		Last Modified: Sat, 09 Oct 2021 00:24:13 GMT  
		Size: 1.4 KB (1434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c67cec4741c182ea838953e2f32b3d375e3d9f2288955113a45e814c293071cf`  
		Last Modified: Sat, 09 Oct 2021 00:24:13 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3762284f98f2fe140e1bf467efb2817c41361d4a9d341a5df7a5f1a0377fa378`  
		Last Modified: Sat, 09 Oct 2021 00:24:34 GMT  
		Size: 183.4 MB (183384204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e17b42042487765a4c69205f61f954415cbea7db2aa58797d7c56369a4b1df6`  
		Last Modified: Sat, 09 Oct 2021 00:24:12 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
