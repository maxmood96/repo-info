## `openjdk:26-ea-windowsservercore`

```console
$ docker pull openjdk@sha256:47a9a60948809e466efa51291a471d39f5536fa794eda64917c300839b9e243e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.6899; amd64
	-	windows version 10.0.20348.4294; amd64

### `openjdk:26-ea-windowsservercore` - windows version 10.0.26100.6899; amd64

```console
$ docker pull openjdk@sha256:bd608056e62d6b3613bb95b9aa98ef8055d4f653338be82e240ebda5b346597e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3442753626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ac62255e89d3e00fbc8daeec622254b8637fb56584e8fea5f2f031001939602`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 11 Oct 2025 16:27:11 GMT
RUN Install update 10.0.26100.6899
# Tue, 14 Oct 2025 20:43:35 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:54:19 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:54:19 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Oct 2025 20:54:24 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:54:25 GMT
ENV JAVA_VERSION=26-ea+19
# Tue, 14 Oct 2025 20:54:26 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_windows-x64_bin.zip
# Tue, 14 Oct 2025 20:54:27 GMT
ENV JAVA_SHA256=b31dc1d0afdaba4c6b7a399e0a932fb1a4f5a61e7624aaad8ca40b85400f966a
# Tue, 14 Oct 2025 20:54:46 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:54:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 09 Oct 2025 08:11:23 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a050b25516334eac5bca074c4f4b42f39b3cf4be3d40626ee4f574c862e03e8b`  
		Last Modified: Tue, 14 Oct 2025 21:11:35 GMT  
		Size: 1.0 GB (1005173296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b31ef2acd9573fa311450133976eaea07e0ccfd74f3de24d672c7bf465eba24`  
		Last Modified: Tue, 14 Oct 2025 20:51:54 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38b1d59512b551b45d414cee37daf983b7e1db9327373d30999488444a9d4a67`  
		Last Modified: Tue, 14 Oct 2025 20:55:14 GMT  
		Size: 351.5 KB (351473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c92d8adfdb171a3e6e4f28b1f5ebb38a4c00e47ef027af283cb1028603b896d`  
		Last Modified: Tue, 14 Oct 2025 20:55:14 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1253aed0cf5f5b54316975d1ce65169de1e4545304939eae66cfb2734f35053c`  
		Last Modified: Tue, 14 Oct 2025 20:55:14 GMT  
		Size: 333.5 KB (333508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9dbf428108e664fd0924172d860f5d96ca974edefcfb2968c5651477f7323e78`  
		Last Modified: Tue, 14 Oct 2025 20:55:14 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9b68131a614948acc9ddd72825f41311731962ec7093bf81b8da90c089c894`  
		Last Modified: Tue, 14 Oct 2025 20:55:14 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de8a3c56dd1322543b956f6f2282d057edbd672411f5eb954be152c944a868d`  
		Last Modified: Tue, 14 Oct 2025 20:55:14 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1dc3bab9885e556b67a45bf3d335b7745c95fb73c06bb1fb3cebc710fc76e9`  
		Last Modified: Tue, 14 Oct 2025 21:15:58 GMT  
		Size: 221.6 MB (221580352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a609c50553ade2f4acfb34b9962b4cfcf5d30e4e72092d01fa4cee1b147b11c0`  
		Last Modified: Tue, 14 Oct 2025 20:55:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-ea-windowsservercore` - windows version 10.0.20348.4294; amd64

```console
$ docker pull openjdk@sha256:826622f424a234bb80f061d12735170cd24bbfade47fe1dcaa84b424ede2d7fe
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.7 GB (1711295615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ed2284ebc3ba5149ccc40460d57418b935c1e9f9a8ada6cdbadae7593f22051`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 14 Oct 2025 20:50:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Oct 2025 20:51:05 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:51:06 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 14 Oct 2025 20:51:11 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:51:12 GMT
ENV JAVA_VERSION=26-ea+19
# Tue, 14 Oct 2025 20:51:13 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk26/19/GPL/openjdk-26-ea+19_windows-x64_bin.zip
# Tue, 14 Oct 2025 20:51:14 GMT
ENV JAVA_SHA256=b31dc1d0afdaba4c6b7a399e0a932fb1a4f5a61e7624aaad8ca40b85400f966a
# Tue, 14 Oct 2025 20:51:36 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 14 Oct 2025 20:51:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:800e1d3f69793c122ec179934d6ba62874c4636dfa09f29bd4cc31d710eab334`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af3e7f9a82d03757fd0bbe74b3783c6b5aceccb36c9330419dde769e20a0b519`  
		Last Modified: Tue, 14 Oct 2025 20:52:12 GMT  
		Size: 354.7 KB (354731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c35fb1972f31007fd8d78ed3bd86fa2455980e8358f386b82aea00b6cef2a8`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33f8871d8c32099b6cb070a0ad034b8664063fd00391d024ce6094bd5b6b97a7`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 336.7 KB (336698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:543865876369a319b8baa942b507f3448a826fed7ac2d6665cdbb9d105ca8018`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51eacc050d2cbfc45cfb812157a3700b260b86a5317a9777b0362de9f468f5c8`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a03ba4752e9d2a0572cc028c4abecfe0a3e8467f435211e0d61e2198f9f62fef`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d9280d6a32905e49059a8c0b9331bce31be805bed426e6cc1a174fda17d6a3`  
		Last Modified: Tue, 14 Oct 2025 21:14:49 GMT  
		Size: 221.6 MB (221577231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52eb6ada84434bb960a11cad9e432fcfb66233be467e6f684b5828a5210a0e9f`  
		Last Modified: Tue, 14 Oct 2025 20:52:11 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
