## `openjdk:27-ea-jdk-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:86ce4b54b9233e5a3b1b2912690849715058d8ac8321ffe3edf8dd5b88d3492f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32995; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2025` - windows version 10.0.26100.32995; amd64

```console
$ docker pull openjdk@sha256:5b6bda0d60ac24d9c44e6ccbe965f0dd1ef7cda59914cd26e1c7f4aff4933476
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2503463228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a64e703c5b7f044586e4a81167f82d934b40061cf8a9b0bf03f52774b1a0382`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Sun, 07 Jun 2026 07:36:39 GMT
RUN Install update 10.0.26100.32995
# Fri, 26 Jun 2026 22:42:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jun 2026 22:43:26 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:27 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 26 Jun 2026 22:43:33 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:33 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 22:43:34 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_windows-x64_bin.zip
# Fri, 26 Jun 2026 22:43:34 GMT
ENV JAVA_SHA256=72394e06c335cb58cef351c47e54a05ebb0c03338f3d2f92fb941927445670aa
# Fri, 26 Jun 2026 22:44:00 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:44:01 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee71d57b2226db82d002abc39a97b7dd144f007db435566364a0285bf115b83`  
		Last Modified: Tue, 09 Jun 2026 18:08:12 GMT  
		Size: 756.1 MB (756083682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37b16c77d6773401beaabaf98aeff43f9a4d2cc20798f4795e4c2e198364ba69`  
		Last Modified: Fri, 26 Jun 2026 22:44:08 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6f083081f7de152c19555682a70489e6146de69d65be869372f11d837f09d5b`  
		Last Modified: Fri, 26 Jun 2026 22:44:08 GMT  
		Size: 397.3 KB (397311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a542cd4c3fc2f7c110cb6dad3b9f4cc3cdb6cafd5fee3384f60a516d3d6104`  
		Last Modified: Fri, 26 Jun 2026 22:44:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e60822a7858375e2b4fbc810a0e471fe4cb04ba7680d481c336b6151e3f96829`  
		Last Modified: Fri, 26 Jun 2026 22:44:08 GMT  
		Size: 385.9 KB (385949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10388e106e743193f38c0b6e29ec42daaca12b2b8bc91ea38474edd9b837660`  
		Last Modified: Fri, 26 Jun 2026 22:44:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0063b4b22a1108c8298ea114541dabcdb56d345b40b653a0d00abdb9cc1d179`  
		Last Modified: Fri, 26 Jun 2026 22:44:06 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb0c1a83cb180e79a28fd665616769e600d6871e00d81ed5439e9417fac71b6d`  
		Last Modified: Fri, 26 Jun 2026 22:44:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b5710604c6d93fc34e752a8c38b8b08296f795522f829f28d2446e95c9839a`  
		Last Modified: Fri, 26 Jun 2026 22:44:22 GMT  
		Size: 223.5 MB (223529189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cb4bfdb5b027256e2f4aac037d20e364d282e54ead7e5aebeac90a566d543e`  
		Last Modified: Fri, 26 Jun 2026 22:44:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
