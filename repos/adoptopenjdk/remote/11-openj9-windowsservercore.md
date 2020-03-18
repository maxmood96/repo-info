## `adoptopenjdk:11-openj9-windowsservercore`

```console
$ docker pull adoptopenjdk@sha256:3e1d65bfcbcaa8419eff8f38c01492101f58d5ff56a78647543448abd74aa7e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3568; amd64
	-	windows version 10.0.17763.1098; amd64
	-	windows version 10.0.14393.3568; amd64

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.14393.3568; amd64

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

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.17763.1098; amd64

```console
$ docker pull adoptopenjdk@sha256:0062d143e1dd1440b37745897fb27cf8b746ff05df65e6de4c7b0860965ad8f1
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2649810162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:546b9f49d253b2f743e561dc93ab181ab450a948d83f1ef4c190c8f538784be3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 06 Mar 2020 11:12:29 GMT
RUN Install update 1809-amd64
# Wed, 11 Mar 2020 00:42:10 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Mar 2020 16:00:06 GMT
ENV JAVA_VERSION=jdk-11.0.6+10_openj9-0.18.1
# Wed, 11 Mar 2020 16:03:08 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jdk_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '6297191f89d9905248c2f9b638ede5ed3dbc79eb9ac3587eb4139631479fa1ba') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 11 Mar 2020 16:03:10 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Wed, 11 Mar 2020 16:03:12 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:23645bd7ee0885911e1e2ab55ebcb36ce35795e1ceba9166ffd1b26dde18c3ee`  
		Size: 730.7 MB (730650958 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a7fab05ac5ad4b2f665ad71b5c08a81e82bff7ea2fdcbb66c14193d2dd268875`  
		Last Modified: Wed, 11 Mar 2020 01:16:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cecdcf8a677926825396a1aeec0ca6fc098b80ad6553e4fa3f94c0af16d41a1e`  
		Last Modified: Wed, 11 Mar 2020 16:19:21 GMT  
		Size: 1.2 KB (1189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb5df3ab1370c53dc3cf4959d7cc69b68db5f763c65af38cbfa02f65397c94ec`  
		Last Modified: Wed, 11 Mar 2020 16:20:23 GMT  
		Size: 384.5 MB (384469057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c6127bc95cd1d657a2e7e274024bff0fa7455213ff910b928c94737df97da72`  
		Last Modified: Wed, 11 Mar 2020 16:19:21 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693b728a10a6363a807393ff9b7ae222de802b68614826575c704b34da8bea5a`  
		Last Modified: Wed, 11 Mar 2020 16:19:21 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `adoptopenjdk:11-openj9-windowsservercore` - windows version 10.0.14393.3568; amd64

```console
$ docker pull adoptopenjdk@sha256:ae312b1b84c93a5dff419f489b2d2f20af792f5c85097a2793dfd16f37fb9059
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5804734224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:884f9c1282587cba0c0242c4129c9a7688c57bb035a0c474af3f62396a2387b2`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Wed, 18 Mar 2020 14:38:36 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jre_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.6%2B10_openj9-0.18.1/OpenJDK11U-jre_x64_windows_openj9_11.0.6_10_openj9-0.18.1.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (d3d6f7c320b4d2c1bc270cf85ef901395c74ef66562455ca51b48eb2cbff5380) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'd3d6f7c320b4d2c1bc270cf85ef901395c74ef66562455ca51b48eb2cbff5380') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Wed, 18 Mar 2020 14:38:37 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:8f40057eb9d277a322cfa72658d6be13ed87b97e969780a7d354f5ad7a3ecb72`  
		Last Modified: Wed, 18 Mar 2020 14:53:25 GMT  
		Size: 76.0 MB (75969787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba0e3ee99a49ceb1ec937dbf9373114354d7599a1407419eadeb1b47ae9af09`  
		Last Modified: Wed, 18 Mar 2020 14:53:15 GMT  
		Size: 1.1 KB (1115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
