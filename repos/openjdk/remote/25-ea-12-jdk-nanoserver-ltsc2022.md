## `openjdk:25-ea-12-jdk-nanoserver-ltsc2022`

```console
$ docker pull openjdk@sha256:f557322b2978059e957aeb6692cc1c9478277e59a3ee473e72c7589a9bf64770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3207; amd64

### `openjdk:25-ea-12-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3207; amd64

```console
$ docker pull openjdk@sha256:2aac1137d95b735b3087dd4d2f52b2c6cd42ff82a276475342749456db820a2c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.4 MB (328397381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd12f979ba2a0c34dee204fedf0ed1327f57b2bb081255b4b3184ef993065905`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 20:45:43 GMT
RUN Apply image 10.0.20348.3207
# Tue, 04 Mar 2025 22:43:12 GMT
SHELL [cmd /s /c]
# Tue, 04 Mar 2025 22:43:13 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 22:43:13 GMT
USER ContainerAdministrator
# Tue, 04 Mar 2025 22:43:18 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 04 Mar 2025 22:43:18 GMT
USER ContainerUser
# Tue, 04 Mar 2025 22:43:19 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 22:43:26 GMT
COPY dir:e3a80d16f60f733e38f65676798afaa74a4cc6b6b9e0edd1774eacf12556d4ac in C:\openjdk-25 
# Tue, 04 Mar 2025 22:43:31 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 04 Mar 2025 22:43:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:938e4585b186fc3df3c1959d47ba7a634fea121cec7545db7923ceb191d99a33`  
		Last Modified: Tue, 11 Feb 2025 22:43:09 GMT  
		Size: 120.7 MB (120666610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac64d6470a52c0ba79e03c43dc8cb5078654278dfe23f9ab56bda7b6ce4af21`  
		Last Modified: Tue, 04 Mar 2025 22:43:38 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f386abf5a4c38f1ff4e64a2c5040f13e552738a13f2b6a44977582eef567460`  
		Last Modified: Tue, 04 Mar 2025 22:43:37 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c938a6efb8d328446ceaeb8653a02a2e623a851b9cc958899eb4f4bf9bf1133`  
		Last Modified: Tue, 04 Mar 2025 22:43:37 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ed5c1ba8685ee500ba2e038b6441b2feaee8f3903b42d3055f143556102219e`  
		Last Modified: Tue, 04 Mar 2025 22:43:37 GMT  
		Size: 73.9 KB (73869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d72487195cbb84c988a547e72cca83b0c95ad75ff304ac52e8b83fc82422ba`  
		Last Modified: Tue, 04 Mar 2025 22:43:35 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a842215fa8d4d6a9e837dd100d10460d4f314e81c607825445c6483d4c31469e`  
		Last Modified: Tue, 04 Mar 2025 22:43:35 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271e0e3986dad9e348b2161934e930745c92006314bb637c8f9b4f11cca52c63`  
		Last Modified: Tue, 04 Mar 2025 22:43:46 GMT  
		Size: 207.5 MB (207541798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59ebd13db6fd22637ef2a69feb68e1002fd950085fbb878b01c0c3af9f693301`  
		Last Modified: Tue, 04 Mar 2025 22:43:36 GMT  
		Size: 108.9 KB (108913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:806dfe97feb49fba7e148440f8d1408a576adfc8585871661fd243b290f29864`  
		Last Modified: Tue, 04 Mar 2025 22:43:35 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
