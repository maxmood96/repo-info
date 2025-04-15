## `openjdk:25-windowsservercore-ltsc2025`

```console
$ docker pull openjdk@sha256:90193af865a08b7a345fada4ac8926081378ef8e1c5684021af41884bfd6a1b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3775; amd64

### `openjdk:25-windowsservercore-ltsc2025` - windows version 10.0.26100.3775; amd64

```console
$ docker pull openjdk@sha256:77f162bda00e724a0d2525a72c6707c514ec1ff879cc438662b6f4fd501ca067
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3603479545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee748757f7208a2dadbc267357d82fc6bf020371d35b9c85cfffab3a23c1d11b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 06 Apr 2025 07:48:58 GMT
RUN Install update 10.0.26100.3775
# Mon, 14 Apr 2025 23:05:08 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 14 Apr 2025 23:05:22 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:05:23 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:05:31 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:05:33 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:05:35 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/18/GPL/openjdk-25-ea+18_windows-x64_bin.zip
# Mon, 14 Apr 2025 23:05:37 GMT
ENV JAVA_SHA256=41f24482b5d173e5a8f242d81909835bd7e85fdb131b901bff9a150186c3c03c
# Mon, 14 Apr 2025 23:05:56 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 14 Apr 2025 23:05:57 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:761846874dadc4dd9490d5635a266306989ac061986d0e4bcfe36a76ef6888b8`  
		Last Modified: Tue, 08 Apr 2025 21:29:58 GMT  
		Size: 1.2 GB (1179372285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59547f15d816541b9e52f79da41e5915341f9161ea4407c06790e8f499d801e6`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2052da3b70068b8084d54a8cc947ba9d64c214dc8af5c47621341dcab19f6fae`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 409.9 KB (409911 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26a2027742f2fb8b2b88d4c10ae07d814c258c0e8fe4cc2cd860bab11f4efc29`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24012a31c58ece28351ee6560c6e49a900ee1dc8fdb0d62d065892eb8cb1ba1b`  
		Last Modified: Mon, 14 Apr 2025 23:06:05 GMT  
		Size: 388.0 KB (388039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c996547c40ebafa0f8cd758453bb89e959cddf9ab37fd47c2ca5d27becce4c`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a70be02496f600d630ce63232129d27b16ca988c5f72590f75ae5d3ea257c16`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1120fbf6386950eebcbd7e341e0e84cc56917a6a7a2b0556f2fc1ce7c6e6dc1`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4845737e64f189008c0cba13b849a661c127131aa7374fd1d524a41ab676a57`  
		Last Modified: Mon, 14 Apr 2025 23:06:16 GMT  
		Size: 208.0 MB (207994250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba50aa4cdb293648d84e79b4dee88834c018912b9f24d45eeb1a6d66588777a8`  
		Last Modified: Mon, 14 Apr 2025 23:06:03 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
