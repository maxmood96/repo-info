## `openjdk:26-rc-nanoserver`

```console
$ docker pull openjdk@sha256:55b525374aa0c0e5158bb34393fa327e32796efc1ef571cc94bede466fc9b96a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:26-rc-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:644aaf534ee84dbef71363aaf6e635e6011fa4f260da94e55c07eb685d72bf34
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423564300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989ad8a9f7342684d2738fdf744da1534ad5a55e37b898baadd11c0f321fb8b7`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Tue, 10 Mar 2026 22:43:00 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:44:43 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Mar 2026 22:44:43 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:44:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Mar 2026 22:44:45 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:44:45 GMT
ENV JAVA_VERSION=26
# Tue, 10 Mar 2026 22:44:58 GMT
COPY dir:48d9a1614aae77abafeeb59360dca42b580c313456033330908c8e794bbb7778 in C:\openjdk-26 
# Tue, 10 Mar 2026 22:45:03 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Mar 2026 22:45:03 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71f7869993458abe7da3875a434f95cf18f3fba5016f632bb0bc2664816a15ad`  
		Last Modified: Tue, 10 Mar 2026 22:43:29 GMT  
		Size: 1.1 KB (1092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92b04f443c75bff7996218116cc891abe05e1cf054cbe013c8cb69e859b2540c`  
		Last Modified: Tue, 10 Mar 2026 22:45:08 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6690b6679bd59ce4fa0f3f7e855f755c561dbd8975fb409fc54e56554e21653f`  
		Last Modified: Tue, 10 Mar 2026 22:45:08 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b1fa54c5bea630664f2060ef3a240aef0895f6a64e343bb469a54c456a6ac25`  
		Last Modified: Tue, 10 Mar 2026 22:45:08 GMT  
		Size: 71.8 KB (71790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4256b2ff13f8932168ab92ee9570751907f0c7b6e19aaf0ae7875ac6082ee24a`  
		Last Modified: Tue, 10 Mar 2026 22:45:07 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83242110ce50f8a66ae6f3a155e9cde7f1e72be8e17e4ed9ad2a1a8c27729d10`  
		Last Modified: Tue, 10 Mar 2026 22:45:07 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5318783896b096a9bd8a5002ffa7b0e332ebd71c2128c81207923de0d3118e80`  
		Last Modified: Tue, 10 Mar 2026 22:45:22 GMT  
		Size: 224.0 MB (223950533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011f794361e2e9c2bd4e1714f8db0573cc327a6ae8e27fead512d361d0cb572a`  
		Last Modified: Tue, 10 Mar 2026 22:45:07 GMT  
		Size: 126.2 KB (126210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b323db2f930e23987b104f500f7b836c6468806596de8823f45e2dce9039da23`  
		Last Modified: Tue, 10 Mar 2026 22:45:07 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:26-rc-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:d1c794df0993baf25f56b2af4a4ed8d8dd870cbb6437db89a4ad987cd2f8f3b4
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.8 MB (350791120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a908652b9ea31947f0a9db5b5da1c26d6d93dab6b55abdf2f3daebcd88d30b0f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Tue, 10 Mar 2026 22:36:18 GMT
SHELL [cmd /s /c]
# Tue, 10 Mar 2026 22:40:11 GMT
ENV JAVA_HOME=C:\openjdk-26
# Tue, 10 Mar 2026 22:40:11 GMT
USER ContainerAdministrator
# Tue, 10 Mar 2026 22:40:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 10 Mar 2026 22:40:13 GMT
USER ContainerUser
# Tue, 10 Mar 2026 22:40:14 GMT
ENV JAVA_VERSION=26
# Tue, 10 Mar 2026 22:40:23 GMT
COPY dir:48d9a1614aae77abafeeb59360dca42b580c313456033330908c8e794bbb7778 in C:\openjdk-26 
# Tue, 10 Mar 2026 22:40:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 10 Mar 2026 22:40:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ba2425154dbe4f9c92a7daa50ee78f1d65a2f56409da6f247f3870c5a1f698a`  
		Last Modified: Tue, 10 Mar 2026 22:36:37 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cb82b6bc5a9f90952aac65c3cb71ba080613cc4a16a8388c783cd9f3ebb193b`  
		Last Modified: Tue, 10 Mar 2026 22:40:34 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2f330fcf134f213b9995ae1fedd12c50293ebfaf7eb746e93dcd86bdf84521`  
		Last Modified: Tue, 10 Mar 2026 22:40:33 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af2b3ac0a842aba78ce85591fa7bf73969fd8cd7816507d8a4fa03720bbb5a06`  
		Last Modified: Tue, 10 Mar 2026 22:40:33 GMT  
		Size: 76.6 KB (76570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e081012b9980a99fae51fabebcbc40a8ad24d56765e26af362f9243ab9a2a5bd`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58d469dc3944df392e5e1ebf1661dde9c2b32c7c1aa13193652f1c5e889989b4`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ece040cee1133bd1fa98e8add636620831529308448f281ee69b5491a8b1610c`  
		Last Modified: Tue, 10 Mar 2026 22:40:48 GMT  
		Size: 224.0 MB (223950547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0f1035e3dd36028d312b78cd344fd9f6ca69745dadc2340c3bd54dcf702d692`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 107.0 KB (107044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6bcd72ec7de00fed32731e88b906c3af715de3b5a49761e88ac6c2d6b40fbe6`  
		Last Modified: Tue, 10 Mar 2026 22:40:32 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
