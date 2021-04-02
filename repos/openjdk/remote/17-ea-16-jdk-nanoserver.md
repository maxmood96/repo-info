## `openjdk:17-ea-16-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:6da5f5f93117d639bdf9b8483f74606b030cd4bdb25caf7526d853cbf9e2e410
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1817; amd64

### `openjdk:17-ea-16-jdk-nanoserver` - windows version 10.0.17763.1817; amd64

```console
$ docker pull openjdk@sha256:5686a2d3e1845de65abd2c6f7f7129522c0a22f80835e174116d01e012284cd8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.9 MB (285856869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0e1cda44344e4c2da54fbb8760ef85987f702152596b73504940fefe7c20c5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 26 Feb 2021 16:47:31 GMT
RUN Apply image 1809-amd64
# Wed, 10 Mar 2021 17:50:47 GMT
SHELL [cmd /s /c]
# Wed, 10 Mar 2021 17:50:48 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 10 Mar 2021 17:50:49 GMT
USER ContainerAdministrator
# Wed, 10 Mar 2021 17:51:08 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Mar 2021 17:51:08 GMT
USER ContainerUser
# Fri, 02 Apr 2021 18:31:28 GMT
ENV JAVA_VERSION=17-ea+16
# Fri, 02 Apr 2021 18:31:47 GMT
COPY dir:99f84c2b26faf2d565bb1a3007e29fd9ae380b3f297b73d49a257bd2f562d63e in C:\openjdk-17 
# Fri, 02 Apr 2021 18:32:26 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 02 Apr 2021 18:32:27 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a11c4ca8f1ba16b6e1395d4523be2215bd0871c2e3e4695b9f2b87bd7472be52`  
		Size: 101.4 MB (101389964 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b1146273d9b624ee892dfcbb3c753523f09f79536a16d63b711cb0027825374a`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c1ac1e6f2d0594fe7e8e0395310c60461fc8ce5183f6a15db964a07b66176e`  
		Last Modified: Wed, 10 Mar 2021 18:33:51 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:050de60c3748a5bfc798f599cadba652e52a162ca31f36b8c783664c11ed224b`  
		Last Modified: Wed, 10 Mar 2021 18:33:54 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e309359702f2d5c4fa7bc854144ad320712050892d017cdfcb58acff4fea2609`  
		Last Modified: Wed, 10 Mar 2021 18:33:50 GMT  
		Size: 66.6 KB (66576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97ecf2dccedb4699a8caf6c19a7a80768c90efb0af5959f1465b00abe8faa12`  
		Last Modified: Wed, 10 Mar 2021 18:33:48 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8aa6f04d76c2e693bf7bbbf9f5372f4321155521b92191173ecbf04e6cca605b`  
		Last Modified: Fri, 02 Apr 2021 18:40:23 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567511542d63ecce710c82eadaaebd869bf3c9b7da60430329bbbecdcdb6ad6f`  
		Last Modified: Fri, 02 Apr 2021 18:40:43 GMT  
		Size: 180.8 MB (180770399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ef9f6b468d695234df3744b5b91c866defc88cb41917cface8f2f494fd3476`  
		Last Modified: Fri, 02 Apr 2021 18:40:27 GMT  
		Size: 3.6 MB (3623121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e72eaa6e013771964f55fc2260cb8a1360e090aaeab1471258da1048abf625a9`  
		Last Modified: Fri, 02 Apr 2021 18:40:23 GMT  
		Size: 1.1 KB (1096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
