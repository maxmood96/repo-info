## `openjdk:27-ea-jdk-windowsservercore`

```console
$ docker pull openjdk@sha256:d091e987918092e7427e61b3c9be20b2869eff2071dc85f484e5d540275ad19b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:e5c44201a06cfa1180a0d6c26950ac428e17682a23c5c0aaad6e2794e0a4f92e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2190102031 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e0ca682e3a125e8db4bc70ba5a35a2b018232009f2670b4771ea0553e90315e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Feb 2026 22:21:49 GMT
RUN Install update 10.0.26100.32370
# Fri, 13 Feb 2026 00:06:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Feb 2026 00:06:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:06:55 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 13 Feb 2026 00:07:00 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:07:00 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:07:01 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_windows-x64_bin.zip
# Fri, 13 Feb 2026 00:07:01 GMT
ENV JAVA_SHA256=d3ecddd6cae9d89198ec453bda26dd10c1e83e3bfcac8040a493acad08a14c6f
# Fri, 13 Feb 2026 00:07:22 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:07:22 GMT
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
	-	`sha256:bed9629fae65d97b1386cda5cbb1e0567ed29ab07757815d5ee878b696356554`  
		Last Modified: Fri, 13 Feb 2026 00:07:28 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1aaa3813929be6fb7b39fa78177d396d1e7243216cc85ee659f1cdf985a82b19`  
		Last Modified: Fri, 13 Feb 2026 00:07:28 GMT  
		Size: 342.3 KB (342271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d593e40b9ed94145c6663124561e6d77dcc0d9911056d9d05ee12aa46e347`  
		Last Modified: Fri, 13 Feb 2026 00:07:28 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7546944fa1e6a10627120217dbe83d5e5ceab50a183a2fd09b035df860a13e`  
		Last Modified: Fri, 13 Feb 2026 00:07:28 GMT  
		Size: 330.4 KB (330396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8dfb8784961f382294b530a00d49b3fce6bd5a7b2d1346c41f929ed15e64853`  
		Last Modified: Fri, 13 Feb 2026 00:07:26 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:594645165a695a722db76f06e790fd7534a1ab8e830d4f46eb587f872e98848c`  
		Last Modified: Fri, 13 Feb 2026 00:07:26 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1870cb0c7e97f69c5e4f40f31f44ae1c520a151498367aba0c4403f38ce6e1`  
		Last Modified: Fri, 13 Feb 2026 00:07:26 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3454f015c0e75292e3ea64d758b9843445d53ba6c82d0ce15874fe7eea4da073`  
		Last Modified: Fri, 13 Feb 2026 00:07:41 GMT  
		Size: 224.7 MB (224661634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6edfe3af3a14d149c0108530b021f3a4362e4bd2ff1a6acac826ab569d532a`  
		Last Modified: Fri, 13 Feb 2026 00:07:26 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-jdk-windowsservercore` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:8b2182c9614d10cef41717fc0480244319faa05f1f78a523cf1cd06261136692
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088193652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202f98bea30f592d91f1840cc7caeb9e9b1546fb09efd7b29f27401d51cdf4b0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Fri, 13 Feb 2026 00:05:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 13 Feb 2026 00:06:43 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:06:44 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 13 Feb 2026 00:06:53 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:06:54 GMT
ENV JAVA_VERSION=27-ea+8
# Fri, 13 Feb 2026 00:06:56 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/8/GPL/openjdk-27-ea+8_windows-x64_bin.zip
# Fri, 13 Feb 2026 00:06:58 GMT
ENV JAVA_SHA256=d3ecddd6cae9d89198ec453bda26dd10c1e83e3bfcac8040a493acad08a14c6f
# Fri, 13 Feb 2026 00:08:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 13 Feb 2026 00:08:48 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c87a3784ab1d08cbacea3288e90f8106f6e7a20b792ab27cdc739fc966a73e`  
		Last Modified: Tue, 10 Feb 2026 18:50:57 GMT  
		Size: 373.6 MB (373638099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6643ecba3ab0e56acbda6c8fc09eed623cb962aa6618535fe7c2a047ba8c3fe8`  
		Last Modified: Fri, 13 Feb 2026 00:08:57 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1d4f2e2d35e389b56ef1556dea97a0b12837c858f890e3d9e286e60b1d09fa`  
		Last Modified: Fri, 13 Feb 2026 00:08:57 GMT  
		Size: 499.9 KB (499889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28d3188c353022c84506464e32615b1c11f5e304ebfde7a364454c0f651af746`  
		Last Modified: Fri, 13 Feb 2026 00:08:57 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7d067fa99c77298e8728e50a96b83debbd7bfa5135e128520e7ae9045c3087`  
		Last Modified: Fri, 13 Feb 2026 00:08:57 GMT  
		Size: 337.7 KB (337702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acaf3eb6b64d17c0e95c64795083e33c672e141d417bb7aeafdd9408f359da95`  
		Last Modified: Fri, 13 Feb 2026 00:08:55 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0149da14cb55de299d7afa677d091e172df43f16b9b6f5a280cbb12a22d0bebe`  
		Last Modified: Fri, 13 Feb 2026 00:08:55 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bd1e72a10ed1c6e737f1c729b1f3f8777f4b82bc797acffca244aad0a4c2846`  
		Last Modified: Fri, 13 Feb 2026 00:08:56 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358ba7d2a1f54ed79b92347b051e91f93fd1e8c7a6518ded8146e2a0dd31e75d`  
		Last Modified: Fri, 13 Feb 2026 00:09:11 GMT  
		Size: 224.7 MB (224691024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95658649a6c8ca7c921391fee17951dccd6a8e8528baf31df3ff252b643dbf1`  
		Last Modified: Fri, 13 Feb 2026 00:08:55 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
