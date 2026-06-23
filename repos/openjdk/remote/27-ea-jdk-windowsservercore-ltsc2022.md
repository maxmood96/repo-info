## `openjdk:27-ea-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:7dcf42a6185e3f06d69ee1e3969664f1168b0a60a58c8580f13c97c6a8ba037f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5256; amd64

### `openjdk:27-ea-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5256; amd64

```console
$ docker pull openjdk@sha256:e048a4ca63828a80c91e1d4243d37bcd084817a075227ca98b54372bdd2c4aff
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2356493763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88bc863c516de819abdb42c530d594dd1151391e93c730cd69d990eff6cdd54`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Sun, 07 Jun 2026 06:43:23 GMT
RUN Install update 10.0.20348.5256
# Mon, 22 Jun 2026 22:44:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 22 Jun 2026 22:45:16 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:45:17 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 22 Jun 2026 22:45:26 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:45:27 GMT
ENV JAVA_VERSION=27-ea+27
# Mon, 22 Jun 2026 22:45:27 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/27/GPL/openjdk-27-ea+27_windows-x64_bin.zip
# Mon, 22 Jun 2026 22:45:29 GMT
ENV JAVA_SHA256=95f2039dcf26a1c012aaa98a839b7c4ccc5974f9697e6d7c7c6a332afcf12fed
# Mon, 22 Jun 2026 22:46:42 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Mon, 22 Jun 2026 22:46:43 GMT
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
	-	`sha256:5c95a3509eb5b1e3191c0c24f4e8d70327752ac2b10ac257f83ad7555d263ee1`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c346f0d4d92e655eb3a2ada75422b42a066d7817184a8b161363b8cf4f437750`  
		Last Modified: Mon, 22 Jun 2026 22:46:50 GMT  
		Size: 502.4 KB (502416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ad18c4c77cb604f9aed745b28124908916593ba55de3defd3d416b9ed5e60cb`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9b221005e200979d08b3d8ef1cd1359f6d49de2db1ad2419d4d5b198f8d42b3`  
		Last Modified: Mon, 22 Jun 2026 22:46:49 GMT  
		Size: 352.2 KB (352208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1248870a9b37975620492cc95b831602f8340587f9d8ff0b95cbc2f908547d`  
		Last Modified: Mon, 22 Jun 2026 22:46:47 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06cfbb859d3cdbc93be9ed335a20ad4436647dd7d80f80cdf545f96f3a2f7052`  
		Last Modified: Mon, 22 Jun 2026 22:46:47 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d158d53a993eb382bf1f611bc359f77a733ab166e9cebc8fca7f6ec8c484a8e9`  
		Last Modified: Mon, 22 Jun 2026 22:46:48 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c92dadbba67903e0eb8376fc8b7ccc1dca8dd09d684d41f0b23e05c7302b793`  
		Last Modified: Mon, 22 Jun 2026 22:47:02 GMT  
		Size: 223.5 MB (223505748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a894cdac940df41f38ad86a46384b8f84dc6ab593cdd7da5802a0108eaded6e`  
		Last Modified: Mon, 22 Jun 2026 22:46:47 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
