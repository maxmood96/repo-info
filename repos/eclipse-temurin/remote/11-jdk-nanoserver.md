## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:f62685d7576354e8d8fc9c1591114c84e3cc60f174d88af857c6d9e9657a4883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3775; amd64
	-	windows version 10.0.20348.3453; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.3775; amd64

```console
$ docker pull eclipse-temurin@sha256:400952a872d49a6fffee7a7546fa2247a3459a2e0c3de76288bc44ee84fd1f2d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384878741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4f050a749d23d4d0b8a1648b2856c69bcf1bac560ce78052dd6d28b342d77d4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Apr 2025 07:26:08 GMT
RUN Apply image 10.0.26100.3775
# Wed, 09 Apr 2025 01:18:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 01:18:34 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 01:18:35 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 01:18:37 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 01:18:41 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 01:18:42 GMT
USER ContainerUser
# Wed, 09 Apr 2025 01:18:51 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 09 Apr 2025 01:18:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 01:19:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:79b2ed45f890e91d23d7d22491a8fb6909c9268c668dc6a0e3b40131da02ed74`  
		Last Modified: Wed, 09 Apr 2025 00:36:30 GMT  
		Size: 190.1 MB (190113206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dcbc248e2fe87185099346d851ee13f4b4cf01d5a1bc19965c5077f53a6ba7`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab6014ac3080da2617258e6b355f19fb22beb231a26f8593309c6c9ef8b4dd52`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f052e6ee89dedf32994ac0627ca7353e80c177d975ba2d3f2fd37d7d20eca2c`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038ca4752a6776aff58311712fde24e2884eb2e5476b75b81233cff4bcb6ae15`  
		Last Modified: Wed, 09 Apr 2025 01:19:04 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b47d40a0e8b97141cd32b122897cb409d23b64ca23a0734cb1a4abb700e6d925`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 76.5 KB (76527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0716bd0bae9252c84f5af88998e8175726a0e4287b1155381d4b81e2e78e2bd9`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84f232d7ff09612987060b1f2d243b8ce1318e0670fcc78f8831c61222d32b8c`  
		Last Modified: Wed, 09 Apr 2025 01:19:13 GMT  
		Size: 194.6 MB (194557425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2447486d86c56788eb90bfaf44025ef54f05b4c8e339e9d3b6e3f62e68021d`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 125.4 KB (125378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102fb78643a5d0258004617e920007ef0b1cee8f154cefb79b54e49bd5f08ae3`  
		Last Modified: Wed, 09 Apr 2025 01:19:03 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.3453; amd64

```console
$ docker pull eclipse-temurin@sha256:9f50659a33dc7cb06ad87fd8f5bfa854d85519b29ea3c14ddff8003ed23ef9bb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.5 MB (315492835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf0e1ae6ba8686282d6b45123e25b213a46c61833bc56266ed8d62ec0f5d6b1a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 04 Apr 2025 22:57:50 GMT
RUN Apply image 10.0.20348.3453
# Wed, 09 Apr 2025 04:17:47 GMT
SHELL [cmd /s /c]
# Wed, 09 Apr 2025 04:17:48 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 09 Apr 2025 04:17:49 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 09 Apr 2025 04:17:49 GMT
USER ContainerAdministrator
# Wed, 09 Apr 2025 04:17:52 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 09 Apr 2025 04:17:52 GMT
USER ContainerUser
# Wed, 09 Apr 2025 04:17:59 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 09 Apr 2025 04:18:05 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 09 Apr 2025 04:18:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5caa30147a287e99992660f7f85276c53fe3299503a06c47d476387410721453`  
		Last Modified: Wed, 09 Apr 2025 01:13:36 GMT  
		Size: 120.7 MB (120736312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9683628ca8845013c48a6027efaf6727a5b90919f644f3a02262d9fee471c59`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39f6bd67fe2292c2a37e1e43d9e5d59f5c8a922ec8d8aeedeaafef6879049327`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c113151fd89a92d8bb5b086ee708dc12356213b4e621a45a568bc22e7bf0044`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc2fb458557294e152c19911ac0bb71350a4182bdb2d4f00778e3a43fd9da5bc`  
		Last Modified: Wed, 09 Apr 2025 04:18:12 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f856d7a5a393e68b03ac916bc7f168c6ae1e1ae90831dd149e7115bb44fac1d4`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 77.0 KB (76999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4f67392eb965eea705b34bdc7ac9852cd7ee6d9effb7bcb97b83c3855a12cb`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef0e5d4065ea3bac5e0ab6fe81e59216c88938496a03b4d7c3cff98db5807c0`  
		Last Modified: Wed, 09 Apr 2025 04:18:20 GMT  
		Size: 194.6 MB (194555115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b857b1e25e202212bc10cf8fabfadcd877d1eb55ffac7e4dfd9e9f0f82eb05b`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 118.2 KB (118241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf70b98fe957ebc27ba955c22340265fae75e9528c27bb503018aa0f201114e`  
		Last Modified: Wed, 09 Apr 2025 04:18:10 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:3d89f3c73bb09669d906046eadd1abde5b15cbe5c02dba8c774c6f6c3e2782c4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.6 MB (301643792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d767b69fb2669a8353b273a8312ac2035d6c1d23980587200795656e3d720d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:23:07 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:23:09 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 19:23:09 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Mar 2025 19:23:10 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:23:12 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:23:12 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:23:20 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 12 Mar 2025 19:23:24 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:23:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3b33a3bb4001732af2969450134eea7a145ad85aac9499f48aed459b483f006`  
		Last Modified: Wed, 12 Mar 2025 19:23:31 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:153d970595e5b9cca45e6e377c1945c413433f813053de79d6811a46a829106e`  
		Last Modified: Wed, 12 Mar 2025 19:23:31 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa64753f340b97875964e6fce87a4a6e6c68bbef10ba765fa4f2b211d6028157`  
		Last Modified: Wed, 12 Mar 2025 19:23:31 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b9ec4440a54170c51cb602e13e37399279a2bd395bae08bb3fb160b3cbc7e1`  
		Last Modified: Wed, 12 Mar 2025 19:23:30 GMT  
		Size: 1.1 KB (1077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab14f4fbbe20856a44de30ae7cd939dfb521e136f6632ff4d5c6592ea434358`  
		Last Modified: Wed, 12 Mar 2025 19:23:29 GMT  
		Size: 69.0 KB (69002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b1fc015a48b0502d3fbf00a1c317da6e3ed529ccbdb0b5c5b5496605de7f39`  
		Last Modified: Wed, 12 Mar 2025 19:23:29 GMT  
		Size: 1.1 KB (1076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d8f3ffac34e6134b1daec252dcab099a05fe7ffb84303940c503ef9223d013`  
		Last Modified: Wed, 12 Mar 2025 19:23:39 GMT  
		Size: 194.6 MB (194556473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c5303af7ece69a5555a56634714aadf182fd4bddb04de9a3b3d2b5474fa5133`  
		Last Modified: Wed, 12 Mar 2025 19:23:29 GMT  
		Size: 104.3 KB (104290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df01380aec47152cd2a1c7f6064b765e9cf0884327357bc2cf6cd1e1f452379d`  
		Last Modified: Wed, 12 Mar 2025 19:23:29 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
