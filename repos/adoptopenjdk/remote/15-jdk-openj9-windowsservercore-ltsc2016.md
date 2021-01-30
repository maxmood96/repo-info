## `adoptopenjdk:15-jdk-openj9-windowsservercore-ltsc2016`

```console
$ docker pull adoptopenjdk@sha256:801a58d55ec7a0ceceae43e82641ae64448d853422e9c3c107990b1fcec0b15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `adoptopenjdk:15-jdk-openj9-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull adoptopenjdk@sha256:62a62600b76bccec3f22cc263199cbdb879561e0c30207f0c15a6de2e9eb936e
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 GB (6177574400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19e7197048791a86b4e8a9de0c695bfddee56ae6377c98aa959ff5687a9fe5a`
-	Default Command: `["jshell"]`
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
# Sat, 30 Jan 2021 02:07:27 GMT
RUN Write-Host ('Downloading https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jdk_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi ...');     [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12;     wget https://github.com/AdoptOpenJDK/openjdk15-binaries/releases/download/jdk-15.0.2%2B7_openj9-0.24.0/OpenJDK15U-jdk_x64_windows_openj9_15.0.2_7_openj9-0.24.0.msi -O 'openjdk.msi';     Write-Host ('Verifying sha256 (f366ebd9f9b4243a86bbf72975f9357a7fa6aec5dac40af4edd4c97ddb4d28b8) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'f366ebd9f9b4243a86bbf72975f9357a7fa6aec5dac40af4edd4c97ddb4d28b8') {             Write-Host 'FAILED!';             exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome' -Wait -Passthru;     Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Sat, 30 Jan 2021 02:07:29 GMT
ENV JAVA_TOOL_OPTIONS=-XX:+IgnoreUnrecognizedVMOptions -XX:+IdleTuningGcOnIdle
# Sat, 30 Jan 2021 02:07:31 GMT
CMD ["jshell"]
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
	-	`sha256:a74eb3060812510a9cdc3af164443f417b1ecc62efcf42985ac7ce32cd042227`  
		Last Modified: Sat, 30 Jan 2021 02:59:17 GMT  
		Size: 383.7 MB (383675097 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e0975346fa55611bedbc0bbfc997fc289576db2ed2a521479c9e521efa1637`  
		Last Modified: Sat, 30 Jan 2021 02:51:54 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16b27c1a6cd1f7f06e006bcdfb64a4c1644cc9dda4b668402b4dbc015d474601`  
		Last Modified: Sat, 30 Jan 2021 02:51:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
