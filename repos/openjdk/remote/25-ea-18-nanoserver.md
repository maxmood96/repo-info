## `openjdk:25-ea-18-nanoserver`

```console
$ docker pull openjdk@sha256:bb385ec1ae38965d9ca6590715fb707c07f0e68e56af180d2ff9ac3dddad38d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7136; amd64

### `openjdk:25-ea-18-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull openjdk@sha256:0711e22c2b5968dff9907838459454e488b36f3c428115fbcffaadd4b0fffbd2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.5 MB (328509882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272701b30a85c1e375853dbf5d7490e847eed0ff3f150522136ff48c786fb6fb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Mon, 14 Apr 2025 23:24:32 GMT
SHELL [cmd /s /c]
# Mon, 14 Apr 2025 23:24:33 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:24:34 GMT
USER ContainerAdministrator
# Mon, 14 Apr 2025 23:24:36 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 14 Apr 2025 23:24:37 GMT
USER ContainerUser
# Mon, 14 Apr 2025 23:24:37 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:24:45 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Mon, 14 Apr 2025 23:24:52 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 14 Apr 2025 23:24:53 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1271dc6466f60914f513fd58b86a3963158664cbc978ebd558924d38830f49eb`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ce172a953b02da88a39f83e9e2a560e668585012672e0a3261d04c2f94a0f21`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa44aea9556d4463f7e87ded735698719df8dfc0c0b7c32b3647a3715db989f6`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 1.0 KB (1018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b2e2042c88f487a96dffc116642cfd3991b785bafa84e22178e0db5eb329ac`  
		Last Modified: Mon, 14 Apr 2025 23:24:57 GMT  
		Size: 76.3 KB (76291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0bf3300c9f523b2987f709b3633ff61a5e53d6f40892e59ca9effe4797fe8a3`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:debad990a6b0334dbf12d87eca164b18cf991b610ebbf985e7e8bd4bf9a2348b`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 1.1 KB (1091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b463d977dd09f2e70b780d5e2300411837fdd97e46b521d6904db176cdb09`  
		Last Modified: Mon, 14 Apr 2025 23:25:08 GMT  
		Size: 207.6 MB (207583880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f03979774dbb19709dc7c914da6827bf4083dc74019a9ca751415b0ab3939e19`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 107.1 KB (107105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed29696f7bbf7c157e5de30b1a60404af0295efe9896c473f8ae82efa0448c5`  
		Last Modified: Mon, 14 Apr 2025 23:24:56 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-ea-18-nanoserver` - windows version 10.0.17763.7136; amd64

```console
$ docker pull openjdk@sha256:91b78dbaa0ec18ee1b6a539ac8dc33b75b4449dfa527e1cc21051618318b06e2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (318962754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bafd74a724a524f55c7afe7ce798487791e8ea60f0cf2a681e5936d586d5bafb`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 05 Apr 2025 01:31:28 GMT
RUN Apply image 10.0.17763.7136
# Mon, 14 Apr 2025 23:14:27 GMT
SHELL [cmd /s /c]
# Mon, 14 Apr 2025 23:14:29 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 14 Apr 2025 23:14:29 GMT
USER ContainerAdministrator
# Mon, 14 Apr 2025 23:14:32 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 14 Apr 2025 23:14:33 GMT
USER ContainerUser
# Mon, 14 Apr 2025 23:14:33 GMT
ENV JAVA_VERSION=25-ea+18
# Mon, 14 Apr 2025 23:14:41 GMT
COPY dir:98e2e7765cda338b9693b53f1f8eb40deb194d41cda93e2a54447c0586fe61ce in C:\openjdk-25 
# Mon, 14 Apr 2025 23:14:45 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 14 Apr 2025 23:14:46 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:a06e0965a0fa3715e629889bd9332aa22aadd75654cac5c9818b67c0264b3ee1`  
		Last Modified: Tue, 08 Apr 2025 20:16:02 GMT  
		Size: 106.9 MB (106922524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e45f08fe1603498d7be8297376c43a71dcd1099582214677de399e7a1ac3214`  
		Last Modified: Mon, 14 Apr 2025 23:14:53 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:363a1af7ac5fd9212432a78a7fcf21a286207ee45f67090f8790a665469a4c8d`  
		Last Modified: Mon, 14 Apr 2025 23:14:52 GMT  
		Size: 1.1 KB (1108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad671457faa3a978b1da4cb3d46e3eb68f07ab588b2c185e4819a0b1b985611d`  
		Last Modified: Mon, 14 Apr 2025 23:14:52 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8406ff0c69029e9e16a4dcb74165833979752d96d8f75dccaf4efda54b9ec59b`  
		Last Modified: Mon, 14 Apr 2025 23:14:52 GMT  
		Size: 69.3 KB (69332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd7cd413bd897e315a8e0b5b6ff874472c8ade4927ade11698ea99570d2e617a`  
		Last Modified: Mon, 14 Apr 2025 23:14:50 GMT  
		Size: 1.1 KB (1088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d04fcc22ec54d6a2c4690731c847355e40553022a3bce0264740b537c1553ff1`  
		Last Modified: Mon, 14 Apr 2025 23:14:50 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:506751f9c1d864d1bf9e15a05c22656b7b6523567c332c0a8ead179dfa00affd`  
		Last Modified: Mon, 14 Apr 2025 23:15:02 GMT  
		Size: 207.6 MB (207581792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1dc106429ab630ccafce240fa5913a3b66959be9044e0a5d5e61f0d8713db5d`  
		Last Modified: Mon, 14 Apr 2025 23:14:51 GMT  
		Size: 4.4 MB (4382709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e3fd7a95929801c7a720b711505d901e5af59828c4c3d30c9d6bc426c54cb6`  
		Last Modified: Mon, 14 Apr 2025 23:14:50 GMT  
		Size: 1.0 KB (1022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
