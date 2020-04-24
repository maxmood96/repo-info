## `adoptopenjdk:11-jdk-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:667f6b6eb1eedf321b5f9519dd59938b6b4407664fed04cd509f5db58e24a847
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `adoptopenjdk:11-jdk-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull adoptopenjdk@sha256:dfde893c8d33f8a3d81517534d045bd93566c4701612e809ce5638606db09015
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 GB (6106211142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ca14c740c1aa69fff40bd608f5a92d638944ed12d28835e27e2e64f2eff6eb7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Apr 2020 20:51:48 GMT
ENV JAVA_VERSION=jdk-11.0.7+10.1_openj9-0.20.0
# Fri, 24 Apr 2020 20:55:02 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.7%2B10.1_openj9-0.20.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.7_10_openj9-0.20.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.7%2B10.1_openj9-0.20.0/OpenJDK11U-jdk_x64_windows_openj9_11.0.7_10_openj9-0.20.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (386e33d5b3bb9ed01b3b96e4d68933cc50d87deca7cfbdc8d360929340de16d5) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '386e33d5b3bb9ed01b3b96e4d68933cc50d87deca7cfbdc8d360929340de16d5') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Fri, 24 Apr 2020 20:55:03 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
# Fri, 24 Apr 2020 20:55:04 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:920ecb876e9daf059c0657ad46a7f3ab65b3360b8d551f9efef8a70791d4205a`  
		Last Modified: Fri, 24 Apr 2020 21:26:21 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7a719dc8bf2ea40664c4b952a5f90d78f70a007b7ba78d516cf10b125ef22aa`  
		Last Modified: Fri, 24 Apr 2020 21:26:50 GMT  
		Size: 378.1 MB (378138896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3e8b902cc598ed876de3d2bdcde1b12e30f0a120748827cc630d9480336a29`  
		Last Modified: Fri, 24 Apr 2020 21:26:21 GMT  
		Size: 1.2 KB (1193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e42ae39015ab902093c4c55bcec67a09b0a8dbabd966bf9ff19920108437398`  
		Last Modified: Fri, 24 Apr 2020 21:26:21 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
