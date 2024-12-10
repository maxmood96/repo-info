## `openjdk:25-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:3a999484e2df5bb3ba18a61f7c868e813c95a9f2847c9d787e65b3dc0fb421bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2849; amd64

### `openjdk:25-windowsservercore-ltsc2022` - windows version 10.0.20348.2849; amd64

```console
$ docker pull openjdk@sha256:1a748c153e40408b6a98ac41158362e3eda044bf98804decce613cef9bb2a72a
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2462141129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134a6f3207995540f1dca2c8fdd2ab20c55407379a98250ec4a87487b6a05fac`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sat, 02 Nov 2024 23:52:43 GMT
RUN Install update 10.0.20348.2849
# Mon, 09 Dec 2024 23:30:00 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 09 Dec 2024 23:30:49 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:30:49 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 09 Dec 2024 23:30:57 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:30:57 GMT
ENV JAVA_VERSION=25-ea+1
# Mon, 09 Dec 2024 23:30:58 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk25/1/GPL/openjdk-25-ea+1_windows-x64_bin.zip
# Mon, 09 Dec 2024 23:30:58 GMT
ENV JAVA_SHA256=e613057ce9dd454d410ac2462a504dd7679eeec29d28c18c9d16c6d12f12f346
# Mon, 09 Dec 2024 23:31:26 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 09 Dec 2024 23:31:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5987a3191d90ca1e07fd03dae1963abcaa49ceabc649ec3bc43f2c96b55d0464`  
		Last Modified: Tue, 12 Nov 2024 18:35:44 GMT  
		Size: 790.3 MB (790291816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f62744fe0bffce54ba5c69993794a493843c155d541e18b0d74f9365ff6f07`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dec8c4be008b03b6877f47753901f70a486eb2b094f302794690be01bc06154`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 363.4 KB (363444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93a3c453de130ff99a3d6f4cf73bf82b0a7085b98beb3e48482f8817aed6fdf1`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 1.3 KB (1310 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9384c35821d963b7ac1a73f732165922794ef59958ddafb3100ba91fc51ce89`  
		Last Modified: Mon, 09 Dec 2024 23:31:34 GMT  
		Size: 347.2 KB (347190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafd07f0b873df552e6d036c1491e18167cdb70d61048e9cfba67a359a1e435d`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5515e93df28f8f47408a0476e608aca15b9b52350b657b0edffaafe332133f22`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea4197bd5a482eed83557bce5b488187d0214329960e1ccd914ff3b6a1b748a`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.4 KB (1364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113bcb9ec4332b2f117ae80b264a590be20614177d2b66c22f4ce4ed81c00581`  
		Last Modified: Mon, 09 Dec 2024 23:31:44 GMT  
		Size: 208.9 MB (208938413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18b0c92d636855cdb04428662688d9eee149c1ce9d32c1b88427b546b233ff47`  
		Last Modified: Mon, 09 Dec 2024 23:31:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
