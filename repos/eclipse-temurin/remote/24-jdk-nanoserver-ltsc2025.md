## `eclipse-temurin:24-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:cfd3c64d75812de6b0006d37ae9515d7f17ddb55b1cd56192c1f1fa7ba5c85f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.3781; amd64

### `eclipse-temurin:24-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.3781; amd64

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
