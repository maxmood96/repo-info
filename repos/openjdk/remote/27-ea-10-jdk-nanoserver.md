## `openjdk:27-ea-10-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:d3c6381985352240a1b44e821977c0bff5ac5bf77dc816085bcc178e67f9b2ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32370; amd64
	-	windows version 10.0.20348.4773; amd64

### `openjdk:27-ea-10-jdk-nanoserver` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:f19542765bb57765e807109115939e96eefbd84ba7057f05e30393d62a97674d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.9 MB (423895148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:248826ce1ca586dd069122cde2865b230f1026c7524823d0502b81d071d7da80`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Sat, 21 Feb 2026 02:11:18 GMT
SHELL [cmd /s /c]
# Sat, 21 Feb 2026 02:11:19 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 21 Feb 2026 02:11:20 GMT
USER ContainerAdministrator
# Sat, 21 Feb 2026 02:11:33 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 21 Feb 2026 02:11:34 GMT
USER ContainerUser
# Sat, 21 Feb 2026 02:11:34 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 02:12:10 GMT
COPY dir:b5fb2cdf15741fc61f648125fc522c32c71b7cde2bc942ffb1c055f2d9c3754f in C:\openjdk-27 
# Sat, 21 Feb 2026 02:12:18 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 21 Feb 2026 02:12:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07979ad76735b94dfc2b231b37dae878f36ad28f306b99dddbccd0d878c5051`  
		Last Modified: Sat, 21 Feb 2026 02:12:26 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e960a0783ae9a83d94ef189c5bacd96581169d3c3731488278c0fbda44a26ec`  
		Last Modified: Sat, 21 Feb 2026 02:12:26 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba9137cd87bb64680edd88151579a0d9d20b4051ee422f71c707260fe26a6424`  
		Last Modified: Sat, 21 Feb 2026 02:12:26 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a83c0f87c8abe76efe927395d6941e3782b6bb2792633baf0f6f15d94e6939`  
		Last Modified: Sat, 21 Feb 2026 02:12:26 GMT  
		Size: 69.7 KB (69655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165aade3cb18bb70885719e155d4615cee737ac98326801fd26c78d0a00c9cef`  
		Last Modified: Sat, 21 Feb 2026 02:12:25 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414fa7b1b9e355b907aa22076271681f0c5416a3ee4926fedd4fcdfa4434e0e5`  
		Last Modified: Sat, 21 Feb 2026 02:12:25 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eff30a50c1d268429b03d3df7c32ac25eae20cdb8dbfb464eaebbf00cc7d1d7d`  
		Last Modified: Sat, 21 Feb 2026 02:12:40 GMT  
		Size: 224.5 MB (224472687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2573b3aee361b9bb21492b0b92b3d42661e662f5ed7d8486227c3e81444fd505`  
		Last Modified: Sat, 21 Feb 2026 02:12:25 GMT  
		Size: 94.7 KB (94703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0336e745664ea152a69be59f1401ce9881265d58bcf9a8d2967a4893bb57ece`  
		Last Modified: Sat, 21 Feb 2026 02:12:25 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-10-jdk-nanoserver` - windows version 10.0.20348.4773; amd64

```console
$ docker pull openjdk@sha256:ac08341ff769990404d1eab73d6c6e294f2b77367c9e60c2a12206e918b68083
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.3 MB (351338772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fdbdbe4bf5d8d8f9de2fd8a61f0a09dd52728d61915c9161de9640ffaadfb41`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Sat, 21 Feb 2026 02:11:18 GMT
SHELL [cmd /s /c]
# Sat, 21 Feb 2026 02:11:20 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 21 Feb 2026 02:11:21 GMT
USER ContainerAdministrator
# Sat, 21 Feb 2026 02:11:28 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 21 Feb 2026 02:11:29 GMT
USER ContainerUser
# Sat, 21 Feb 2026 02:11:30 GMT
ENV JAVA_VERSION=27-ea+10
# Sat, 21 Feb 2026 02:13:00 GMT
COPY dir:b5fb2cdf15741fc61f648125fc522c32c71b7cde2bc942ffb1c055f2d9c3754f in C:\openjdk-27 
# Sat, 21 Feb 2026 02:13:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 21 Feb 2026 02:13:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f20948fe61bf2379e73728c08be7e1a9dca4703d7dd6a29bbc9262fb138b4120`  
		Last Modified: Sat, 21 Feb 2026 02:13:14 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b064ee25ebe92bc2646ee95dffa6357500cd31b13083136f51f015835555e4b4`  
		Last Modified: Sat, 21 Feb 2026 02:13:14 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b76fecc32e87771c09a6b5c522c9bfad1d0c8fb7180a06ac61b71b3579f16ad0`  
		Last Modified: Sat, 21 Feb 2026 02:13:14 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:060d31498e66597acbc719eeaa40373bc09f17daec751eb0a5576eaaa4c45821`  
		Last Modified: Sat, 21 Feb 2026 02:13:14 GMT  
		Size: 83.2 KB (83227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f81c022ad7435f06ac81707af7cefb894733c8ca2554752c4012014b4fccb696`  
		Last Modified: Sat, 21 Feb 2026 02:13:13 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa08a5446f918d4a9f59e034f1820b012c703d4c5fa67b42b6ecf25dcd0c1fa7`  
		Last Modified: Sat, 21 Feb 2026 02:13:12 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8166dfe709fcedc0dfaddd1abd751a2cce7847fc8ff795e4ece392871904c353`  
		Last Modified: Sat, 21 Feb 2026 02:13:29 GMT  
		Size: 224.5 MB (224472390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4350e2e52a304cb6c5d1ef904de9d7a0ed3decbf7173b38ae94b9d6094972a9e`  
		Last Modified: Sat, 21 Feb 2026 02:13:12 GMT  
		Size: 130.9 KB (130902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be2de0dc3a40e676605e99c8477db77c5cb7ef9404b0acee75c9a015e7a455a`  
		Last Modified: Sat, 21 Feb 2026 02:13:12 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
