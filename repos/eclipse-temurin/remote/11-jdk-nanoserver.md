## `eclipse-temurin:11-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:9f15fe5901e99b9ce319dbc5c450fc3613d90479258802d4caaf37186f20469b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.26100.3476; amd64

```console
$ docker pull eclipse-temurin@sha256:2908c11866f8e587e0f1e8b4f2ec3daf936d0ff1d2c0e2d8a6c381ee085eab6d
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **401.1 MB (401055879 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd2506bb66a4fac0d391bc23efb3a6266fb7021a1d3d96da66e16e9d24fb41e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Mar 2025 05:48:38 GMT
RUN Apply image 10.0.26100.3476
# Wed, 12 Mar 2025 19:17:04 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:05 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 19:17:06 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Mar 2025 19:17:06 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:09 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:09 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:16 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 12 Mar 2025 19:17:23 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:17:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6008a43ec9274f69b461027b7f4e2fe6a71387d40072c0b5b4f0dbbfa688d8a5`  
		Last Modified: Wed, 12 Mar 2025 18:43:31 GMT  
		Size: 206.3 MB (206302205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad7d153dfbd73dbd7445361ee4abd0c925b3782b941f2cb10da810deae12f18f`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.1 KB (1101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bae8217fc4e3f853c1d8e924733ec62171a6351c553cdd9ef1c40902c481638`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb5bad9e1dad86eed81cb376a494a6adb3986943ef027566aec156c1f249dc43`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.1 KB (1053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73346353498cabcbc9aa5cdc24f14a05bbcd114a2f7e035ee001eb515310770`  
		Last Modified: Wed, 12 Mar 2025 19:17:29 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8eb841fc19f548316554c038c90da823b0289452e18d69322a93a44f89351dfb`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 76.2 KB (76156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ca5eef1acf6ac6b58b44ce0092be89738768ea5ca4f18939a5d57af7037e0b9`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098108396781f50b453dc7320c678473cdcd355a8526a655d1a0398671d1b0ed`  
		Last Modified: Wed, 12 Mar 2025 19:17:48 GMT  
		Size: 194.6 MB (194556941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea2850a8379c200c7c2ed1c174013a31a2cf3fb0dffa2c82fb9d7b46ae3c969`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 114.2 KB (114227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc21f030bc45b02fced89861dfabb43561de952018859b1ddb778dd713b9559`  
		Last Modified: Wed, 12 Mar 2025 19:17:27 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:11-jdk-nanoserver` - windows version 10.0.20348.3328; amd64

```console
$ docker pull eclipse-temurin@sha256:37e7bccc754da3cfe8c4943c0801ab00468afe2678121a2df9a9f1ffa0d36393
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **315.4 MB (315440651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56af9c22ad6e76af64fd50d5db7c683df9f5a7fdd9761626fdfd64c04984889a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 06 Mar 2025 10:30:39 GMT
RUN Apply image 10.0.20348.3328
# Wed, 12 Mar 2025 19:19:31 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:19:31 GMT
ENV JAVA_VERSION=jdk-11.0.26+4
# Wed, 12 Mar 2025 19:19:32 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 12 Mar 2025 19:19:32 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:19:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:19:35 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:19:41 GMT
COPY dir:9a97e9a1ce762bb8542962ee0a2b0ca6fa379668e092b80acfc01b297b3b57a6 in C:\openjdk-11 
# Wed, 12 Mar 2025 19:19:46 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Mar 2025 19:19:47 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:47ec0d45ee7716f773dfebb62d84eb3893d3af9baf9c799960566b016a17e330`  
		Last Modified: Wed, 12 Mar 2025 02:22:56 GMT  
		Size: 120.7 MB (120695547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74c895280976ae6354815213c06d9eea68770de9bec20516b5b7e0646d8a801f`  
		Last Modified: Wed, 12 Mar 2025 19:19:51 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f26ba0f1267b81cb87df55668f8d09d88f55e738fcd0552c95d5efe77358c4a0`  
		Last Modified: Wed, 12 Mar 2025 19:19:51 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62114677ec808afb9e5a132ebd194815994b1f124c813490674f15436df82a4`  
		Last Modified: Wed, 12 Mar 2025 19:19:51 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675b3dd780e5096ee16f951241f7a52091bd9badb4f2e1046fbba6310d1e10a9`  
		Last Modified: Wed, 12 Mar 2025 19:19:51 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d6295f4f8a40a8af16bcde72c33524b90b873bb9eb0a35f08a4b1f7acaf05e`  
		Last Modified: Wed, 12 Mar 2025 19:19:50 GMT  
		Size: 76.8 KB (76790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35ccc58047e026d356e52b354194949dcbad5da9d938f3683319fd5e9ce685a8`  
		Last Modified: Wed, 12 Mar 2025 19:19:50 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f95aafd3f142c84bb4dbd7d5d7e62e6053aced54cee8f4ed7da7c20ea821616a`  
		Last Modified: Wed, 12 Mar 2025 19:20:00 GMT  
		Size: 194.6 MB (194554754 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0f0d49341e4fef611efaa49ffb1f475ece487562255894ae15606ab6923b451`  
		Last Modified: Wed, 12 Mar 2025 19:19:50 GMT  
		Size: 107.4 KB (107373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0308eba8d8f99b0ded3384b5e76fe75ca385444ba728055b8b14cbf9ed1d6d`  
		Last Modified: Wed, 12 Mar 2025 19:19:50 GMT  
		Size: 1.0 KB (1033 bytes)  
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
