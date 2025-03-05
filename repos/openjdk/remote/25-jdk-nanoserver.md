## `openjdk:25-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:6e98fce41697910f730060e3fa74b02879ca165eae4cea40e116b7db81de0a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3194; amd64
	-	windows version 10.0.20348.3207; amd64
	-	windows version 10.0.17763.6893; amd64

### `openjdk:25-jdk-nanoserver` - windows version 10.0.26100.3194; amd64

```console
$ docker pull openjdk@sha256:ee3dd26e990906bf8953fe1fff7f1e6ee3e96134be30a9a4850daf120c4b3260
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **413.6 MB (413618536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a80deb00cfee2da575662aede9bb7104a4f61a85f0b44845a421750053ebff5e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 08 Feb 2025 22:31:47 GMT
RUN Apply image 10.0.26100.3194
# Tue, 04 Mar 2025 23:16:24 GMT
SHELL [cmd /s /c]
# Tue, 04 Mar 2025 23:16:25 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 23:16:25 GMT
USER ContainerAdministrator
# Tue, 04 Mar 2025 23:16:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 04 Mar 2025 23:16:30 GMT
USER ContainerUser
# Tue, 04 Mar 2025 23:16:31 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 23:16:37 GMT
COPY dir:e3a80d16f60f733e38f65676798afaa74a4cc6b6b9e0edd1774eacf12556d4ac in C:\openjdk-25 
# Tue, 04 Mar 2025 23:16:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 04 Mar 2025 23:16:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e075dd07cbf907b7da8dbd8365b73a71ac92a834b78f520bd976cb97e0fcc0a1`  
		Last Modified: Wed, 12 Feb 2025 22:34:59 GMT  
		Size: 205.9 MB (205890263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76761fd2e245b1e403d649a70752cdf0616d6994d479b43cc56a67786201e04d`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9991ce78411fa1ec567ea38fd441c3754e39f4444cfb2d4ecef50b6fbf57e576`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0c6188898568e1a61f8e563cdc3efe7bb56622fa8f3feefa86fc254a41bb753`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:987bb5021dce531b24c9c3c119c2f93067cf27eb460a4b44bb97bb366987e6cd`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 77.1 KB (77076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e1980b4694b50d71ccc57e6f470e79cb09d08e7556de210632a17679d88acdb`  
		Last Modified: Tue, 04 Mar 2025 23:16:48 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739d672e2a8690261e96ac0091a9606132ae2193545d0209ff13f60f445d127a`  
		Last Modified: Tue, 04 Mar 2025 23:16:48 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:152155a8db3edd812443377d8f3472161628687b1e68c864ba185b817d431793`  
		Last Modified: Tue, 04 Mar 2025 23:17:00 GMT  
		Size: 207.5 MB (207540093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9580863c552293d72409cc4e077eccb6e6b0267e49fcc42e90429e6e87c697a5`  
		Last Modified: Tue, 04 Mar 2025 23:16:49 GMT  
		Size: 104.8 KB (104765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cdceda218bce764a3cce306bb3ce9bf322e1187f594314c1e1820bff8c54f6d`  
		Last Modified: Tue, 04 Mar 2025 23:16:48 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-jdk-nanoserver` - windows version 10.0.20348.3207; amd64

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

### `openjdk:25-jdk-nanoserver` - windows version 10.0.17763.6893; amd64

```console
$ docker pull openjdk@sha256:a1f40899fe1e9c05347d364d6771066bc7ece4fb88efb60349b9954b49c2b9d1
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318908882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1001f1f40cd52bb4596dc106a60ee18bfdd930195daf34f1c43ed3dc32627ecc`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Feb 2025 17:59:14 GMT
RUN Apply image 10.0.17763.6893
# Tue, 04 Mar 2025 22:43:40 GMT
SHELL [cmd /s /c]
# Tue, 04 Mar 2025 22:43:42 GMT
ENV JAVA_HOME=C:\openjdk-25
# Tue, 04 Mar 2025 22:43:43 GMT
USER ContainerAdministrator
# Tue, 04 Mar 2025 22:44:01 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 04 Mar 2025 22:44:01 GMT
USER ContainerUser
# Tue, 04 Mar 2025 22:44:01 GMT
ENV JAVA_VERSION=25-ea+12
# Tue, 04 Mar 2025 22:44:12 GMT
COPY dir:e3a80d16f60f733e38f65676798afaa74a4cc6b6b9e0edd1774eacf12556d4ac in C:\openjdk-25 
# Tue, 04 Mar 2025 22:44:17 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 04 Mar 2025 22:44:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5965f4f533e4b42b41b3fd8dff42c138329bf35311ce090d4c7cc4acd5a59360`  
		Last Modified: Tue, 11 Feb 2025 20:25:23 GMT  
		Size: 106.9 MB (106915466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:061f782b9fd12caea0f483589b063feb21f942f137d798e5bb3d27b990df9723`  
		Last Modified: Tue, 04 Mar 2025 22:44:22 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724cd741e3cd0f7dd0f6a6ffab21d57c4101e4b1acc0e57f35f469f90015299b`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d7025f713263ca3e5013a9701ce60f4350f08da9b7791caf087eeefcbe93d76`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44a88d13e78e2d7a96ebf7242ea66cec5283fc3791960c83b8951f76a4ed41e6`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 68.0 KB (68039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75464489d8b70232cd685e65d80fa11fd59be46d15f0f7b628458aa92c344f0c`  
		Last Modified: Tue, 04 Mar 2025 22:44:20 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39c0df8e4d1e5fe657d0f5c059dce25d242383979d6b706602edebfc3930b16`  
		Last Modified: Tue, 04 Mar 2025 22:44:20 GMT  
		Size: 1.0 KB (1048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6378fee93d5717240e23b0a00bd12e2f6088c600d932534064bee9911e8c18e0`  
		Last Modified: Tue, 04 Mar 2025 22:44:31 GMT  
		Size: 207.5 MB (207541773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09c6922e19d3083228c3f79ffde53bae177b36c6e9ab6f5e8df3dc356820d9cf`  
		Last Modified: Tue, 04 Mar 2025 22:44:21 GMT  
		Size: 4.4 MB (4377320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d1343abfc49ef5c40bf1ecb5cca0d3e4b42a481948b8753347c498ead5b27f`  
		Last Modified: Tue, 04 Mar 2025 22:44:20 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
