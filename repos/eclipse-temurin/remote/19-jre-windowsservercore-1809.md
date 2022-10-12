## `eclipse-temurin:19-jre-windowsservercore-1809`

```console
$ docker pull eclipse-temurin@sha256:49a394290696bb1f914fc6122aa5067063c595fc7c327c698a2fa49b6c1a328d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3532; amd64

### `eclipse-temurin:19-jre-windowsservercore-1809` - windows version 10.0.17763.3532; amd64

```console
$ docker pull eclipse-temurin@sha256:fe5ff3ff465453fb4a65ee7da4aebda2b45b6cec0672ebf1b792c504fcbb95cb
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2792043977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5417cbf9caa5ed08640972852dd1fcad3dc6a2a5ea2ccdbca996d5d5ab297c3e`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Sat, 08 Oct 2022 01:55:32 GMT
RUN Install update 10.0.17763.3532
# Tue, 11 Oct 2022 20:24:02 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Oct 2022 15:46:57 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 12 Oct 2022 15:52:37 GMT
RUN Write-Host ('Downloading https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ...');     curl.exe -LfsSo openjdk.msi https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jre_x64_windows_hotspot_19_36.msi ;     Write-Host ('Verifying sha256 (2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35) ...');     if ((Get-FileHash openjdk.msi -Algorithm sha256).Hash -ne '2fe3e0989b31551b65cd3d276f8435618aad7f4e3f2996a58c3b51f0de4ccf35') {         Write-Host 'FAILED!';         exit 1;     };         New-Item -ItemType Directory -Path C:\temp | Out-Null;         Write-Host 'Installing using MSI ...';     $proc = Start-Process -FilePath "msiexec.exe" -ArgumentList '/i', 'openjdk.msi', '/L*V', 'C:\temp\OpenJDK.log',     '/quiet', 'ADDLOCAL=FeatureEnvironment,FeatureJarFileRunWith,FeatureJavaHome', 'INSTALLDIR=C:\openjdk-19' -Wait -Passthru;     $proc.WaitForExit() ;     if ($proc.ExitCode -ne 0) {         Write-Host 'FAILED installing MSI!' ;         exit 1;     };         Remove-Item -Path C:\temp -Recurse | Out-Null;     Write-Host 'Removing openjdk.msi ...';     Remove-Item openjdk.msi -Force
# Wed, 12 Oct 2022 15:53:39 GMT
RUN Write-Host 'Verifying install ...';     Write-Host 'java --version'; java --version;         Write-Host 'Complete.'
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:028c482fad0f111537a40f65401f65de54c9fd682951a4f8cf9b644d7c128e18`  
		Size: 834.0 MB (833997855 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c70f9828a2aec7ea0624298c8cc6f0bcb5f21b439f4e96304b8b47c8bf15ef8d`  
		Last Modified: Tue, 11 Oct 2022 20:35:04 GMT  
		Size: 1.4 KB (1424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3dee8b9b3dd566ea929a35fa67b2ac465b6d1cb9366aabe0ca02008ba24990c`  
		Last Modified: Wed, 12 Oct 2022 16:10:35 GMT  
		Size: 1.4 KB (1445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a4b2a19265e7c6851348cf8ade3cc836b2a686dadaeb2b9bcc9f85fddb04f8`  
		Last Modified: Wed, 12 Oct 2022 16:12:22 GMT  
		Size: 77.6 MB (77557187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7b222eba6b17343cf86f872c6aff4e9662a4e2de63516c5c179621e5a37219`  
		Last Modified: Wed, 12 Oct 2022 16:12:12 GMT  
		Size: 3.3 MB (3319978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
