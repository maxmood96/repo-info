## `eclipse-temurin:21-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:176c5c9c71667b0ddd5dea699f4e83496c3d9bb25671b25aeb29558a13b07856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.3932; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.3932; amd64

```console
$ docker pull eclipse-temurin@sha256:d599c668950217f0d21877b7e905935af7461c72f79d37eb0574d5be715f69f7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **324.4 MB (324374646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c2f38457b4a0f8e3cff2cdbdd34af0bca564321ef7d14858362cfce00b9625`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Jul 2025 05:15:23 GMT
RUN Apply image 10.0.20348.3932
# Wed, 09 Jul 2025 19:12:26 GMT
SHELL [cmd /s /c]
# Wed, 09 Jul 2025 19:12:28 GMT
ENV JAVA_VERSION=jdk-21.0.7+6
# Wed, 09 Jul 2025 19:12:29 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 09 Jul 2025 19:12:30 GMT
USER ContainerAdministrator
# Wed, 09 Jul 2025 19:12:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Jul 2025 19:12:33 GMT
USER ContainerUser
# Wed, 09 Jul 2025 19:12:40 GMT
COPY dir:db067bfbcc086396d5dfa4ac3979b5c2114a2c9ec3e102fbc339048e5a829713 in C:\openjdk-21 
# Wed, 09 Jul 2025 19:12:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Jul 2025 19:12:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:b1cf2c299ff70c52cb8ecf52e66d64d5068519867510919d8807ed2c58a54ba2`  
		Last Modified: Tue, 08 Jul 2025 21:55:51 GMT  
		Size: 122.6 MB (122630906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06fe2274f38ad1a38bc60861757fc560e37b1f973124cd416e0193f9d0437474`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b693823f39d9a8f6bd698c99ef27c224b756b257bfd1c7d1d85e8603e113fcf3`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:727cdaa79b87d3729b380e9e080048d75a21f546cb1d39b5f831a3146772d27f`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af172acbb5a1711fdc375d86e5f8438140b66e6eabc5763f293437760aaea4ee`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83758e3be61a8ea514c2885fb741f1df38abb48999cfcb27e02e05f93fee0c33`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 79.3 KB (79325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5daf818a9abeb7e634296b41ee5a75329447958c2374b222f6ffb46b378277`  
		Last Modified: Wed, 09 Jul 2025 19:13:09 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1915cba74f768d6258dea24021b2ee8d045c0c506ca88696f608a211abe31496`  
		Last Modified: Wed, 09 Jul 2025 21:15:44 GMT  
		Size: 201.6 MB (201551161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a306962865f4875f6b97b2bf2b69d1c34d7a66083519a96f54a79383295c485d`  
		Last Modified: Wed, 09 Jul 2025 19:13:10 GMT  
		Size: 107.1 KB (107081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db80a41d93cd97b1810fefbd90d954b1f9ea2edf025b7a77b8e4da21a24efd77`  
		Last Modified: Wed, 09 Jul 2025 19:13:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
