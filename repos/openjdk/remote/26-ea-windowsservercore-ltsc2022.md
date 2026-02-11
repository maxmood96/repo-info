## `openjdk:26-ea-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:a5f5c6280a0e044ebcb149b9f28f269f1da039dba43bbb3ea5e54d51d420c73c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:26-ea-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:bedb7a78e541da3342e29ee5494ffae56f4b1bb2a7356b46aee1f1940c6143d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2087759313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd817a41e7002c156c1ed82f963546ed3991f807596a7c74abdc3b6deb326a4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Tue, 10 Feb 2026 22:50:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 10 Feb 2026 23:08:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:08:50 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Feb 2026 23:08:55 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:08:56 GMT
ENV JAVA_VERSION=26-ea+33
# Tue, 10 Feb 2026 23:08:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/33/GPL/openjdk-26-ea+33_windows-x64_bin.zip
# Tue, 10 Feb 2026 23:08:57 GMT
ENV JAVA_SHA256=1613acc47081355dcb54aca5db4a0cc088734861b42bd254657ab88fd50944ec
# Tue, 10 Feb 2026 23:09:20 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 10 Feb 2026 23:09:21 GMT
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
	-	`sha256:30e5017e3b27d0eb763aca0362354553282eee78a4264a4b5ecd6f52bd60dcd3`  
		Last Modified: Tue, 10 Feb 2026 22:51:59 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee72633dd7fdc1a4c854ac578e0ac5359c6b631366ca6d14a3f670b06c2b368`  
		Last Modified: Tue, 10 Feb 2026 23:09:27 GMT  
		Size: 489.7 KB (489714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce87a5c5be33f6f9458f48e0ba1f8317355a6d48f0d865b7cf042eb5836e104e`  
		Last Modified: Tue, 10 Feb 2026 23:09:26 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb2e51325e08400298f12fcce70d7795358031c3448c57d61151bb89897a770`  
		Last Modified: Tue, 10 Feb 2026 23:09:26 GMT  
		Size: 338.2 KB (338250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3870e1253c3451fa4281f5388609dc880b7f9129c84824089cee2592a54bde25`  
		Last Modified: Tue, 10 Feb 2026 23:09:25 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04456c1d6886e520c01d4adb7944ac8b5b833255060782da083e0c6ab723e754`  
		Last Modified: Tue, 10 Feb 2026 23:09:25 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b888b8ae420779213e33551df0b681edc622bfd6d57bb3c97f40a6b4be7753`  
		Last Modified: Tue, 10 Feb 2026 23:09:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8e95a8734b0f28d19d3608a6f3a1da5c4dc780223a4d8ac3b9e03a5a296cb3`  
		Last Modified: Tue, 10 Feb 2026 23:09:41 GMT  
		Size: 224.3 MB (224266304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3822630386c039fc1629f02416057b6998e108e0433ffbe1d2439ef4251f00ec`  
		Last Modified: Tue, 10 Feb 2026 23:09:25 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
