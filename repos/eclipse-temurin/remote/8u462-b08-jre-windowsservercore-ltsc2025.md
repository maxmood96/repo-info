## `eclipse-temurin:8u462-b08-jre-windowsservercore-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:d1ac37bdf8e88d20c6a984e612bae2a96bba4d4292b7f40d51f2ed136a3f7835
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6584; amd64

### `eclipse-temurin:8u462-b08-jre-windowsservercore-ltsc2025` - windows version 10.0.26100.6584; amd64

```console
$ docker pull eclipse-temurin@sha256:4f3d7017489425b27995acb9860076f520dd03f9f42f91f9174e6f487d81baf6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 GB (3644454332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:224ddeff818ad78684ed68571f7d70c4b6ed2f65f300e5888948a236293ea080`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 06 Sep 2025 02:36:14 GMT
RUN Install update 10.0.26100.6584
# Wed, 10 Sep 2025 21:49:23 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Sep 2025 21:49:23 GMT
ENV JAVA_VERSION=jdk8u462-b08
# Wed, 10 Sep 2025 21:49:46 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u462-b08/OpenJDK8U-jre_x64_windows_hotspot_8u462b08.msi ;     Write-Host ('Verifying sha256 (22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '22a64b7531443577dd70eb244c943111121180dbf20a6a867452ed6da99b556d') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-8' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 10 Sep 2025 21:49:53 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java -version'; java -version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e9750fac680d8e6b6c2e0a6f7718b1ccb76f68a6ebd9f9da4c5e470458c7e72`  
		Last Modified: Wed, 10 Sep 2025 08:38:21 GMT  
		Size: 1.4 GB (1356132583 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c39bf991b65b005f2b7f122bb8e11deadf02225b06438805e32f109fda66c1ea`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb586cde9fe79b148e95e71b779ad680dcc362288a7fdb752668a7c966c3c71e`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9a2bbff228707fa4e67a4db24ae4b13db653c1623c922995c7709ba7ecede30`  
		Last Modified: Wed, 10 Sep 2025 21:57:10 GMT  
		Size: 72.6 MB (72649119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da555e552108fcf8055d96f5fceb0875964bef88a56af7c5115c67a45b58a2ec`  
		Last Modified: Wed, 10 Sep 2025 21:57:04 GMT  
		Size: 362.9 KB (362863 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
