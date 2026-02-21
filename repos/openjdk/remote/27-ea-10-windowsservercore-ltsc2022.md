## `openjdk:27-ea-10-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:5ea636332717f90a6ca399811016d68a362b6ac0ac9dc0b9694ad156e6a3cc91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-10-windowsservercore-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:24e5a260da8c574b7232f3191ad9cc21d5966524909f8d54ae8b89bd08bc67be
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2088364326 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4f20b44fa7828f77b3bb5949fd9c99033a8b324095d81aba563557dae115cd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Fri, 06 Feb 2026 10:02:33 GMT
RUN Install update 10.0.20348.4773
# Sat, 21 Feb 2026 01:26:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 21 Feb 2026 01:27:01 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:27:01 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 21 Feb 2026 01:27:09 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:27:09 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 01:27:10 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/10/GPL/openjdk-27-ea+10_windows-x64_bin.zip
# Sat, 21 Feb 2026 01:27:10 GMT
ENV JAVA_SHA256=243b7c1e79f8514af5765815d8b878c7362cacf8a9c4312c5c9c9e7a1eeee3e9
# Sat, 21 Feb 2026 01:28:57 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Sat, 21 Feb 2026 01:28:58 GMT
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
	-	`sha256:4455e12a722854dec189070503128f07b315332481bd47ab452831f38dee2024`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994b76b7872980b61a0083cfa6cf66aaaead8b2419a21599d91179a735134c33`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 496.7 KB (496733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca81ba43813b91e8f016387b3b31f870e2c80fcee0cd3660ad532f6c08c8e24d`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc4fbc86b4134ba5b52de34e6d38c3e017c75cac92621f976a81487cb2fc65e`  
		Last Modified: Sat, 21 Feb 2026 01:29:05 GMT  
		Size: 344.2 KB (344205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d948c33ed1543b39bba0fba694ed5134d0e8492c95d058bbf5fc165ab385922`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e63f337d7603f477a8287d116bd201911577005cf4f8208281c54031991139dc`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7388502ef9b29d6f07ab81a98f7fba272b5e950ea08befaace6915e2a42bda50`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3a9454f2509be81920740dd24ac124c46498fd9a90e901c4b1ecb7e79b9a31`  
		Last Modified: Sat, 21 Feb 2026 01:29:20 GMT  
		Size: 224.9 MB (224858332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f87699a62cfa4074e20326cea14fb09aeffdf9c9496ac6df7986ad7d8ddf1cf2`  
		Last Modified: Sat, 21 Feb 2026 01:29:03 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
