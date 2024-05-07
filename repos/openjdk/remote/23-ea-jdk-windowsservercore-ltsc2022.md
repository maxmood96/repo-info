## `openjdk:23-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:d0553d9b7414b9c186d4c83ebce3eb4dbe019bcfd02c63592b2d580bf91467dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2402; amd64

### `openjdk:23-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.2402; amd64

```console
$ docker pull openjdk@sha256:df36e821a20956bc802d5d13eeae54595808c7034d7a44c295373587a1be69d9
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2204944196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c0844910b5456d3100887152bc514685920365500d596d8f7552ae688c45d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Mon, 06 May 2024 23:05:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 May 2024 23:05:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 May 2024 23:05:40 GMT
ENV JAVA_HOME=C:\openjdk-23
# Mon, 06 May 2024 23:05:46 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 May 2024 23:05:46 GMT
ENV JAVA_VERSION=23-ea+21
# Mon, 06 May 2024 23:05:47 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/21/GPL/openjdk-23-ea+21_windows-x64_bin.zip
# Mon, 06 May 2024 23:05:48 GMT
ENV JAVA_SHA256=c98243a78a073b3efebfce22fb6ecfd0dd918c983fb0812e40259405e02ee2a0
# Mon, 06 May 2024 23:06:09 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 May 2024 23:06:10 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233f06d7c97ef59b2ff97fbff627960eba0bf623661dfc9985695079d2205368`  
		Last Modified: Mon, 06 May 2024 23:06:18 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb65ac230c3b2317101cf717a049133af5e86b5f28b26d12af41b2481ea9fb8`  
		Last Modified: Mon, 06 May 2024 23:06:18 GMT  
		Size: 489.7 KB (489671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:972aab4e941c760a040d698202dd6e8579d2e20da4590ff51aeb4d1fb1b1a783`  
		Last Modified: Mon, 06 May 2024 23:06:18 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484716df6e899088f21d054693c1d8e4751de30fbde9a9d83138461ed2e115c1`  
		Last Modified: Mon, 06 May 2024 23:06:18 GMT  
		Size: 342.4 KB (342419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5aaaff1498af49ad882dc5e8c5430c9deb706ca4b00be46a50cb5949bda0dc`  
		Last Modified: Mon, 06 May 2024 23:06:15 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d2c36ebcf5a1d765b70198e0abb77bba789ca9da73bc225f0642e5c1b573a0`  
		Last Modified: Mon, 06 May 2024 23:06:16 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d2858da77ae620b58db737a562d2f3d7455ee5dc39c06fc9328bf23f110d801`  
		Last Modified: Mon, 06 May 2024 23:06:16 GMT  
		Size: 1.3 KB (1302 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee1ef39eeaa7c254a6b15099a5e12fadf8c53abe1ae8ffae8f30077f47eb2c3`  
		Last Modified: Mon, 06 May 2024 23:06:26 GMT  
		Size: 204.7 MB (204730723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10c9091475e31906e1c86ee8efc38207c41f4656db9486024e8e39f02da80aa`  
		Last Modified: Mon, 06 May 2024 23:06:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
