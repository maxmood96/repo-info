## `eclipse-temurin:20-jdk-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:8d6b6134d88bc98e3ad1af2f568befa72b7978f0f350c60dfc84e341532f62c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1850; amd64
	-	windows version 10.0.17763.4645; amd64

### `eclipse-temurin:20-jdk-windowsservercore` - windows version 10.0.20348.1850; amd64

```console
$ docker pull eclipse-temurin@sha256:0cfe8aafdbd1385e8c9e2882572c264e8043599b822d6113f1b24cd57f92e5f5
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2107261563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3eeb9ca34e62ade50d1770b0b97c098d34bade3a087560f75b1bc5a3bc3fa63`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 07 Jul 2023 21:29:32 GMT
RUN Install update 10.0.20348.1850
# Thu, 13 Jul 2023 20:29:18 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Jul 2023 22:01:16 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 13 Jul 2023 22:02:14 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_windows_hotspot_20.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_windows_hotspot_20.0.1_9.msi ;     Write-Host ('Verifying sha256 (8cd9abe9b188ef11f976c854e181c932c84aa15a44b94144e4b472990764229c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8cd9abe9b188ef11f976c854e181c932c84aa15a44b94144e4b472990764229c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Jul 2023 22:02:36 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 13 Jul 2023 22:02:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c84a7416e1317a892f4786a89c62493b21df55e0e06b82a4bb007cc79df0f949`  
		Last Modified: Tue, 11 Jul 2023 18:03:32 GMT  
		Size: 348.8 MB (348766456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e3828ab9c4326158b6161915d8bad87619b3107529ab32863eb31b684d127`  
		Last Modified: Thu, 13 Jul 2023 21:07:36 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49811356fad22212e54ecd48d2e7bf4674062e70c2e5a929e5cea432c3b59366`  
		Last Modified: Thu, 13 Jul 2023 22:25:40 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4507d2f51e50d7c87ea8003b510e7286e889d19672c967cba32a4d22a677635f`  
		Last Modified: Thu, 13 Jul 2023 22:26:08 GMT  
		Size: 369.6 MB (369614571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f1456bafdc72e1a3b7df6b16e995e10893c95152965c30613430c33037decd`  
		Last Modified: Thu, 13 Jul 2023 22:25:41 GMT  
		Size: 277.7 KB (277695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff04516ec701b81f4740f88e070dcf4a423174445af479b7e2d0035dd0ce3dd`  
		Last Modified: Thu, 13 Jul 2023 22:25:40 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:20-jdk-windowsservercore` - windows version 10.0.17763.4645; amd64

```console
$ docker pull eclipse-temurin@sha256:c4016c632be1063c3fe84b6b39d911f59845c49fb2328af74c0e2384e8d2ed3d
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2313213594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f48a98bb3c30b67469afaa0f27bb838f3b31dbd7f40e9d59dfdbc7a7133cbfd`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Fri, 07 Jul 2023 08:17:39 GMT
RUN Install update 10.0.17763.4645
# Thu, 13 Jul 2023 20:32:48 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 13 Jul 2023 22:02:44 GMT
ENV JAVA_VERSION=jdk-20.0.1+9
# Thu, 13 Jul 2023 22:04:21 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_windows_hotspot_20.0.1_9.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.1%2B9/OpenJDK20U-jdk_x64_windows_hotspot_20.0.1_9.msi ;     Write-Host ('Verifying sha256 (8cd9abe9b188ef11f976c854e181c932c84aa15a44b94144e4b472990764229c) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '8cd9abe9b188ef11f976c854e181c932c84aa15a44b94144e4b472990764229c') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-20' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 13 Jul 2023 22:05:25 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 13 Jul 2023 22:05:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e36dba1ee29cd36713c8785a5de7dd2a487244d734ed4c5e7b0a6890bffb806e`  
		Last Modified: Tue, 11 Jul 2023 18:27:38 GMT  
		Size: 289.1 MB (289068746 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e991bb72ebb8bf12a5cb5fcb2075d938e3508db6634bdfe6a5bb73e4c612051`  
		Last Modified: Thu, 13 Jul 2023 21:08:51 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0136ff96e8ae19a8cb717c15b5c664c7b16b5f92ef5e714fe1db4c63c08e114e`  
		Last Modified: Thu, 13 Jul 2023 22:26:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54cc1d4b5534e2bb85a13fbbb40381f9cdd2be3f0e4baf7fb6fd89e6f96fbe8`  
		Last Modified: Thu, 13 Jul 2023 22:26:49 GMT  
		Size: 369.6 MB (369630701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2bd0dff2f8d8cbb801af1488e0f0b47f408db6ec3a24fb11863ca45f9351f81`  
		Last Modified: Thu, 13 Jul 2023 22:26:21 GMT  
		Size: 3.9 MB (3889713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204f8d54fbaf52291e0e3c1944fcadf7181050e258fff1bb5c3b271afb2c5b31`  
		Last Modified: Thu, 13 Jul 2023 22:26:19 GMT  
		Size: 1.4 KB (1442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
