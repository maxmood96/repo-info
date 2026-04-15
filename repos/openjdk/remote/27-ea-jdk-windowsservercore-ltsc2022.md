## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:59ed8e6a1c4704be3d6539e8ef17e0328d9e4076087884d3f92bb8ec0a60aed7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5020; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5020; amd64

```console
$ docker pull openjdk@sha256:82a1e3b2456a44cb3c7cda1e7cad70926a42db10057a8480036b07fb1615555f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2296241918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8710eed708c01f046c91f118281e1b8fbf8d1412eea4b736910482d904bd730d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:27:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:28:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:28:03 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 14 Apr 2026 21:28:10 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:28:12 GMT
ENV JAVA_VERSION=27-ea+17
# Tue, 14 Apr 2026 21:28:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/17/GPL/openjdk-27-ea+17_windows-x64_bin.zip
# Tue, 14 Apr 2026 21:28:13 GMT
ENV JAVA_SHA256=3cc253c247f136b430f6f42ac667120512f18fff012cfbf20817c6425edf15c7
# Tue, 14 Apr 2026 21:29:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:29:19 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48a7714c59919c6d44b28cf949bd217d46331d307a2e65ee104808286d94e42d`  
		Last Modified: Tue, 14 Apr 2026 21:29:26 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21c3b0b3d2577cbf533fea0da989b44db0c4d3517aa9be19594e7498351686ad`  
		Last Modified: Tue, 14 Apr 2026 21:29:26 GMT  
		Size: 498.0 KB (497977 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3686f058a0872f704d42eaec54442f986f56c3f54b436baf160194f7d32417c`  
		Last Modified: Tue, 14 Apr 2026 21:29:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfc6ebceebf7adaefa0f4e550b5b37607999f707505431435d2699b5204aade5`  
		Last Modified: Tue, 14 Apr 2026 21:29:27 GMT  
		Size: 344.3 KB (344333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba0b905db28010609a00e5647a94f27d5c64155c70bbbf1a50623fe04ccf517`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80e70d0045bdfd8ef733b1fe499f0fe50d8516eeef6a6556296d43390484317d`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f8fb0859c184b9cdd81c522accd01484d857babd9c5e560bf06a0ee2fb15a6`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae97122d31259f7791675d94a05e21ba7971565d0efd458705ffb92368f84d03`  
		Last Modified: Tue, 14 Apr 2026 21:29:41 GMT  
		Size: 225.2 MB (225180440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4035c286f1de5c9f4bb9d5c1288d03d05748e680a7ec469a879810e566945263`  
		Last Modified: Tue, 14 Apr 2026 21:29:25 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
