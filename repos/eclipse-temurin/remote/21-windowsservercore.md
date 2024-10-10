## `eclipse-temurin:21-windowsservercore`

```console
$ docker pull eclipse-temurin@sha256:f3d2d7950ea6b3fdd93a84e1c2876670080e0336cbe6196225adde20116c5541
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2762; amd64
	-	windows version 10.0.17763.6414; amd64

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.20348.2762; amd64

```console
$ docker pull eclipse-temurin@sha256:1478198a58ee32888c649086b105fb76f385346d5b82f8c3102f2117cb5abbcd
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2178633845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdcf30059dbc9db94e9bd4364a886023194eeb83799f9b5a6ed8b3e927da5779`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 06 Oct 2024 04:56:48 GMT
RUN Install update 10.0.20348.2762
# Wed, 09 Oct 2024 23:33:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:56:45 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 09 Oct 2024 23:57:42 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.4_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.4_7.msi ;     Write-Host ('Verifying sha256 (5eadbdeabdca1a7abf6416a6b35bf7afd86e7edade7b5d44059fbcecacaef372) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5eadbdeabdca1a7abf6416a6b35bf7afd86e7edade7b5d44059fbcecacaef372') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 09 Oct 2024 23:58:05 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 09 Oct 2024 23:58:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3445b497121718058765c341117a0c1522c51cd65bec8c517981a745ff91f0bf`  
		Last Modified: Tue, 08 Oct 2024 17:56:28 GMT  
		Size: 337.1 MB (337149137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6dd7a167e5d8024c2db3283a385811103c47c1e1349528ae29d41d1aa3117ae`  
		Last Modified: Thu, 10 Oct 2024 00:18:53 GMT  
		Size: 1.4 KB (1416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75a887a2a966ca16312c98c9e88eec4617cd8b1fb41854a62813f9e7ba205c28`  
		Last Modified: Thu, 10 Oct 2024 00:27:53 GMT  
		Size: 1.4 KB (1411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:277a550185d8c13467c5dc841b681a987005e531833d14d898ee568c8e79a825`  
		Last Modified: Thu, 10 Oct 2024 00:28:20 GMT  
		Size: 379.0 MB (379022516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9656888281e3df851c0981e727223af7ac7ae9e24030018b5863d8059bd442`  
		Last Modified: Thu, 10 Oct 2024 00:27:53 GMT  
		Size: 265.6 KB (265593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30e9f636e6a6d091f1f8d1bd7366f4200bae1052a9a8b45a6c5469eec44fdcbd`  
		Last Modified: Thu, 10 Oct 2024 00:27:53 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21-windowsservercore` - windows version 10.0.17763.6414; amd64

```console
$ docker pull eclipse-temurin@sha256:d9ff0b4c414e676c38f95003e828a3e4ae53b2dc016680ac660b7401e36343bb
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2284872315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc07cc751070ea22f127d805578ec11c596260ac807eb7d56768432bcc48af82`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 04 Oct 2024 21:48:44 GMT
RUN Install update 10.0.17763.6414
# Wed, 09 Oct 2024 23:35:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Oct 2024 23:58:13 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Wed, 09 Oct 2024 23:59:34 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.4_7.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_windows_hotspot_21.0.4_7.msi ;     Write-Host ('Verifying sha256 (5eadbdeabdca1a7abf6416a6b35bf7afd86e7edade7b5d44059fbcecacaef372) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '5eadbdeabdca1a7abf6416a6b35bf7afd86e7edade7b5d44059fbcecacaef372') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-21' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Thu, 10 Oct 2024 00:00:11 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Thu, 10 Oct 2024 00:00:11 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eec1ab8e4a3936959c2381d3aaa9aaf9caf01f82fb701f2b4c3cc3dbf6d035dd`  
		Last Modified: Tue, 08 Oct 2024 17:36:07 GMT  
		Size: 181.6 MB (181556913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71416d65806874920ade48cad9fe9e847b67ca207c59353ff136f87da9c117ce`  
		Last Modified: Thu, 10 Oct 2024 00:19:58 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc751f056192cff9f7bfd4fbf85ed9b28a75d2f9d7f9d5361e9729cc14189be4`  
		Last Modified: Thu, 10 Oct 2024 00:28:30 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d1f0edc16ba0433e9b9b48904a3d18019925f90ae8277032f04117818a6f82`  
		Last Modified: Thu, 10 Oct 2024 00:28:56 GMT  
		Size: 379.0 MB (379040868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d926a71c44908ce51fbb9fefd18b37da7f64cb6e8085aa69dfa60440ae49117e`  
		Last Modified: Thu, 10 Oct 2024 00:28:31 GMT  
		Size: 4.0 MB (4001932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ffba8f3bb40dc1b4545bde5496c2b12c482114e20e02077b64dcf0568889d8`  
		Last Modified: Thu, 10 Oct 2024 00:28:30 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
