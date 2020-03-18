## `adoptopenjdk:11-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:d2cfe24f7840a1fb8c46c9facd1ca6abeb2dbc715cb25745a53d62b0bbf25a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:11-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:3a96e75453567e36cf8e0397887b9197fbec915714b6037d17359bbfcc515021
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6118421489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb74c0c73341ab6c72284327248c3c3139cdf20a644bcd6cde55f5344e886101`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 10 Mar 2020 08:14:00 GMT
RUN Install update ltsc2016-amd64
# Fri, 13 Mar 2020 21:32:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 18 Mar 2020 14:32:54 GMT
ENV JAVA_VERSION=jdk-11.0.6+10_openj9-0.18.1
# Wed, 18 Mar 2020 14:36:20 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 18 Mar 2020 14:36:22 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 18 Mar 2020 14:36:23 GMT
CMD ["jshell"]
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
	-	`sha256:48cd618192d6c8179b658fb661c635e57bd8969a445014912cba82bdb32028c7`  
		Last Modified: Wed, 18 Mar 2020 14:52:25 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29b599ed9db5af78edeac9065f592dc32f0de70c3f61837071f736aa06ba5821`  
		Last Modified: Wed, 18 Mar 2020 14:53:01 GMT  
		Size: 389.7 MB (389655889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a07edd32093f7f64d78a50d4431dc350e24fc65253c1f8cc1b639fe8251f5b`  
		Last Modified: Wed, 18 Mar 2020 14:52:26 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f15eb044c41a1b549f28c6b8aeb722f3f9b04e40c1d3efcc9b3984af0fe97430`  
		Last Modified: Wed, 18 Mar 2020 14:52:25 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
