## `eclipse-temurin:11-jre-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:8887f4fa077f2d2644d73e042d14dbc2a32c53b675b7622fec7973fe5fe7db1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.26100.32690; amd64

```console
$ docker pull eclipse-temurin@sha256:9d8782a31bc7bc92251dbe165b76c3362518ec6da61e5920dabffe34d6b29f9a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **243.6 MB (243614557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257bf71ce852bc4bf11ae25bcd744c23b29ffea3fa8fecbe2fd8ba5d78575408`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 06:39:57 GMT
RUN Apply image 10.0.26100.32690
# Tue, 14 Apr 2026 22:13:03 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:13:05 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 22:13:05 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Apr 2026 22:13:05 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:13:11 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:13:12 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:13:21 GMT
COPY dir:9d7273a61bdbfae69a7bd32ee7f3a7621be43375d7aad513ad72640646f9a6e0 in C:\openjdk-11 
# Tue, 14 Apr 2026 22:13:26 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:8af320c3b6d19296bcc7947e3beb8bc0c69cb12143db52efe988dc998ac088dc`  
		Last Modified: Tue, 14 Apr 2026 21:00:37 GMT  
		Size: 199.7 MB (199717094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69b3777470a25f52dc7758f72e3cf1174041fc1dc70a1d5254719bab44b3e86`  
		Last Modified: Tue, 14 Apr 2026 22:13:32 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:448c245b35bea78c50c64ea9380e890ba0a530293f1cf8602d4cb0ba4a5de14f`  
		Last Modified: Tue, 14 Apr 2026 22:13:32 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f102a6b573896ddc79baf816fb132e6985f0186be592a77043ac03b53294e571`  
		Last Modified: Tue, 14 Apr 2026 22:13:32 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36799754ff6c03294080c2f464714faece64e7770b6f685c7c2687ac1c85342e`  
		Last Modified: Tue, 14 Apr 2026 22:13:30 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd5c4bb818fcafa634c0e993f9d2049dea38692656d9383e96a9f65789a6acb8`  
		Last Modified: Tue, 14 Apr 2026 22:13:30 GMT  
		Size: 70.3 KB (70254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0755870aa7323308196636cc9dec87d388b2f85719c96ecdad66aed65d53d5d`  
		Last Modified: Tue, 14 Apr 2026 22:13:30 GMT  
		Size: 1.1 KB (1079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2915592636ac14109abc7239925057f97e19c80f5f3fc0d4d9d025a144d9b94d`  
		Last Modified: Tue, 14 Apr 2026 22:13:36 GMT  
		Size: 43.7 MB (43719024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9711c27512769a54e74852808af6796b1243df4aae0088e6db846d4583e4c796`  
		Last Modified: Tue, 14 Apr 2026 22:13:30 GMT  
		Size: 102.8 KB (102782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jre-nanoserver` - windows version 10.0.20348.5020; amd64

```console
$ docker pull eclipse-temurin@sha256:c983e052f221d19819cb21bd1f7dd5cf84b5b301882a6ce1253ef27e2efdf5f1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.9 MB (170851984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7259befd7611a0361adb8a1d1435f9b8658453deec2db399425db2e2393612`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 13 Apr 2026 03:09:06 GMT
RUN Apply image 10.0.20348.5020
# Tue, 14 Apr 2026 22:11:10 GMT
SHELL [cmd /s /c]
# Tue, 14 Apr 2026 22:11:11 GMT
ENV JAVA_VERSION=jdk-11.0.30+7
# Tue, 14 Apr 2026 22:11:12 GMT
ENV JAVA_HOME=C:\openjdk-11
# Tue, 14 Apr 2026 22:11:13 GMT
USER ContainerAdministrator
# Tue, 14 Apr 2026 22:11:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 14 Apr 2026 22:11:20 GMT
USER ContainerUser
# Tue, 14 Apr 2026 22:11:31 GMT
COPY dir:9d7273a61bdbfae69a7bd32ee7f3a7621be43375d7aad513ad72640646f9a6e0 in C:\openjdk-11 
# Tue, 14 Apr 2026 22:11:33 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:076097f7bbc6f69c9354a56f2043172887b5d6056c3fdc093335fd876d092957`  
		Last Modified: Tue, 14 Apr 2026 18:00:15 GMT  
		Size: 127.0 MB (126955949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8993acfdf4686dba6fe118f01f7811517ee4c5ef953a3f4ff4422198e46d0cd0`  
		Last Modified: Tue, 14 Apr 2026 22:11:39 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ced5e408f4f1b1d7c321b9c1f8f732a6e49fefa841de724ec8524fb85221f71`  
		Last Modified: Tue, 14 Apr 2026 22:11:39 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9b01e7140185c8e98cf76d072c8f16ebeb7b39269c077e68d67a9471bafeaff`  
		Last Modified: Tue, 14 Apr 2026 22:11:39 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0629af5c86b106dc0c466fc12dab705ab9f0b5f77d23702680d0b81fcbc3fffa`  
		Last Modified: Tue, 14 Apr 2026 22:11:37 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3928d3189310ee1b7c0b11f99d3f3ff5d0e50d23b66197764cb7fc866302a537`  
		Last Modified: Tue, 14 Apr 2026 22:11:37 GMT  
		Size: 85.0 KB (85008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fad85b4c2b662309f43c63f064a5b2e3904269adc38bcbaf1138b2c76237f04`  
		Last Modified: Tue, 14 Apr 2026 22:11:37 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97596e461b189b6fae86bfaba93e79033081a54d5136db42012ad3e7f6002e4`  
		Last Modified: Tue, 14 Apr 2026 22:11:43 GMT  
		Size: 43.7 MB (43718826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d73f252092faecca7e7797eed9cf98e519c0d19016a399fdafd66512d6b4e06`  
		Last Modified: Tue, 14 Apr 2026 22:11:37 GMT  
		Size: 86.8 KB (86836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
