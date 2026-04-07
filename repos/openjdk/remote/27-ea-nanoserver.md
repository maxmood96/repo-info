## `openjdk:27-ea-nanoserver`

```console
$ docker pull openjdk@sha256:ac0f9603d460bbbe33c6723ae6991eb868afae1ea19c80baa0e999d724f1ed08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `openjdk:27-ea-nanoserver` - windows version 10.0.26100.32522; amd64

```console
$ docker pull openjdk@sha256:6284b729a40c159a1c208ad4a04a42c055d2d673dbffec24141c160a65267055
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.4 MB (424360829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a92dc0c96d93d3d8b9aedab3af94d2109408040a7b4855128f40ce65f4ff44e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Mar 2026 01:45:55 GMT
RUN Apply image 10.0.26100.32522
# Mon, 06 Apr 2026 18:50:32 GMT
SHELL [cmd /s /c]
# Mon, 06 Apr 2026 18:50:33 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 06 Apr 2026 18:50:34 GMT
USER ContainerAdministrator
# Mon, 06 Apr 2026 18:50:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Apr 2026 18:50:46 GMT
USER ContainerUser
# Mon, 06 Apr 2026 18:50:47 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:51:45 GMT
COPY dir:55270656ab5feced27f5cb37a9607ccdf4477020b36ca2637f5afcedca09c62e in C:\openjdk-27 
# Mon, 06 Apr 2026 18:51:55 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Apr 2026 18:51:55 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:06fab7822816d5f43d6835d07ac8db280fdf81384187f36d8dc43bbb7064a76d`  
		Last Modified: Tue, 10 Mar 2026 20:41:46 GMT  
		Size: 199.4 MB (199409325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca15b088faeff2cfe9e130485d2d9a221329914b77166bf77c15655c70b6ea49`  
		Last Modified: Mon, 06 Apr 2026 18:52:01 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bc5a0884d786d3d71224663f73ce21f216d5ffa7680f8ba4d100c7ee1dc0dc1`  
		Last Modified: Mon, 06 Apr 2026 18:52:01 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:074429098f87aabcdb840549fe260156b369550404b68980daa739c6a1aaac46`  
		Last Modified: Mon, 06 Apr 2026 18:52:00 GMT  
		Size: 1.1 KB (1094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f902af4d0e88abc6d52a74db6f02d627cb6a57f6463a5805a8ae47bb90ac8112`  
		Last Modified: Mon, 06 Apr 2026 18:52:00 GMT  
		Size: 84.8 KB (84764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:161697602044aa6ab408c3554e78a5dd8eb2d454f54b8c3b78b395e2c501a013`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a997eeb80e711c575653f5fa9c0c27c70fe110e7bf59318442e1c1e079192d`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 1.0 KB (1047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb0627295a0b6d2b263f47e20e96b3b4b92d88fcb0549c2fe4d4414bcb5d61c`  
		Last Modified: Mon, 06 Apr 2026 18:52:16 GMT  
		Size: 224.7 MB (224745852 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e93da66049b756117951e76af42d482082222d1b0f54be6a1fe60a5a216fe7f`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 114.5 KB (114467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4da22da6547026c68f8eefd588f78f6259c2854b3f8f55826174813ed693d897`  
		Last Modified: Mon, 06 Apr 2026 18:51:59 GMT  
		Size: 1.1 KB (1082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `openjdk:27-ea-nanoserver` - windows version 10.0.20348.4893; amd64

```console
$ docker pull openjdk@sha256:6def18358dee1a28d8000d949f57f8c29746c3481c25fff21220823f35250a01
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351614396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8e1810172be6904e464f2b09783cec674a045e5584af21ab84b4d95344c68d0`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 03 Mar 2026 22:33:04 GMT
RUN Apply image 10.0.20348.4893
# Mon, 06 Apr 2026 18:50:33 GMT
SHELL [cmd /s /c]
# Mon, 06 Apr 2026 18:50:33 GMT
ENV JAVA_HOME=C:\openjdk-27
# Mon, 06 Apr 2026 18:50:34 GMT
USER ContainerAdministrator
# Mon, 06 Apr 2026 18:50:42 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 06 Apr 2026 18:50:43 GMT
USER ContainerUser
# Mon, 06 Apr 2026 18:50:44 GMT
ENV JAVA_VERSION=27-ea+16
# Mon, 06 Apr 2026 18:52:26 GMT
COPY dir:55270656ab5feced27f5cb37a9607ccdf4477020b36ca2637f5afcedca09c62e in C:\openjdk-27 
# Mon, 06 Apr 2026 18:52:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 06 Apr 2026 18:52:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:621e4ed9fe406fab7f834f69927b2244d740ddc4eeb8985e9fc776f2f4ff0420`  
		Last Modified: Tue, 10 Mar 2026 21:55:56 GMT  
		Size: 126.7 MB (126650500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9d2930097ed273eb2ee4c08dd2d4374740c260827d105d346eb7350019f664a`  
		Last Modified: Mon, 06 Apr 2026 18:52:46 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43f11810d1c434703228b4450ddf8521994bb89a31a26ec534ae9d191ace3ee0`  
		Last Modified: Mon, 06 Apr 2026 18:52:46 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30013cc49ca4fc2da2df51d34fb0024bb81784de9d8508ac21279e44b431c288`  
		Last Modified: Mon, 06 Apr 2026 18:52:46 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541ba62b4de61f2a477c77a6fe896fc8173e255ceedc1983404ca2b556ab2eb5`  
		Last Modified: Mon, 06 Apr 2026 18:52:46 GMT  
		Size: 71.1 KB (71103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e63abf07b9031e13341fadee1aabfb2e03359eb26542503b3ff9c15cffc44c`  
		Last Modified: Mon, 06 Apr 2026 18:52:45 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c9a7a12dcd6f025ad6580496a4375b17d2b40b93bf47df0d7e696fedb12ad6e`  
		Last Modified: Mon, 06 Apr 2026 18:52:45 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bedbb3dd8a934fcacce7ea02d75127e6f79dcdc354ed279f9a718f06e686a53`  
		Last Modified: Mon, 06 Apr 2026 18:53:01 GMT  
		Size: 224.7 MB (224746072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77087ee9d726fe1556436a702c3ac3c3a41238850fd80f702038b555676fea0a`  
		Last Modified: Mon, 06 Apr 2026 18:52:45 GMT  
		Size: 140.3 KB (140308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e308c6ffb96e6e9cea13c2d930ae33d368399ec72c58b8d3f2fd113ef546f0f0`  
		Last Modified: Mon, 06 Apr 2026 18:52:45 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
