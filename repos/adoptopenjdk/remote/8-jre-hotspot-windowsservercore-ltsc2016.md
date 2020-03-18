## `adoptopenjdk:8-jre-hotspot-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:bbd79aad798cb9ed0b352f8ea7eba04445d53baf832cb9abbe276ac8e1d70219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:8-jre-hotspot-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:fbed8627bc2b0135260c71d91574d2785d85d9c0553df7d8264c0af0261aeb15
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5807371714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:676be300020cf1b3dcdd02dece9adb3c5c62423b2357434efb9ec959f23b2378`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Mar 2020 14:10:21 GMT
ENV JAVA_VERSION=jdk8u242-b08
# Wed, 18 Mar 2020 14:15:03 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_x64_windows_hotspot_8u242b08.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u242-b08/OpenJDK8U-jre_x64_windows_hotspot_8u242b08.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (b1c486ca9fb9632bba9dd70778c7b371d5ee84cfbfaf6bd59a3e5cfd310a4f74) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'b1c486ca9fb9632bba9dd70778c7b371d5ee84cfbfaf6bd59a3e5cfd310a4f74') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a5d20b7a2294a0d2631f74f49fc34574484a692913559546ef0bceae789fd7a8`  
		Size: 1.7 GB (1658775203 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f08cc5bf7287bc1d8f72edfe2439c99210e433230a22fc73264fcf1685850ed2`  
		Last Modified: Fri, 13 Mar 2020 22:09:47 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c383ed6765cf597a8d53b8a7f30df1a6cc75eeb3219457f6c318cba46dbadbdb`  
		Last Modified: Wed, 18 Mar 2020 14:47:40 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:453fcb5079624fea0a50631d1f18f87bec485aa50046c0d747212b3014e407d2`  
		Last Modified: Wed, 18 Mar 2020 14:48:22 GMT  
		Size: 78.6 MB (78608338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
