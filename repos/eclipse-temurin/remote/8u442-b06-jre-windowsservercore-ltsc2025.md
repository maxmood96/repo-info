## `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d2af4806660e981a96da02c1dae6441e03889d8983244e1e256054b7ebdafffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3194; amd64

### `eclipse-temurin:8u442-b06-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.3194; amd64

```console
$ docker pull eclipse-temurin@sha256:527447ab0b16b8b8447eae274abbd2bf9295f0f2f5d81a9ed3a73eabd7483ea1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 GB (2889769596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4316b0392867c3bba92f10d8ae9d2a0e264edd35cf1b4dde42a5f396848216b`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 08 Feb 2025 22:54:28 GMT
RUN Install update 10.0.26100.3194
# Thu, 27 Feb 2025 18:20:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 27 Feb 2025 18:20:40 GMT
ENV JAVA_VERSION=jdk8u442-b06
# Thu, 27 Feb 2025 18:20:54 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u442-b06/OpenJDK8U-jre_x64_windows_hotspot_8u442b06.msi ;     Write-Host ('Verifying sha256 (4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '4dd03622b9690427dbcd6df6c60eb6e1a422f1eb7389f0d08ef844bf43e23eab') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 27 Feb 2025 18:21:02 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39ec821b2720b751c1158ef60a69ee9d879169daea9bb3099c4f6c525fc30ff3`  
		Last Modified: Tue, 11 Feb 2025 19:01:39 GMT  
		Size: 601.3 MB (601280394 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6afd09e33c0ddff90775a82e64e7d3256b0fe9428eb5ba172daab70e7189a0`  
		Last Modified: Thu, 27 Feb 2025 18:21:06 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d8be9241c7446a843c6dbe125863edb7963d0bf3bf8c4f4a2b8f2acec2226e`  
		Last Modified: Thu, 27 Feb 2025 18:21:06 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:865e7a886be99eb13b9338cd33c480f750bd2ae5676931d792e3b46c775e40aa`  
		Last Modified: Thu, 27 Feb 2025 18:21:11 GMT  
		Size: 72.8 MB (72786288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:befbfa12188b68c7a0524790d203f25df09e3965c3bf3c32da0fecde88929d7c`  
		Last Modified: Thu, 27 Feb 2025 18:21:07 GMT  
		Size: 393.1 KB (393143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
