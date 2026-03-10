## `openjdk:26-rc-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:32c2f2d4b039cb3b2820f42282880a0975c8dab755fa6266277df74d4e4288c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32522; amd64

### `openjdk:26-rc-nanoserver-ltsc2025` - windows version 10.0.26100.32522; amd64

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
