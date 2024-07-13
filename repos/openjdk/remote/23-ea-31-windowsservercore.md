## `openjdk:23-ea-31-windowsservercore`

```console
$ docker pull openjdk@sha256:ae0af5509620d0f6c6b59c62cd046f0a3368392d8f7a4c6cf27460490432da70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2582; amd64
	-	windows version 10.0.17763.6054; amd64

### `openjdk:23-ea-31-windowsservercore` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:83de0e5da6c2e07e8768e135fc551c7f91f7cb42106a6d5bf04e6f4882ed3060
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346749993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16123944cec3a5879ce76788de77f5f6cdb2cdf1e4cf2c07ae2dd071ae9dd3cb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 12 Jul 2024 22:00:57 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:01:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:01:06 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 12 Jul 2024 22:01:12 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:01:12 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 22:01:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:01:14 GMT
ENV JAVA_SHA256=7894a87e50c30dfa4be1f1432dfb289c4de40e1c0fd447b8f4b5fce3141e6615
# Fri, 12 Jul 2024 22:01:31 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:01:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f0206d135152eb909f50159d6ca348a5aead199afacbafc000b770c1b0720f6`  
		Last Modified: Tue, 09 Jul 2024 18:30:31 GMT  
		Size: 751.0 MB (751001543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18a50da7446f6b879900d4a46641e38ebbddc6006b94f71a2f3237c06d89acfa`  
		Last Modified: Fri, 12 Jul 2024 22:01:40 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65a5bf071f393dbfa3d42014a3d3142bb76c0035b57fd311b94132edd15a0fa`  
		Last Modified: Fri, 12 Jul 2024 22:01:40 GMT  
		Size: 359.6 KB (359587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dd96e949fcaf81c98afa509c043c4cc04aca6ffc122586f646de13b5cf02b4`  
		Last Modified: Fri, 12 Jul 2024 22:01:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27130019b0d98ed213425d82413a23238997d405a0607e2f429d5e408f9d6d1`  
		Last Modified: Fri, 12 Jul 2024 22:01:40 GMT  
		Size: 346.1 KB (346144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c40013168fbbb7e81331173e0eb945c1867227485ca56ff26e36c46e72330a`  
		Last Modified: Fri, 12 Jul 2024 22:01:38 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb0bd54db4c1ebe2aafd17c57a9d2cc352884132d6b4e2618f09c0c314647857`  
		Last Modified: Fri, 12 Jul 2024 22:01:37 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a248220857a340bd6df7ea494655fca068a4679f8761680a1177f05b520e6d`  
		Last Modified: Fri, 12 Jul 2024 22:01:38 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bea9a3f678d7a2cd9120cefa308f1f5d8b48788deea8fb2c284d39f43c634937`  
		Last Modified: Fri, 12 Jul 2024 22:01:49 GMT  
		Size: 206.4 MB (206436219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f38cfc8c3a631f2de1186966ae41ac1f938880ee40de66a860253c2ae5b146c3`  
		Last Modified: Fri, 12 Jul 2024 22:01:38 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:23-ea-31-windowsservercore` - windows version 10.0.17763.6054; amd64

```console
$ docker pull openjdk@sha256:3610b7fea5f423b9172d83a8ca638462d58e5f1d72e0662ca95c601ddca33b00
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2445733678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:323f9a364646f0f49617668117e43a9444200f938b18526177ac02263b9a87f7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Wed, 03 Jul 2024 00:34:32 GMT
RUN Install update 10.0.17763.6054
# Fri, 12 Jul 2024 22:07:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:08:23 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:24 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 12 Jul 2024 22:08:44 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:45 GMT
ENV JAVA_VERSION=23-ea+31
# Fri, 12 Jul 2024 22:08:46 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/31/GPL/openjdk-23-ea+31_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:08:46 GMT
ENV JAVA_SHA256=7894a87e50c30dfa4be1f1432dfb289c4de40e1c0fd447b8f4b5fce3141e6615
# Fri, 12 Jul 2024 22:09:23 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:09:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5f98e7fe87492b83d7775a348ae0c94412b638ab5bba1a80b03c3a547708acd`  
		Last Modified: Tue, 09 Jul 2024 17:23:28 GMT  
		Size: 587.8 MB (587809033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e038a148c7feb7f6010c1a044eab9010d7366ab1fb7354bf3b1c47a5a899c5`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a09613aba4fe06f7a33a4835642da64c9046a3ba825deaf232d6ff53ebd87f`  
		Last Modified: Fri, 12 Jul 2024 22:09:33 GMT  
		Size: 499.5 KB (499451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c636eb003f485953497b0c84c27688c71b18f764c6609c1546aabeff7347395`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:181510fa1de9a60c846800436a088f4d2cb5934c9175973eaa381e31122d28c8`  
		Last Modified: Fri, 12 Jul 2024 22:09:32 GMT  
		Size: 351.3 KB (351272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:423b6a3d8d9b45b5894ac877a42feccabc49fbf7ed8ce3bab9864501e9a182e0`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e44444c0cd7387445289886fb4133a979f4cd09dd206dc4b2b7af4ff966ed64c`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2291c13bd05a63826b47b0ee530a041dccf8f00fc1bbbcf3f077a45b83e5c37a`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e71d5824591b9663c45a15dc762c052a8e43d1fe7365b96439431495da924a9f`  
		Last Modified: Fri, 12 Jul 2024 22:09:41 GMT  
		Size: 206.4 MB (206445751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35fd2491ff21be1bde2b47a997dcbde2488df01ebea2aaa7771668517d82b08c`  
		Last Modified: Fri, 12 Jul 2024 22:09:30 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
