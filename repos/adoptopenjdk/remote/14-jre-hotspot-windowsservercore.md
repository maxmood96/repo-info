## `adoptopenjdk:14-jre-hotspot-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:101e8c8df10f034988237c492855e8d0eb0b1176800e469fba8b5557a20c618f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:14-jre-hotspot-windowsservercore` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:729f0110476393af5abbb0c43e107efda4c58289c0fbab01d1357b05fa59850e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5841343949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c03b23804759918f6bc99c3c09fb660fa17acff38397d9245a8a34a6054776c`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:55:28 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Wed, 12 Aug 2020 17:03:45 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jre_x64_windows_hotspot_14.0.2_12.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jre_x64_windows_hotspot_14.0.2_12.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (bf468c78387b8095914a2d46af6961d5c22697929b66961e346a41fc8bf909d4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bf468c78387b8095914a2d46af6961d5c22697929b66961e346a41fc8bf909d4') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:18c978e1ac9975ef8ef38080b6f67b130c8a22752931908c388958d905e0b016`  
		Last Modified: Wed, 12 Aug 2020 18:01:47 GMT  
		Size: 1.1 KB (1122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b34872a4a77c0ebb825847498cda245ff4f220a51ae4d829e9075ad5b0735244`  
		Last Modified: Wed, 12 Aug 2020 18:04:32 GMT  
		Size: 103.2 MB (103194244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:14-jre-hotspot-windowsservercore` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:5aef9a37cbfdb8b521c0830679abfbd272482069f0944a46c15a925c537fdc08
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2438390468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a50bfd6a0dd134c3a60e3256694d0bf179928ce74bb043e1e8df9c42b7a21735`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 06 Aug 2020 16:53:49 GMT
RUN Install update 1809-amd64
# Tue, 11 Aug 2020 20:36:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 16:58:54 GMT
ENV JAVA_VERSION=jdk-14.0.2+12
# Wed, 12 Aug 2020 17:05:14 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jre_x64_windows_hotspot_14.0.2_12.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.2%2B12/OpenJDK14U-jre_x64_windows_hotspot_14.0.2_12.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (bf468c78387b8095914a2d46af6961d5c22697929b66961e346a41fc8bf909d4) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'bf468c78387b8095914a2d46af6961d5c22697929b66961e346a41fc8bf909d4') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
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
	-	`sha256:8819af825e098fdf494065c262fe675b42e36a3d26aaf6c1fa8e462b2dd370fb`  
		Last Modified: Wed, 12 Aug 2020 18:03:03 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30ab3476a850c05bb29e095fb8a11e92168e0c6f599be7d50de6da130ea22eac`  
		Last Modified: Wed, 12 Aug 2020 18:05:00 GMT  
		Size: 102.5 MB (102521195 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
