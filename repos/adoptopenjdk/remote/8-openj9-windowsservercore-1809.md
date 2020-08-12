## `adoptopenjdk:8-openj9-windowsservercore-1809`

```console
$ docker pull adoptopenjdk@sha256:6a1c19dc7ef71a982ea2877fae64c813af7d5b440a0923783dbec527e16011ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1397; amd64

### `adoptopenjdk:8-openj9-windowsservercore-1809` - windows version 10.0.17763.1397; amd64

```console
$ docker pull adoptopenjdk@sha256:3aad190bb2235b68a15777dc9d5326335e6f108b353246d69e385ffd07f1cbf2
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2560878041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec1a8c0212e1f73d1cde16737a9096784e87ad35db1f4167470b67f432a9003e`
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
# Wed, 12 Aug 2020 17:10:28 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_x64_windows_openj9_8u262b10_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u262-b10_openj9-0.21.0/OpenJDK8U-jdk_x64_windows_openj9_8u262b10_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (824f32604bee0469d9dac5208dc8a025a142d95c53d838eab753bda619d46614) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '824f32604bee0469d9dac5208dc8a025a142d95c53d838eab753bda619d46614') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:10:29 GMT
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
	-	`sha256:4c7277b40ede8cff9445ae53f1ac1d19e36741c17926696ed0ae30d12613b4da`  
		Last Modified: Wed, 12 Aug 2020 18:06:20 GMT  
		Size: 225.0 MB (225007664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3d061a91f88d0ff73cf5ce1e5cc69652ded3f601fcdecf139d248097fbd8b97`  
		Last Modified: Wed, 12 Aug 2020 18:05:55 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
