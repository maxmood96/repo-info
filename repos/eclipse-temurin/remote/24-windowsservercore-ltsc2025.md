## `eclipse-temurin:24-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d2f8ac8cf768ac977be4998e7ea403af980ac3519d1197d06afd32551f44f3ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.4652; amd64

### `eclipse-temurin:24-windowsservercore-ltsc2025` - windows version 10.0.26100.4652; amd64

```console
$ docker pull eclipse-temurin@sha256:f5660d73033942a14c1803d747e68538deec0c10539081af9965ec9be7f33aad
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.7 GB (3744119300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5125f71e3bca8d00400c83a0ba96c2c36f7af7771a49e68198cade81b1fdbbc8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 05 Jul 2025 18:40:54 GMT
RUN Install update 10.0.26100.4652
# Wed, 09 Jul 2025 18:08:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jul 2025 18:09:00 GMT
ENV JAVA_VERSION=jdk-24.0.1+9
# Wed, 09 Jul 2025 18:09:20 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin24-binaries/releases/download/jdk-24.0.1%2B9/OpenJDK24U-jdk_x64_windows_hotspot_24.0.1_9.msi ;     Write-Host ('Verifying sha256 (c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne 'c820fd88f666dbb56109095a7a82ce82ebc0aedb0a0d6d1dd9f75fe2b7ac0eb0') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-24' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Jul 2025 18:09:28 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Jul 2025 18:09:29 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ebc78effce2335b8fe04c34f5f1f3e33e513d5a7831fa81718af6737b3d654`  
		Last Modified: Wed, 09 Jul 2025 19:09:08 GMT  
		Size: 1.3 GB (1275866158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48c29d016e265eea15a39f3d9cb6e3a50e9752c2fc93bb882b9edb4dd075828a`  
		Last Modified: Wed, 09 Jul 2025 19:08:50 GMT  
		Size: 1.3 KB (1346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78472807ecdad05d0b17e14c1fd6c1e05e7a66d720f611acb3a252cb8282a55a`  
		Last Modified: Wed, 09 Jul 2025 19:08:52 GMT  
		Size: 1.3 KB (1309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5239567bd81a1ca481027ee89311b97d982d77090c9e98e9f52f912c2146cded`  
		Last Modified: Wed, 09 Jul 2025 19:09:00 GMT  
		Size: 252.6 MB (252569037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d469389c60d1dbfcbbc14f01d8e4ab8beb1ecb44620172daac127c03c105051`  
		Last Modified: Wed, 09 Jul 2025 19:09:20 GMT  
		Size: 373.0 KB (372986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd1be30f1528e180598acb0f0b37248608dc0794ec5a46518209e128419986c3`  
		Last Modified: Wed, 09 Jul 2025 19:09:20 GMT  
		Size: 1.4 KB (1354 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
