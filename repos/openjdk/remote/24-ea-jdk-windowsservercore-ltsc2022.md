## `openjdk:24-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:52aed523cb85b424fd6a7a4973996e3bf6f4934a73799089c1b74089aec41718
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2582; amd64

### `openjdk:24-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2582; amd64

```console
$ docker pull openjdk@sha256:0a65355883750200cc3e8e16e4314027b276538e6f8a24fbd11c40fb7bf68162
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2347036012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:252c3452a87ca673fc18c784ba9d66898e3618e84f90a244e351902c3a92e66c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Wed, 03 Jul 2024 10:07:02 GMT
RUN Install update 10.0.20348.2582
# Fri, 12 Jul 2024 22:07:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 12 Jul 2024 22:08:15 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:16 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 12 Jul 2024 22:08:22 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:22 GMT
ENV JAVA_VERSION=24-ea+6
# Fri, 12 Jul 2024 22:08:23 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk24/6/GPL/openjdk-24-ea+6_windows-x64_bin.zip
# Fri, 12 Jul 2024 22:08:23 GMT
ENV JAVA_SHA256=de012f73dcdc78f7014626b96cb7a381e0bed5be0c8ffac72b7be101bf3d3087
# Fri, 12 Jul 2024 22:08:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 12 Jul 2024 22:08:43 GMT
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
	-	`sha256:90cdef924f34b87fac9d081e881d5e30661c9ca17abd9889d3cbd16e51b55318`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a9e7fd4bd5bb36d2de8797866aea104415fc33c343103bd243cbcf9c749d92`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 371.6 KB (371574 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57cd4e919c0b61bbe3e9a6b040da1951a4f12c5725b5a6b53d161d8900ba7549`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:052c3ef8d7b597e56a45635bf0ee70f053c64814c7edda28501dea69445d4997`  
		Last Modified: Fri, 12 Jul 2024 22:08:48 GMT  
		Size: 356.1 KB (356139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582eb1fbe26795aba53e7144f8a0f62b51b609e0f9c2bc352c4702cd78905519`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e41ef539c1f30af22ee3c64c9bf48227076e34248abf7a6c68380f4259292f8`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0202cbc27c97abfc59dbd69a2d104d1f2523c7d486f7abab35848e6ee51979da`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85be59bfdfb316aa676fb2d5f1649936e2dec45193f165b226871ceb2d84edac`  
		Last Modified: Fri, 12 Jul 2024 22:08:58 GMT  
		Size: 206.7 MB (206700265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39aea13824e6699eafe333d2f94ca11db76d993d13acde4ad6e3126f84b2544d`  
		Last Modified: Fri, 12 Jul 2024 22:08:46 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
