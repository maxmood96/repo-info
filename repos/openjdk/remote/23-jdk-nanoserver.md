## `openjdk:23-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:6e30a033742f9d08899ae61ef829473288512f08b81b40c11c55752a3e00517e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5576; amd64

### `openjdk:23-jdk-nanoserver` - windows version 10.0.17763.5576; amd64

```console
$ docker pull openjdk@sha256:31495cbe657647621a31604112cf81392ffc3567f5b4b051678b786b35c4f3ea
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.4 MB (307351956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:362c309a80ca8fdbed662d5ee5476d849128f64899d165139c935dd9feed14c2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Mar 2024 00:43:57 GMT
RUN Apply image 10.0.17763.5576
# Wed, 13 Mar 2024 02:11:16 GMT
SHELL [cmd /s /c]
# Wed, 13 Mar 2024 02:11:17 GMT
ENV JAVA_HOME=C:\openjdk-23
# Wed, 13 Mar 2024 02:11:17 GMT
USER ContainerAdministrator
# Wed, 13 Mar 2024 02:11:20 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Mar 2024 02:11:20 GMT
USER ContainerUser
# Wed, 13 Mar 2024 02:11:20 GMT
ENV JAVA_VERSION=23-ea+13
# Wed, 13 Mar 2024 02:11:28 GMT
COPY dir:074f54b878561a19d242c8e2a7ebf93761c9ac51677c094a49834e516e5e10e3 in C:\openjdk-23 
# Wed, 13 Mar 2024 02:11:34 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 13 Mar 2024 02:11:35 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7d1978583f4a1122c5128a802637410697b681e7aa97b596dcb589b088c0b85d`  
		Last Modified: Tue, 12 Mar 2024 19:41:51 GMT  
		Size: 104.6 MB (104620103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afd50d59495df879e330b3d826852761b4b1ad45af196865c8b1ab17693812b`  
		Last Modified: Wed, 13 Mar 2024 02:11:42 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb5d7cdf56471879188e26993d3f89cb6564fb0351f5a1d55f93c3498ce9b3d`  
		Last Modified: Wed, 13 Mar 2024 02:11:42 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5809f2b202c18a7801a830e5ed4a3f9353672ffee4a9ee91c11a7f14619fe6da`  
		Last Modified: Wed, 13 Mar 2024 02:11:41 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017a0d3136bac22ade09c81a7d3f5e60137610435b335a97806d405b13f75561`  
		Last Modified: Wed, 13 Mar 2024 02:11:41 GMT  
		Size: 71.5 KB (71459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a7f3c32b0ad67336cf00a0c7998a2ac2b4707eb1ee2fda23fc25b64e21e93c`  
		Last Modified: Wed, 13 Mar 2024 02:11:39 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ee90c4084bc8ada98cfc93d03f56ffd1f93fd48af6a34fd9f0f603d685b1bef`  
		Last Modified: Wed, 13 Mar 2024 02:11:39 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd913bb647c9d72c91e80434c2cbc9c96931de79487b74ec7fc22f71a318018`  
		Last Modified: Wed, 13 Mar 2024 02:11:52 GMT  
		Size: 197.2 MB (197154422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709acc8201845ea8d9793ada7fbbae5a5ae4d00eee3c74e72c5b5ccbd552dee1`  
		Last Modified: Wed, 13 Mar 2024 02:11:40 GMT  
		Size: 5.5 MB (5499728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f3593d3be5b4c49183687b2974dcceaca5c57fadd48ca85d83c88b4cad568a5`  
		Last Modified: Wed, 13 Mar 2024 02:11:39 GMT  
		Size: 1.0 KB (1042 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
