## `openjdk:27-ea-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:5e04a88b003dd23dea51ec60e4f3c16867351905987a95159932b95cad97184a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:27-ea-windowsservercore-ltsc2025` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:cefa3b8242063977563069618e7bd34497162c6dd8a586d8b487b7f69d8d3569
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2307160733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7a8ff1222056372cd637ce5b7b868c26eb0a2b521b32444edf6612dc0dc5dcc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 13 Apr 2026 23:51:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 00:07:11 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 00:07:11 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 00:07:19 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 00:07:19 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 00:07:21 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_windows-x64_bin.zip
# Tue, 14 Apr 2026 00:07:21 GMT
ENV JAVA_SHA256=3cc253c247f136b430f6f42ac667120512f18fff012cfbf20817c6425edf15c7
# Tue, 14 Apr 2026 00:07:45 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 00:07:45 GMT
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
	-	`sha256:077fdf2334dca0a37a41a024f576999fa4fd25a235de0d94de95313f70dadb5c`  
		Last Modified: Mon, 13 Apr 2026 23:55:08 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a23f64831ced056c2c5b40fe9b7836c7d41fc67828c6f034b9c4a9e05549dc`  
		Last Modified: Tue, 14 Apr 2026 00:07:52 GMT  
		Size: 391.7 KB (391692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04bbb915ab2b4d598c6a7532e71a4263a62c0f382fbf984ad46ac11894bf7bd`  
		Last Modified: Tue, 14 Apr 2026 00:07:52 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:171040597c3d9053b081e0c46ba3fcb290c8df8bb17d901a5a2969ef8ab25363`  
		Last Modified: Tue, 14 Apr 2026 00:07:52 GMT  
		Size: 365.0 KB (365048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4793b6ebc23da9276a3a41fd613998427ed6d23e7ffc4a546c4a5cd84316e85`  
		Last Modified: Tue, 14 Apr 2026 00:07:50 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd064b1d7662b20a2a7336dc9699fd6cb848ce1f77c3e5e584df3ca2b3adf8e0`  
		Last Modified: Tue, 14 Apr 2026 00:07:51 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c5670e8f6093811b7e1446e59272ca64cd0f1ed32612fbcf3d2aec8b94e4f03`  
		Last Modified: Tue, 14 Apr 2026 00:07:51 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c54bf34f6f6a4ed7a9c2ad1b6b955bb2a30766afc349a2654c96d4ef1d2766`  
		Last Modified: Tue, 14 Apr 2026 00:08:06 GMT  
		Size: 225.2 MB (225200101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d16c0cf2ca3cd08cff16b83b613ea5544f0883665afcf2208cb7329c3dbe6d4b`  
		Last Modified: Tue, 14 Apr 2026 00:07:51 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
