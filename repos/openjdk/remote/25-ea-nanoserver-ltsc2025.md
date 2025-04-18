## `openjdk:25-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:f783bd2df6a306e0b761d6ae02099bbb1ba9ac477e5ef61d2ff3e7e0e8c80992
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `openjdk:25-ea-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

```console
$ docker pull openjdk@sha256:f0089bc2f2b91a22d1657db551416c061952a35506ca1785a6e6fa8c15883d7b
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.0 MB (398001132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8786dc0fb9925275c620843df5dc1ba9331be1e01886a7a80560e149588084`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 19:13:25 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 19:13:26 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 18 Apr 2025 19:13:27 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 19:13:29 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 18 Apr 2025 19:13:30 GMT
USER ContainerUser
# Fri, 18 Apr 2025 19:13:31 GMT
ENV JAVA_VERSION=25-ea+19
# Fri, 18 Apr 2025 19:13:38 GMT
COPY dir:595a9046aeb360afc9a03339cfcb9f80b8fb3559c4a1bfb194a0956d7f6a1899 in C:\openjdk-25 
# Fri, 18 Apr 2025 19:13:46 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 18 Apr 2025 19:13:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70cdbebaf49974106aaa6e14ba64219df10aee92d654984eca4bf6d04f54efa4`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4c1f089a47bca587005c935224357921ae601133738cc21d5dfef0f9cbfa5`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dad97aa81a7d82750b8d80df969378391dab1e7089f221abf2d794d803a37d`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e163f320d21f2965653dc9eeb17790c53e55f96aea69f57cf02db83268c41e`  
		Last Modified: Fri, 18 Apr 2025 19:13:53 GMT  
		Size: 76.0 KB (76000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af57c8572c1a819cac1c451452122ea68c9f9db9dfa48a130fe79ecc94eed078`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8326b399b507eaa182218a8e1237e5dccf75e1f277e1bb45f2513185d77fe64`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9c849df021f526105a78f3ba71f4345906561fd3b42d2fe00b48832dcf5c9e`  
		Last Modified: Fri, 18 Apr 2025 19:14:03 GMT  
		Size: 207.7 MB (207662320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a500e7bbb31d65e970330c7ca1a9a87fe8a71ebc78d3ad7d5e6662468f4fde88`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 114.5 KB (114486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e9aae5121233c52e1a92b70b48a8c3eb5be0cb367c23350829b03f9a5df1492`  
		Last Modified: Fri, 18 Apr 2025 19:13:51 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
