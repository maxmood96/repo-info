## `openjdk:27-ea-24-jdk-windowsservercore-ltsc2022`

```console
$ docker pull openjdk@sha256:3790ddeaf980b3bba51bab0232e89d38095029e0fb56292c5cd3ccf2ce991142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-24-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:7dbf28a482faed0c5a55339770e70fb131e21761407663d06fd0c539597c2ba2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2346617785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46208cefe0d736015511075b5cfde1683a8c4f294d8ae51183708af1c92ed42b`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Thu, 07 May 2026 03:49:54 GMT
RUN Install update 10.0.20348.5139
# Tue, 02 Jun 2026 07:23:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 02 Jun 2026 07:24:39 GMT
RUN Write-Host 'Enabling TLS 1.2 (https://githubengineering.com/crypto-removal-notice/) ...'; 	$tls12RegBase = 'HKLM:\\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2'; 	if (Test-Path $tls12RegBase) { throw ('"{0}" already exists!' -f $tls12RegBase) }; 	New-Item -Path ('{0}/Client' -f $tls12RegBase) -Force; 	New-Item -Path ('{0}/Server' -f $tls12RegBase) -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Client' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'DisabledByDefault' -PropertyType DWORD -Value 0 -Force; 	New-ItemProperty -Path ('{0}/Server' -f $tls12RegBase) -Name 'Enabled' -PropertyType DWORD -Value 1 -Force; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:24:39 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 02 Jun 2026 07:24:48 GMT
RUN $newPath = ('{0}\bin;{1}' -f $env:JAVA_HOME, $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	setx /M PATH $newPath; 	Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:24:48 GMT
ENV JAVA_VERSION=27-ea+24
# Tue, 02 Jun 2026 07:24:49 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/jdk27/24/GPL/openjdk-27-ea+24_windows-x64_bin.zip
# Tue, 02 Jun 2026 07:24:51 GMT
ENV JAVA_SHA256=5bbf96e8f91e2c80680961ba7cc2ddb7112131f6fa000d2472ab2ea6c99a06f7
# Tue, 02 Jun 2026 07:26:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:JAVA_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:JAVA_URL -OutFile 'openjdk.zip'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:JAVA_SHA256); 	if ((Get-FileHash openjdk.zip -Algorithm sha256).Hash -ne $env:JAVA_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	New-Item -ItemType Directory -Path C:\temp | Out-Null; 	Expand-Archive openjdk.zip -DestinationPath C:\temp; 	Move-Item -Path C:\temp\* -Destination $env:JAVA_HOME; 	Remove-Item C:\temp; 		Write-Host 'Removing ...'; 	Remove-Item openjdk.zip -Force; 		Write-Host 'Verifying install ...'; 	Write-Host '  javac --version'; javac --version; 	Write-Host '  java --version'; java --version; 		Write-Host 'Complete.'
# Tue, 02 Jun 2026 07:26:54 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857865ad3eca4da109d969134a9cab7225d9de49597914ae325d43661900f513`  
		Last Modified: Tue, 12 May 2026 17:34:16 GMT  
		Size: 633.4 MB (633401492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64818880469c46e82ad7a13b32c2ce7ca26a75a57f681c722c786d77ae355989`  
		Last Modified: Tue, 02 Jun 2026 07:27:07 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f53d4dc39f0640e55c3246822ffcb42aafcc08ad3a3eb7629646b3bd522d73fe`  
		Last Modified: Tue, 02 Jun 2026 07:27:08 GMT  
		Size: 496.7 KB (496678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144ebb81ce7ea3e28ce5b655bc8f39163f288ae22b1141bd8ae67d3c667b981d`  
		Last Modified: Tue, 02 Jun 2026 07:27:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c7e3f786aa934c6e5c7de54c20ee4ec0ea0e9b26e7879f69c4d45154f3f2564`  
		Last Modified: Tue, 02 Jun 2026 07:27:07 GMT  
		Size: 306.8 KB (306777 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b661042879ba25b28496c7bd43a136631ccf4ac8c0229877c3927199465c4ec1`  
		Last Modified: Tue, 02 Jun 2026 07:27:05 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cd8e6b2dd3744242ef2e0ff3a064f3dbf4b01ede0ead6f6a02094e263ee0b9`  
		Last Modified: Tue, 02 Jun 2026 07:27:06 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f8a72306f096bdad2e5f21cdb529f265a94f9f1fdd78b0ab5e0fba81941c330`  
		Last Modified: Tue, 02 Jun 2026 07:27:06 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:253fe32c239c42008c8466a0b99de8b9a51b8e76427658d9e8fd5bfd59f76dd0`  
		Last Modified: Tue, 02 Jun 2026 07:27:21 GMT  
		Size: 223.4 MB (223385898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3981e2a59ead14b875308e79ce71201777cdf7a971f454ef5fede776a77129`  
		Last Modified: Tue, 02 Jun 2026 07:27:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
