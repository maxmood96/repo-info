## `openjdk:28-ea-1-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:e7c14e7af03b055c201963727e7550a99f7de6a6d22bfe034b5e7df096d5312f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:28-ea-1-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:384f2b77658d886f2fb51c0c99f12d4256c32e012068e924e49b2985daaec8d4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356512747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c8dbc8eff6903ac91d970867d7948846b574e9b8344d796c14ca963902aef6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Wed, 10 Jun 2026 20:32:43 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jun 2026 20:32:50 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Wed, 10 Jun 2026 20:32:50 GMT
ENV JAVA_HOME=C:\openjdk-28
# Wed, 10 Jun 2026 20:32:55 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Wed, 10 Jun 2026 20:32:56 GMT
ENV JAVA_VERSION=28-ea+1
# Wed, 10 Jun 2026 20:32:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk28/1/GPL/openjdk-28-ea+1_windows-x64_bin.zip
# Wed, 10 Jun 2026 20:32:57 GMT
ENV JAVA_SHA256=4aaad6cb26305877733b973a209216ad1ed529c381dd88c56e3ab87f579f96cc
# Wed, 10 Jun 2026 20:33:17 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Wed, 10 Jun 2026 20:33:18 GMT
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
	-	`sha256:abd9121b5774d0150ac1e22ec7200dd419a682811de66fff0c1551a900021c0b`  
		Last Modified: Wed, 10 Jun 2026 20:33:24 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb0d28702d321cc626a04fa13376320206724f7fb22a27b8f622af9b427fb6a`  
		Last Modified: Wed, 10 Jun 2026 20:33:25 GMT  
		Size: 488.9 KB (488857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0badc65f3a24a04834f832f7a732c98d4474a0e525173fee01f851e2473fa51`  
		Last Modified: Wed, 10 Jun 2026 20:33:24 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b5b8ebec94fce3e3e71541e14d596ca4b26e1f7148cfc946e826dbe7eb0f65d`  
		Last Modified: Wed, 10 Jun 2026 20:33:24 GMT  
		Size: 337.4 KB (337379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b164be2425dc6c1f79bf5f74339240217ce9ea8b95b53c99e5fa66f9eb74856c`  
		Last Modified: Wed, 10 Jun 2026 20:33:22 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3e476fbc093820445ba9246996283985e11a939a5cd1a82abf079b05dd9b826`  
		Last Modified: Wed, 10 Jun 2026 20:33:22 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f2af31251073e2fbc37360c703cd7c1001282772e16d29f15f3fdcbdad5a54`  
		Last Modified: Wed, 10 Jun 2026 20:33:22 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86eabee0208761fe0cff9a133d7d25f05886835ad1d97a7b6a01e1b46756c42b`  
		Last Modified: Wed, 10 Jun 2026 20:33:35 GMT  
		Size: 223.6 MB (223553179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ddbdaa6f5cbf6df581dbc08baa9746c985702f2370158c339b9e01fe97afed0`  
		Last Modified: Wed, 10 Jun 2026 20:33:22 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
