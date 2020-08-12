## `adoptopenjdk:8u262-b10-jre-openj9-0.21.0-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:5b9c7562167b4f3016f7e2ca6fdf5fb1ff2528da7404a54b26e68be76fbe3a9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:8u262-b10-jre-openj9-0.21.0-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:f6cce74e80e4c2bc49eb5136c4d6672f5f6eccbeb34ce3294fef007002c2bc1b
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5835475168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3186ec7b6af47b298d9aa212ee1f0741f9580166ed7a748623a7ebc9fb4a0d1`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:05:31 GMT
ENV JAVA_VERSION=jdk8u262-b10_openj9-0.21.0
# Wed, 12 Aug 2020 17:12:53 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jre_x64_windows_openj9_8u262b10_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jre_x64_windows_openj9_8u262b10_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (cfa3f17ea264303f1bea55391a10ce9fcfceff2653161c00fd96f84f2e7dcf63) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cfa3f17ea264303f1bea55391a10ce9fcfceff2653161c00fd96f84f2e7dcf63') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:12:54 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b2151f69990007e1df0a2a0a68997c72a9ce7546d653d17a482a51cc3323c047`  
		Size: 1.7 GB (1668161535 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:32838d9637dc39d4acee78700b0f93d6c8c9d2db755f12c8009c1b51687d3fbd`  
		Last Modified: Tue, 11 Aug 2020 20:54:28 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98ef846da4ab4a0aa8371acbe19593de59dfdb23a25abd9bc99cedb8f1b4dcf1`  
		Last Modified: Wed, 12 Aug 2020 18:05:16 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f19b8c0ce1c98c18ff2d7a8b47c199b94f527e845d10c9a5b10759ee8a866a`  
		Last Modified: Wed, 12 Aug 2020 18:06:50 GMT  
		Size: 97.3 MB (97324292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4257638fddbd6b774aafbc280540045d3915a83d73595aaa379210c1b1feaa53`  
		Last Modified: Wed, 12 Aug 2020 18:06:33 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:8u262-b10-jre-openj9-0.21.0-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:d52620fe8e858f2491fdba5a3f513b461150394ac3a6fd04ab58793554dd3cd2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2432518509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:103fc318c988e53233b153201692af06416cfc6a6b457d2d0fccaa4c99138f03`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:08:28 GMT
ENV JAVA_VERSION=jdk8u262-b10_openj9-0.21.0
# Wed, 12 Aug 2020 17:14:30 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jre_x64_windows_openj9_8u262b10_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jre_x64_windows_openj9_8u262b10_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (cfa3f17ea264303f1bea55391a10ce9fcfceff2653161c00fd96f84f2e7dcf63) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'cfa3f17ea264303f1bea55391a10ce9fcfceff2653161c00fd96f84f2e7dcf63') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:14:31 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3ab49687905cb6183025d5ec648fe62fb3d7039a9cf1fe09ef94a62d89d219db`  
		Size: 617.5 MB (617534122 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:43065500f09f35124a5d71517aa493fd23ad75660682600f7f6b40aa7629ac78`  
		Last Modified: Tue, 11 Aug 2020 20:54:54 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2be8725ae4e9a146bbed1d87133662a2d7134812d8d2b6601df69074722d925`  
		Last Modified: Wed, 12 Aug 2020 18:05:56 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7a211e1217948178100f0d0a35d3d8596b0c46584f9018a87d573562bd1ff0`  
		Last Modified: Wed, 12 Aug 2020 18:07:13 GMT  
		Size: 96.6 MB (96648129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee29eb0bd17ec3f5b3785d292736347f4851c8972535f61cd4283486b931caf9`  
		Last Modified: Wed, 12 Aug 2020 18:07:00 GMT  
		Size: 1.1 KB (1131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
