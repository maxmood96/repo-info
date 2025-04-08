## `openjdk:25-nanoserver`

```console
$ docker pull openjdk@sha256:3d45d8e577274c965c4db5225a3ffc5bedbff68c88d246f1046585dad815734d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull openjdk@sha256:503c63806ab9c0452c2fbab9a34bf81a15e7d448b8b8a0bcd2fb0342a3acd029
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.5 MB (414455841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44a73d81243956c533feb16e6a82fe649cb1a727b82e646b86201a89b87531f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Mon, 07 Apr 2025 23:48:12 GMT
SHELL [cmd /s /c]
# Mon, 07 Apr 2025 23:48:12 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Apr 2025 23:48:13 GMT
USER ContainerAdministrator
# Mon, 07 Apr 2025 23:48:16 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Apr 2025 23:48:16 GMT
USER ContainerUser
# Mon, 07 Apr 2025 23:48:17 GMT
ENV JAVA_VERSION=25-ea+17
# Mon, 07 Apr 2025 23:48:25 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Mon, 07 Apr 2025 23:48:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Apr 2025 23:48:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b9ab54e1e778652e40f22bf7a2b51c00e90344a8188b86995b570cc32e8cb1`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f6241a00f7e4291236b5f35f5b95757f175ce0f7647733a36123d7a96c5e2f1`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e50e1bee598d64563fad7b0944759d98cfa68f121b82568f022809ba81f2f27b`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd2e103c7b6496251d6614ed5457c3c08e00a9e7574ea6de96cf8deef47da69a`  
		Last Modified: Mon, 07 Apr 2025 23:48:38 GMT  
		Size: 76.4 KB (76370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0cc0bd25cf59f5f41f37bc1132f8703b58d3fc498e2a6181691255f1314da968`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dabd5e3565a3c3387ee3e6812e3331f1fe1eff6b9e1f7335d52e4e7daae1443f`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76275c5753cb3bb64649bc05f1bc242645a2b1ca36ea6ff0388aaf5f5d07b3d8`  
		Last Modified: Mon, 07 Apr 2025 23:48:49 GMT  
		Size: 208.0 MB (207956286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7df0f25bafe0c3c1973b597b568ac08a4db9366017044d23a10fe2e4537c812`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 114.6 KB (114626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47260128b74b04275aea21e96390a1a9ba06361b68069c5b2c7621e91b7031e`  
		Last Modified: Mon, 07 Apr 2025 23:48:36 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull openjdk@sha256:dd71ceb8b5487836df61fdbe5a84b59c4cdb3869ed35ddbb69371bda862e57ee
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.8 MB (328838463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c869babe348e53a5f396f46340f26a097243201129d1b6151bcb63476e0129e8`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Mon, 07 Apr 2025 23:08:36 GMT
SHELL [cmd /s /c]
# Mon, 07 Apr 2025 23:08:38 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Apr 2025 23:08:39 GMT
USER ContainerAdministrator
# Mon, 07 Apr 2025 23:09:03 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Apr 2025 23:09:04 GMT
USER ContainerUser
# Mon, 07 Apr 2025 23:09:05 GMT
ENV JAVA_VERSION=25-ea+17
# Mon, 07 Apr 2025 23:09:13 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Mon, 07 Apr 2025 23:09:20 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Apr 2025 23:09:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3adbaf979377b73e57263e4d7d7d043747229f2c660dbf1fe4a9195d55275e5`  
		Last Modified: Mon, 07 Apr 2025 23:09:25 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faab8d63e2abdb03b2416da6b024d2e95de95ec200aebfeb74664687291bb841`  
		Last Modified: Mon, 07 Apr 2025 23:09:25 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e2eee29df16a1094c6740eb398ec9c93c006d1aac0a694c9fe9e62cbc3eddd7`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e07608d484196bde6b105555c7f2d14700ea95678f31e0dae8a990357be11bd`  
		Last Modified: Mon, 07 Apr 2025 23:09:25 GMT  
		Size: 89.0 KB (88987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c902cb1dd92da13661f92160e6a3593d28b835fe1d3030518f325ed041d98d3`  
		Last Modified: Mon, 07 Apr 2025 23:09:23 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7792b329ce603fdd5018083b487afea475cd1c85dfbbac4ad1661622d1b187b3`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1342c9718f1fc7c6580c57fa6776ef39c8f0e41d846bf1befaba3fc7c95c3f`  
		Last Modified: Mon, 07 Apr 2025 23:09:34 GMT  
		Size: 208.0 MB (207954960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f750f0dc8e6cb688e9483d2939e06411f0a6ddea92ca37ad543f01c20a9e8f1`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 92.8 KB (92775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6380fd72ad226b5425f4b5c3eb515d88afd132e2e4ddfa9c7b684508156daac2`  
		Last Modified: Mon, 07 Apr 2025 23:09:24 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:25-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:2a5876f81ec1f7d214bf569d80e4df6635a7d59e448615a195e9f3e3802214cd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319338115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a724117dc3582608e5c60b6f5169c5f7fe880602ab859c4dc8eb11dd8939df44`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Mon, 07 Apr 2025 23:08:49 GMT
SHELL [cmd /s /c]
# Mon, 07 Apr 2025 23:08:51 GMT
ENV JAVA_HOME=C:\openjdk-25
# Mon, 07 Apr 2025 23:08:52 GMT
USER ContainerAdministrator
# Mon, 07 Apr 2025 23:09:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 07 Apr 2025 23:09:09 GMT
USER ContainerUser
# Mon, 07 Apr 2025 23:09:10 GMT
ENV JAVA_VERSION=25-ea+17
# Mon, 07 Apr 2025 23:09:21 GMT
COPY dir:31d4a08dd20e935927d81b33c56eb56ceaeead96529382a0c30c5f89fc836ee7 in C:\openjdk-25 
# Mon, 07 Apr 2025 23:09:28 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 07 Apr 2025 23:09:28 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97b4b64051b72c2bcdea71d22d8ee77929d05df2ec94e0a1ec06163f61733015`  
		Last Modified: Mon, 07 Apr 2025 23:09:33 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059db0481803d45332ad65c3aa6a9c08bd31d7bf4955bec319efce52c4c892e0`  
		Last Modified: Mon, 07 Apr 2025 23:09:32 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d415d2255eb357e2bae7c46e9ab8f462e7e9de72b6bb0a0d8c51abf707a1c7d6`  
		Last Modified: Mon, 07 Apr 2025 23:09:32 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18dc4f234054176c77fafafc98e4ef67a065bba8379df64381b53993c139a012`  
		Last Modified: Mon, 07 Apr 2025 23:09:32 GMT  
		Size: 66.8 KB (66833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4efe0e9d863d3e338a86706cbec7d3df163dabb9510d7b45e0b6a11bc07fba97`  
		Last Modified: Mon, 07 Apr 2025 23:09:31 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c2347137e2c31a210c944729dbfbeb926df82c2dad818426206a2d51731704b`  
		Last Modified: Mon, 07 Apr 2025 23:09:31 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d9bbd309267b883cd4abc7880033d73246899a07f333fc866ee3f59d4759ea1`  
		Last Modified: Mon, 07 Apr 2025 23:09:42 GMT  
		Size: 208.0 MB (207954388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3816918df3117de30bc65c0c544634515a00337cdd53d6a3559e75a58f7e00d`  
		Last Modified: Mon, 07 Apr 2025 23:09:32 GMT  
		Size: 4.4 MB (4403005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d53af0b26ed2ad50d8643d8453d3648102303713279d6d7d9f82384c67090cf6`  
		Last Modified: Mon, 07 Apr 2025 23:09:31 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
