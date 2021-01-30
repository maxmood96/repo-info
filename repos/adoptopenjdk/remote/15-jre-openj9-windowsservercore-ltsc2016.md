## `adoptopenjdk:15-jre-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:ee8f26f16642fb833867ebdb02ba960b844fe9c400b94c52a6a8ddb9722e0d5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:15-jre-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:6db1b7dbdb23793a10cbee14c4a5872c767d00cc0d1b5a492be334213e692a80
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5889441905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a36ebccc75c943057ad95edb6f0efd7b3164e5541c0036da86b152666cd1d2e7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Sat, 30 Jan 2021 02:04:18 GMT
ENV JAVA_VERSION=jdk-15.0.2+7_openj9-0.24.0
# Sat, 30 Jan 2021 02:11:16 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jre_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jre_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (8c3899f4f3dfbad444742b00276fd5ce53cdc8c4facb586cdab1834a41c1b71d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8c3899f4f3dfbad444742b00276fd5ce53cdc8c4facb586cdab1834a41c1b71d') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 02:11:18 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c2be906f776ed59fdfafac6768f82759614ab4bbda81368ebfd882633145fbb`  
		Last Modified: Sat, 30 Jan 2021 02:51:53 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07fe4a5fc396838b6a90d89178541605377da084d80626b6ffeaefd361c0fbeb`  
		Last Modified: Sat, 30 Jan 2021 03:01:44 GMT  
		Size: 95.5 MB (95544084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a6c43e1b375888c3e8ad647ea768ea44a74de17ae718b6d9fafc903dfa0f504`  
		Last Modified: Sat, 30 Jan 2021 03:01:31 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
