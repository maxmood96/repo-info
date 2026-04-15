## `eclipse-temurin:11-jre-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:ad45e2639daa530352c7aeee27625ad1a3b528741d82a41d3c11581a98510456
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32690; amd64

### `eclipse-temurin:11-jre-nanoserver-ltsc2025` - windows version 10.0.26100.32690; amd64

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
