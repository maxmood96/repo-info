## `openjdk:23-ea-17-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:9e6be2ca379de02348bc1caa93adca4907210247b4b05d767c36d4c6a49cc989
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2340; amd64

### `openjdk:23-ea-17-windowsservercore-ltsc2022` - windows version 10.0.20348.2340; amd64

```console
$ docker pull openjdk@sha256:c2ed2016840fd187e0c5aaf6f904ca339ed4d00fa27ae5979a565773be356b5d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2163941614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e93138e46ab23fd558e679d4d53df6c019e7c1605742f65ecbd42e753ad014a8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Tue, 05 Mar 2024 19:55:40 GMT
RUN Install update 10.0.20348.2340
# Fri, 05 Apr 2024 17:52:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 05 Apr 2024 17:53:57 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:53:57 GMT
ENV JAVA_HOME=C:\openjdk-23
# Fri, 05 Apr 2024 17:54:04 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:04 GMT
ENV JAVA_VERSION=23-ea+17
# Fri, 05 Apr 2024 17:54:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk23/17/GPL/openjdk-23-ea+17_windows-x64_bin.zip
# Fri, 05 Apr 2024 17:54:06 GMT
ENV JAVA_SHA256=d370ad95643e427d9a9f79c527dc3dfbd3fa07ebda3684fe18acba87d4342d57
# Fri, 05 Apr 2024 17:54:40 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Fri, 05 Apr 2024 17:54:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a61557bf66429be9509f579104808d2853f8f7aefbd49ef26f5f2a90266c46f5`  
		Last Modified: Tue, 12 Mar 2024 17:28:14 GMT  
		Size: 568.9 MB (568860197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29e6da9a119af4900ca32e7b72e122af663d0c124c61162d59efce181be7bf0`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 1.3 KB (1273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2260ed09da21f9844f71fe2f97d63be6d31052332d236c6d78f6525c097f3208`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 509.0 KB (508964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eac57ad1d60d5d20bed6a8a531f654d28a38a043230a2226f7a4913192e8f97`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0850ecf148b4540cf47e5c126725a34c47594df7bb9ccbd475ae0da660a0d992`  
		Last Modified: Fri, 05 Apr 2024 17:54:46 GMT  
		Size: 321.6 KB (321636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57467fcd890b73dd9072775adcb46283f46e151e9f013f84b6df594d2cb9d7ec`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c3b845283c23d3a90f00bdf78916e544dd70f7165a1589b4f42db67bff108c`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54fa450c09a6088c806903d531b21ee15bf1c1d1bb582207065e44fd4168a4c4`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6448a5c4e84a34dcc2a4253d4893a3527f73b68e5eafdde1b251edebf943091`  
		Last Modified: Fri, 05 Apr 2024 17:54:56 GMT  
		Size: 205.6 MB (205644308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:156db67afd9468920a2bcff930e5c27047b7a7e28d1d95af8fd2c258e2e98dbb`  
		Last Modified: Fri, 05 Apr 2024 17:54:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
