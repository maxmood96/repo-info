## `eclipse-temurin:17-jdk-windowsservercore-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:4c338c960df196ef338a8fbbbe93cbd7eb0781c5d2e8fa67ce8dc869d1a505ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4171; amd64

### `eclipse-temurin:17-jdk-windowsservercore-ltsc2022` - windows version 10.0.20348.4171; amd64

```console
$ docker pull eclipse-temurin@sha256:f4b10e58b515136e9020eb8dd7d1d984da798d4d71d5e37ec734ef009c387dd5
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2637725770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb9e900a83da524395aae4cea476ea1c2d3b000a211d467add7a03025b230879`
-	Default Command: `["jshell"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 05 Sep 2025 13:15:05 GMT
RUN Install update 10.0.20348.4171
# Wed, 10 Sep 2025 20:20:13 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:50:52 GMT
ENV JAVA_VERSION=jdk-17.0.16+8
# Wed, 10 Sep 2025 21:51:13 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.16%2B8/OpenJDK17U-jdk_x64_windows_hotspot_17.0.16_8.msi ;     Write-Host ('Verifying sha256 (1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '1c3701f074d75036650731bcf6b08d69b1e3567bfa853f0ddd7aaba44da5b595') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-17' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:51:18 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'javac --version'; javac --version;     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
# Wed, 10 Sep 2025 21:51:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b109a50da182bf38f697ad080cf5640df286bdfc5e6a1f2f6b2002c48534385`  
		Last Modified: Tue, 09 Sep 2025 21:01:58 GMT  
		Size: 820.0 MB (819952539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe60f506e392727a189c473ed3077c57345b082b3f502c4e12299121d8a339`  
		Last Modified: Wed, 10 Sep 2025 21:43:44 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5e1a0aacfa3087c4adc722d3de332f32099f7a9e5b4d7b29fc761603bbc751`  
		Last Modified: Wed, 10 Sep 2025 21:51:47 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a01445a212fb798bf0b4c694bd90525bf623272f8ea656f23c19497ae053f99`  
		Last Modified: Wed, 10 Sep 2025 22:19:08 GMT  
		Size: 355.2 MB (355224901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03ce98c16c118fb7a4820703249dbe327204a0bf5fa4011213657f80a58931cf`  
		Last Modified: Wed, 10 Sep 2025 21:51:48 GMT  
		Size: 352.0 KB (351955 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e9d8ab4005e4a47d6ce9c4d9aadc5bde14db33fe058444beeacfb607b1ac26`  
		Last Modified: Wed, 10 Sep 2025 21:51:48 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
