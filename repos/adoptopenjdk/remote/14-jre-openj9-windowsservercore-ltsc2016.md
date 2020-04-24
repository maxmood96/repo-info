## `adoptopenjdk:14-jre-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:0be25bc6e442dc4a1adfbbd61f3987d5ebf6d12fb40f3ca2b6c4672a0d969eb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `adoptopenjdk:14-jre-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull adoptopenjdk@sha256:2edf4111552a337fd41810371ffd0f47901873cd1c8c7b95f0f3097b1e2f86ad
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5819775790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdbbad56af2adab2e2b720b11e8a21ac30b598d0e16ad9ce0fd1444c09a05b8d`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 24 Apr 2020 21:01:53 GMT
ENV JAVA_VERSION=jdk-14.0.1+7.1_openj9-0.20.0
# Fri, 24 Apr 2020 21:10:16 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7.1_openj9-0.20.0/OpenJDK14U-jre_x64_windows_openj9_14.0.1_7_openj9-0.20.0.msi ...');         [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;         wget https://github.com/AdoptOpenJDK/openjdk14-binaries/releases/download/jdk-14.0.1%2B7.1_openj9-0.20.0/OpenJDK14U-jre_x64_windows_openj9_14.0.1_7_openj9-0.20.0.msi -O 'openjdk.msi';         Write-Host ('Verifying sha256 (caaccca7154504a800facd99210d6a5094aa548ba8b9e40374d4934770edd224) ...');         if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'caaccca7154504a800facd99210d6a5094aa548ba8b9e40374d4934770edd224') {                 Write-Host 'FAILED!';                 exit 1;         };                 New-Item -ItemType Directory -Path C:\temp | Out-Null;                 Write-Host 'Installing using MSI ...';         Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',         '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;         Write-Host 'Removing openjdk.msi ...';         Remove-Item openjdk.msi -Force;         Remove-Item -Path C:\temp -Recurse | Out-Null;
# Fri, 24 Apr 2020 21:10:17 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+UseContainerSupport -XX:+IdleTuningCompactOnIdle -XX:+IdleTuningGcOnIdle
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
	-	`sha256:59500d59a067c650e1d0031bb607c14e7c9fcb1b7e4a5bbf352bc4de1a27cf22`  
		Last Modified: Fri, 24 Apr 2020 21:28:45 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26238029a9947260ef2e545663c6d3ea1beebbd602c062524b7300a63c23993a`  
		Last Modified: Fri, 24 Apr 2020 21:30:47 GMT  
		Size: 91.7 MB (91704799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d181fc6cef0e11b666d1d267cbe5dd017379706aff4c6a4fc7e768423c3bb`  
		Last Modified: Fri, 24 Apr 2020 21:30:32 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
