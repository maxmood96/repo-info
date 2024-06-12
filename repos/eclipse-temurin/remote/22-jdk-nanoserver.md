## `eclipse-temurin:22-jdk-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:7d6edddf6db4b252a2021a41b8aa71024c0f1a3feafb150161ebbbcfece23767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2527; amd64
	-	windows version 10.0.17763.5936; amd64

### `eclipse-temurin:22-jdk-nanoserver` - windows version 10.0.20348.2527; amd64

```console
$ docker pull eclipse-temurin@sha256:344250853f8b9c0f4387f774c811d19b64517af94f1548d9ab88ce7fc38fa8cb
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320689198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6ee38136030be882f06d03dc9fa5c997d32d818225525892af3603b9850645`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 08:41:16 GMT
RUN Apply image 10.0.20348.2527
# Wed, 12 Jun 2024 18:27:44 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:33:03 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 12 Jun 2024 18:33:03 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 12 Jun 2024 18:33:04 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:33:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:33:14 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:33:29 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 12 Jun 2024 18:33:43 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:33:43 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f9825bcd6f9509654677a23b5fa1d32b32e1e32ff51914ebfaa76d5e79c22b50`  
		Last Modified: Wed, 12 Jun 2024 02:27:19 GMT  
		Size: 120.5 MB (120488969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7ae17666c85b2b00f8e5aa24951a59f0b01a1eb41704faa32e1282e0f0ef217`  
		Last Modified: Wed, 12 Jun 2024 18:52:48 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ca9f23647c25d7ffd20f203fcc462773b7d40de69c1bb521a1a311ee563c610`  
		Last Modified: Wed, 12 Jun 2024 18:55:53 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6068732ef9525b4d660e36241562b7663fcc06e9e7541457049db99d6a6bd30`  
		Last Modified: Wed, 12 Jun 2024 18:55:53 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52a68d0423b89de4fa87cb724e47ba677a572ca5bd4fd6ff8d879c0a125b590`  
		Last Modified: Wed, 12 Jun 2024 18:55:53 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5bc581e87d49026aa90c2b0578d55c33da5b05e161cee3750d169e901261b4b`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 76.3 KB (76333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccc1207aa918c5a176ec3532b5fa6b9fea27428c20c03119c289a4521f6d5bb5`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb22d5df619e5c637b75ca6fd2a63c32bc0fc846f482d3e22e6acae2195ab635`  
		Last Modified: Wed, 12 Jun 2024 18:56:10 GMT  
		Size: 200.1 MB (200055718 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:705f6ac78c0fff0c08d0bf62468ea10d4b878f9cfd2f9ad11eba38753b5f7ea4`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 61.2 KB (61218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7314bcbdbe45007b5b5652cc194e45aa89b2b3b05952a43fa833e7da4c4045f4`  
		Last Modified: Wed, 12 Jun 2024 18:55:51 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:22-jdk-nanoserver` - windows version 10.0.17763.5936; amd64

```console
$ docker pull eclipse-temurin@sha256:f799cee5a3959bb4feefede2b7eac054e45265a8a02b2785b93d021b36780458
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.0 MB (358998144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be221dd6667458426a20d2fe091345810dd9e714ccd488c8feb2320ec247058d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 07 Jun 2024 10:54:05 GMT
RUN Apply image 10.0.17763.5936
# Wed, 12 Jun 2024 17:41:08 GMT
SHELL [cmd /s /c]
# Wed, 12 Jun 2024 18:22:06 GMT
ENV JAVA_VERSION=jdk-22.0.1+8
# Wed, 12 Jun 2024 18:22:06 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 12 Jun 2024 18:22:07 GMT
USER ContainerAdministrator
# Wed, 12 Jun 2024 18:22:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Jun 2024 18:22:16 GMT
USER ContainerUser
# Wed, 12 Jun 2024 18:22:33 GMT
COPY dir:b848142647370c7b57f8798114952350d05bf467cc96eb22cf5219409c8a4580 in C:\openjdk-22 
# Wed, 12 Jun 2024 18:22:44 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 12 Jun 2024 18:22:45 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4f703ea968d7f7434cf61e5d835cb3c507a6364ff8c7b3b96b73391b22115615`  
		Last Modified: Tue, 11 Jun 2024 20:35:02 GMT  
		Size: 155.0 MB (155033193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce076c01ab33a997d8fa4a6a49752f31455fef6df331991ad3b3736b3567321`  
		Last Modified: Wed, 12 Jun 2024 18:40:43 GMT  
		Size: 1.2 KB (1181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d5bb9e22f72bbccf429aadef40dc26c849c616be19af7360d07022b9c6e3555`  
		Last Modified: Wed, 12 Jun 2024 18:51:22 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5cae84b96e4a481431f172fff202189402b245b163ddd7feac8e000d2bf81b7`  
		Last Modified: Wed, 12 Jun 2024 18:51:22 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d74170a35e66cab58f46036320f076bcec608c8b45f1f28ba32d5535e5ac73f8`  
		Last Modified: Wed, 12 Jun 2024 18:51:22 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c3e9274ed02b839b87962b770ca3f42c9422727dd32d2030fefbbc512312cae`  
		Last Modified: Wed, 12 Jun 2024 18:51:20 GMT  
		Size: 67.6 KB (67579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39a6f4595ad9de5446ea5c7999b3706deed6381732a01ecd3415d1eaf4e2c2cb`  
		Last Modified: Wed, 12 Jun 2024 18:51:20 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e9e26a10633904da5108cc6816379c7471c5420325e3e9d9ea6e7742f969efd`  
		Last Modified: Wed, 12 Jun 2024 18:51:39 GMT  
		Size: 200.1 MB (200055592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ac234ec7aad62789894162a11b886036b1dd780b9699cf512760a1b0ea7e920`  
		Last Modified: Wed, 12 Jun 2024 18:51:21 GMT  
		Size: 3.8 MB (3834813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad53d84953cb327a59748df70d837de19cbc7e28ee56a394dac308065f4741e1`  
		Last Modified: Wed, 12 Jun 2024 18:51:20 GMT  
		Size: 1.1 KB (1134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
