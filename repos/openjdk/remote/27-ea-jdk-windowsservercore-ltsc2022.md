## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:293ee88ef74b15fb956f30aa9e4b40c768e397b7c8611c0eec680d40ef6ebce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:eb45b67eedd2803108228b7d138f1734ea1f42063f5329a377a22749b6bbbfdb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2208196475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:375ceea08424f1c4ed435d91153a165b9ece980ff59ad6a3a0c4d3924bcc7fa8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 06 Apr 2026 18:26:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 06 Apr 2026 18:27:41 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:42 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 06 Apr 2026 18:27:50 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:27:51 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:27:53 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/16/GPL/openjdk-27-ea+16_windows-x64_bin.zip
# Mon, 06 Apr 2026 18:27:54 GMT
ENV JAVA_SHA256=e5c718947519c88a2ee3b23aea3ed1da5b81b674c4f03fe8b29395ab126d36ef
# Mon, 06 Apr 2026 18:29:48 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 06 Apr 2026 18:29:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c72fc8f6d3e1f9d440258f21d8669b9f0aacd885e9cd5dca2fa0d7efc6b5ca90`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a1553d29986a9afb26d4654683f1640f6f5f4f5a1637762f21ea6bd52ff4eb2`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 505.9 KB (505856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc798538ff19391e156cfcfcf19134db65f1e7df7a15398665449f507ec0f6fe`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d657fb46d0888e2aa30abce440e4032931b2529f37b54c8463f7310a72501d79`  
		Last Modified: Mon, 06 Apr 2026 18:29:58 GMT  
		Size: 305.2 KB (305152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:946f805fdce7eec62bf36217cfd5f5ed02496dd69856c4f98f613cb8031b0dc6`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fefd9ec11c6c5e977745bd6d4906d7d8cc642ebe011af12ee7a9ec283e776f78`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b71f33cf29a9362f6eb1f8279aed2d8fed2752ba4f501b5f0a30592b121a502`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:627d952d69a2940a1429a6cbdfd79099f24b6b31fecba88395849e0349d83293`  
		Last Modified: Mon, 06 Apr 2026 18:30:14 GMT  
		Size: 225.1 MB (225096230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e0deca905a948981090dfd879486816c4e6e4e61185951e3290595eaae9145`  
		Last Modified: Mon, 06 Apr 2026 18:29:56 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
