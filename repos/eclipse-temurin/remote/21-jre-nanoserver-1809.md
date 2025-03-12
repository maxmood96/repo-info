## `eclipse-temurin:21-jre-nanoserver-1809`

```console
$ docker pull eclipse-temurin@sha256:2dc24cb4943351408429b7d5fbf23f0d551e9cadc7242b7b960ea293b8a275c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `eclipse-temurin:21-jre-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull eclipse-temurin@sha256:1332509bda2f2c8ca3afd0351f327521cf9dbdec518cb96477e437ad3d6ec335
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159294181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b52d811aea392bc6702042aee76f354d87c54e6c32fc73c85409c0cb8f1566`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Wed, 12 Mar 2025 19:17:31 GMT
SHELL [cmd /s /c]
# Wed, 12 Mar 2025 19:17:33 GMT
ENV JAVA_VERSION=jdk-21.0.6+7
# Wed, 12 Mar 2025 19:17:34 GMT
ENV JAVA_HOME=C:\openjdk-21
# Wed, 12 Mar 2025 19:17:34 GMT
USER ContainerAdministrator
# Wed, 12 Mar 2025 19:17:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 12 Mar 2025 19:17:38 GMT
USER ContainerUser
# Wed, 12 Mar 2025 19:17:42 GMT
COPY dir:c0b7c132c85049081486a93cd76fe016c559b0b921796f63592a768b082ae9e2 in C:\openjdk-21 
# Wed, 12 Mar 2025 19:17:46 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f348ec31fb415c72de1fe5d9bead7b72e79fdea52c1fbf873cfe2968a12f145`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a6e0db99e71cc00e09e21e082b4d2e7928a095680af042db76f80ebbe60bf5`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.0 KB (1041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea74402b9c0815bdd86961d6395a401a74b2722e949e5ec8a9ecffb75da687c7`  
		Last Modified: Wed, 12 Mar 2025 19:17:51 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a0cf7792a9544429a3fde9cac8e446ab42d27fb6ad8a7ab7f3c160dc602235`  
		Last Modified: Wed, 12 Mar 2025 19:17:49 GMT  
		Size: 1.0 KB (1046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5b33de4bf5cdd2254a4a1aa99e18f43624a57e757f71c8eaa02643cac3188e`  
		Last Modified: Wed, 12 Mar 2025 19:17:49 GMT  
		Size: 69.6 KB (69592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d005618b8d7f8b04b9d824a922f5ca5232ba93a7faaf06e249de24311ed421`  
		Last Modified: Wed, 12 Mar 2025 19:17:49 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5c40a5c05593d44dad5e15652e503eaaa28b8f002f086563b31ae55a65ec97`  
		Last Modified: Wed, 12 Mar 2025 19:17:55 GMT  
		Size: 48.9 MB (48940927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07a95225247050ce916d02689338c79c470f1db12d6061d864e773570cda584b`  
		Last Modified: Wed, 12 Mar 2025 19:17:50 GMT  
		Size: 3.4 MB (3370779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
