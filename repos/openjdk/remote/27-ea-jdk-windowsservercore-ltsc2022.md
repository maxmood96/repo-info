## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:65ef34b18b92e20c2345d525984029731c96833d353d0165ef6e53baf8c9dd1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:0a74bc457c711df98624b6e5a3cc6927933c6ed36aaa42225a6f4d525c421cc5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356489813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ae0f24279e0692fa25178249f05d69993454aa58e0bd8f0559a36c8e2afad91`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Fri, 26 Jun 2026 22:42:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 26 Jun 2026 22:43:54 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:43:55 GMT
ENV JAVA_HOME=C:\openjdk-27
# Fri, 26 Jun 2026 22:44:01 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:44:02 GMT
ENV JAVA_VERSION=27-ea+28
# Fri, 26 Jun 2026 22:44:03 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/28/GPL/openjdk-27-ea+28_windows-x64_bin.zip
# Fri, 26 Jun 2026 22:44:03 GMT
ENV JAVA_SHA256=72394e06c335cb58cef351c47e54a05ebb0c03338f3d2f92fb941927445670aa
# Fri, 26 Jun 2026 22:44:27 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 26 Jun 2026 22:44:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6897a04901ec162be0eabd7eb636b5ac50d6e37c880f1db618610f2d777b1ce6`  
		Last Modified: Tue, 09 Jun 2026 18:12:58 GMT  
		Size: 643.1 MB (643106423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86db39de90fa66eb59ab6cb9ba63de096a82f3a4a2b82bb7f5925cf2a75561cb`  
		Last Modified: Fri, 26 Jun 2026 22:44:34 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dffa60f5533a4048a391bfda0c3d4111e570de875e59ac8b442f4ec34630dd3e`  
		Last Modified: Fri, 26 Jun 2026 22:44:34 GMT  
		Size: 502.9 KB (502869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f557beeb3133b38d24a6978e5ea4f03f4c28f2219ed4981e37a914392226c15c`  
		Last Modified: Fri, 26 Jun 2026 22:44:34 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41f6af9a5e936d1d4ce4acb388cba9adf0ca3d17d25b379618f12231b8cb47e`  
		Last Modified: Fri, 26 Jun 2026 22:44:34 GMT  
		Size: 351.4 KB (351420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c0aa851635537ed61db16ec07c34b2b78571a921d1f60bcee7122fe8dc70c9`  
		Last Modified: Fri, 26 Jun 2026 22:44:32 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1cb28349dd1e5bd1e010676c03c883a1b8b59a08e1f33f0941f4750c4be326a`  
		Last Modified: Fri, 26 Jun 2026 22:44:32 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f3208f76fefc5c1b03993b4898a83d0702cc0618190a0400df7f5b9408a660`  
		Last Modified: Fri, 26 Jun 2026 22:44:32 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d8f3527f7b431c728c6756d5ecd5d8c99306a685b125094ed045eebcba325c`  
		Last Modified: Fri, 26 Jun 2026 22:44:46 GMT  
		Size: 223.5 MB (223502134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04c3f08d4182e9ef469e5562edd093885b32a210d9496c78db34fb00e3353f2a`  
		Last Modified: Fri, 26 Jun 2026 22:44:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
