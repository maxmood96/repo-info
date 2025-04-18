## `eclipse-temurin:24-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:b05c7317d7fee940c1c9406aca84224ed0b2487ab9162e777d85468370ac1e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.26100.3781; amd64

```console
$ docker pull eclipse-temurin@sha256:66862bcfb0f243d2f5cd85485cb9b82a6c4ee0b2b6836dfbccd7307cd36c4fb4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.7 MB (327696597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57177dfc0c908e26f1ad9af7e53fd61b34580e44f6552016b3ecf638acb5e744`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 09:41:29 GMT
RUN Apply image 10.0.26100.3781
# Fri, 18 Apr 2025 04:14:49 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:14:51 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:14:52 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:14:53 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:14:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:14:58 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:15:04 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:15:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:15:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c012166dfdb57168c954f830d80f494e556a2c597b84901e39aefb605b5e1a02`  
		Last Modified: Thu, 17 Apr 2025 02:52:17 GMT  
		Size: 190.1 MB (190142038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2847c9d24d72f635436e018a817bfbec8c004ed18970e71826941c7c06e8173a`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7f69cf3813ea330337df5b524b277303dbd6b44d5cf996b2aabb2e542d3efce`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d629fe854aa08d21b8cc66eec33e28314d6f0d98af0a15e08d6d2e273246fc`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0155bbcf02f70f930e7c15b3f33e416c43116ba99d33218153468c84c14fa929`  
		Last Modified: Fri, 18 Apr 2025 04:15:19 GMT  
		Size: 1.1 KB (1060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97443c3e447a99a0eba23a707ee02d6c31368e685c664103f7d3429012855259`  
		Last Modified: Fri, 18 Apr 2025 04:15:17 GMT  
		Size: 77.3 KB (77275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b7153c90f60c5c041e07de2314611dad556e048fdff2e1d59d0eda05ec793a`  
		Last Modified: Fri, 18 Apr 2025 04:15:17 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4969286679221f97709a9c75be50d743be72c627e9cda1fac0d59e8242053e8`  
		Last Modified: Fri, 18 Apr 2025 04:15:28 GMT  
		Size: 137.4 MB (137355935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92beb34503347837b120bdcf96457002b8fc970a43f655e0b508fa761d3d5351`  
		Last Modified: Fri, 18 Apr 2025 04:15:18 GMT  
		Size: 115.0 KB (115002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667f76f952d48a1f8235d4ebf8f1ef9e43b5bdf0381e3135ae37d492d23aadd0`  
		Last Modified: Fri, 18 Apr 2025 04:15:17 GMT  
		Size: 1.1 KB (1058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.20348.3566; amd64

```console
$ docker pull eclipse-temurin@sha256:3523229d86fbba79fb8660ac0d861f91bf6183ea471793cdb0e39d141ef9fdea
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.1 MB (260084739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0243202d486fd302bd69686d41bd3881e8278f3b549db8128920da54baf4b114`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 16 Apr 2025 03:28:26 GMT
RUN Apply image 10.0.20348.3566
# Fri, 18 Apr 2025 04:18:22 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:18:23 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:18:24 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:18:25 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:18:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:18:28 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:18:34 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:18:40 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:18:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:905464f5b09ec7543cfd4984311153c5e327937892d0e49e145f6b363cf68441`  
		Last Modified: Wed, 16 Apr 2025 23:30:29 GMT  
		Size: 122.5 MB (122539088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa7042c2e4442fc6e6b29d5c1cd91e3c0c2b415e76ac3de3430a75fbc20c42a3`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a4db1978185809159ecf4eeb6510d679d6d362df6f190d4a9f5cda96d8f317`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bc4cd9445867348020310707d919c65754d4cbf4f01c64ecb20e138ff82d3d0`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89d79de9c9e8dfda389edfe81c84a25648e1139adb3acd154430915852adb86b`  
		Last Modified: Fri, 18 Apr 2025 04:18:44 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9dacb06b332fdfa955837a963f1204b25922e8392334c834f7c81b1b47009a4`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 77.0 KB (77022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60671a14b65fe221c93a418e3f485aa2d838de719ff1a0b0c1e47d045ffb06e5`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23e0bfcc428513c565d86a0962b1663f29b4c68c911091abe5aa69d15a4a959`  
		Last Modified: Fri, 18 Apr 2025 04:18:53 GMT  
		Size: 137.4 MB (137355442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590ded974672f778e8ca546a5b6e682734bff3a240e71c53e0635538ade89829`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 107.0 KB (107001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d3723415a88bbee57fbbc0a52a96b6b8890db7578c6cac6a4b7744ef81f7673`  
		Last Modified: Fri, 18 Apr 2025 04:18:43 GMT  
		Size: 1.0 KB (1031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:24-jdk-nanoserver` - windows version 10.0.17763.7249; amd64

```console
$ docker pull eclipse-temurin@sha256:d03ec905c2af0c572ec248810352bf78b77184ca5f7582f1c1cef168ac95a0cf
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **250.6 MB (250601674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f466fd20884eb41ddc4ee6ee7251c5f5e1c49b1ec36d492fde9bb23558a0acf`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 15 Apr 2025 01:30:17 GMT
RUN Apply image 10.0.17763.7249
# Fri, 18 Apr 2025 04:12:09 GMT
SHELL [cmd /s /c]
# Fri, 18 Apr 2025 04:12:10 GMT
ENV JAVA_VERSION=jdk-24+36
# Fri, 18 Apr 2025 04:12:11 GMT
ENV JAVA_HOME=C:\openjdk-24
# Fri, 18 Apr 2025 04:12:11 GMT
USER ContainerAdministrator
# Fri, 18 Apr 2025 04:12:14 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Fri, 18 Apr 2025 04:12:14 GMT
USER ContainerUser
# Fri, 18 Apr 2025 04:12:20 GMT
COPY dir:82098476e422c0fd1b27846be91131b5a5073542830e51603132b80cd94d4318 in C:\openjdk-24 
# Fri, 18 Apr 2025 04:12:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 18 Apr 2025 04:12:26 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:559b23b3f8a9b205cc3c87a98df1233325878f8360cece22c8822b2a5fc8731a`  
		Last Modified: Wed, 16 Apr 2025 23:46:26 GMT  
		Size: 108.8 MB (108752293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aaaa7043bc969ffd10e73283f955d6a41ef6b4cc004dfaec79839e2c5e201890`  
		Last Modified: Fri, 18 Apr 2025 04:12:33 GMT  
		Size: 1.0 KB (1026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c784adec165e2853397805404661a906451a492ceceed1b33c52e5825913412f`  
		Last Modified: Fri, 18 Apr 2025 04:12:32 GMT  
		Size: 1.0 KB (1034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ec9b2136e68954d7a1c6c8e8b488b6450a5f02653a9eb63b17e3a03a8ccf50`  
		Last Modified: Fri, 18 Apr 2025 04:12:32 GMT  
		Size: 1.1 KB (1059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3faa0ac4facd6bcbb529c6b71ef345a89551c460906353f8871618dabfe0ca`  
		Last Modified: Fri, 18 Apr 2025 04:12:32 GMT  
		Size: 1.0 KB (1023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab36e2dd35a5a3a0ae469a69c596eeb82a7a63737bf475a21974ff16d029e9f9`  
		Last Modified: Fri, 18 Apr 2025 04:12:30 GMT  
		Size: 70.7 KB (70723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d04fc37255c2202e815e88873a4ed11f60974781e317e43719c45d908d11ecc`  
		Last Modified: Fri, 18 Apr 2025 04:12:30 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a53c4947b164e13cddb0bd2293a11f7b7df70d8ddb4dc7a60adf62848b26440b`  
		Last Modified: Fri, 18 Apr 2025 04:12:40 GMT  
		Size: 137.4 MB (137355533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec0eaa25554856dd4582d7855999938d374d2e81dc7b686c6e710004e7aa923`  
		Last Modified: Fri, 18 Apr 2025 04:12:31 GMT  
		Size: 4.4 MB (4416931 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287a79f75770626b36b448b84bddb8844362830e5f5eeeac19a8ff463961f09a`  
		Last Modified: Fri, 18 Apr 2025 04:12:30 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
