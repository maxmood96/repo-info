## `adoptopenjdk:11-jdk-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:a6210dd3c848f8c1f7ef99849e5558860fcd61e23ac05565e54ab2d14346c0d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3866; amd64

### `adoptopenjdk:11-jdk-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3866; amd64

```console
$ docker pull adoptopenjdk@sha256:934e548c5dd19208c4201d4915b9a1cc4829573f871c1c0c55ab32088e917283
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6117594388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb7518f9bac73bb920ae85ddfc9feb96ab45964def57c1b95fee22a14e6a013`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 05 Aug 2020 13:27:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 11 Aug 2020 20:31:19 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Aug 2020 17:14:47 GMT
ENV JAVA_VERSION=jdk-11.0.8+10_openj9-0.21.0
# Wed, 12 Aug 2020 17:17:56 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.8%2B10_openj9-0.21.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.8_10_openj9-0.21.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (7250326e5fad877da447bc1e37dfbfcaca18b10f1acc82ffc557a9421dc068bf) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '7250326e5fad877da447bc1e37dfbfcaca18b10f1acc82ffc557a9421dc068bf') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Aug 2020 17:17:56 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 12 Aug 2020 17:17:57 GMT
CMD ["jshell"]
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
	-	`sha256:d7889277f59967edb5ba02ce78be4d4e9da7d6faa849cbd85a8dd4b36292c1fa`  
		Last Modified: Wed, 12 Aug 2020 18:07:23 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5182aad89a58ca05f3b9f7fde987bf8d1cf6310c402ed50bdae27f541a9eb5c`  
		Last Modified: Wed, 12 Aug 2020 18:07:59 GMT  
		Size: 379.4 MB (379442333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca28b1f87c4fedb51c1a7fb4c752512d70a1d5a3db53adffc0761e84fe5e6d3e`  
		Last Modified: Wed, 12 Aug 2020 18:07:23 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2e82e895a9651e141f49387b77fa15b45d8fcf735a05d890958e9f12ec09108`  
		Last Modified: Wed, 12 Aug 2020 18:07:23 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
