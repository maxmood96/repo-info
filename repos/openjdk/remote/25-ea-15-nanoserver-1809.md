## `openjdk:25-ea-15-nanoserver-1809`

```console
$ docker pull openjdk@sha256:5a74206274c520438ac1441cc01f8f88f4b7ee054761e8f2633772d031da7cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-15-nanoserver-1809` - windows version 10.0.17763.7009; amd64

```console
$ docker pull openjdk@sha256:977e258f2f76e0e00f2af4aa2d9afcd6d4ca70e1385da1b545572778ab9c0ec5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.9 MB (318906744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcbed0d385c24dbe0b318f0ce521a16dc1b65f887a9de2c998668d8b43977f71`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 05 Mar 2025 21:54:26 GMT
RUN Apply image 10.0.17763.7009
# Fri, 21 Mar 2025 18:15:20 GMT
SHELL [cmd /s /c]
# Fri, 21 Mar 2025 18:15:22 GMT
ENV JAVA_HOME=C:\openjdk-25
# Fri, 21 Mar 2025 18:15:22 GMT
USER ContainerAdministrator
# Fri, 21 Mar 2025 18:15:24 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Fri, 21 Mar 2025 18:15:25 GMT
USER ContainerUser
# Fri, 21 Mar 2025 18:15:25 GMT
ENV JAVA_VERSION=25-ea+15
# Fri, 21 Mar 2025 18:15:32 GMT
COPY dir:e950963f28ad2c857b90aa9d6a65c8fd16c501192e94c7e71046153717554da9 in C:\openjdk-25 
# Fri, 21 Mar 2025 18:15:38 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 21 Mar 2025 18:15:38 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:543388a101bf4d470af7e8817eff3f6f3b98f13d106939ab3f507a28f2825d0a`  
		Last Modified: Tue, 11 Mar 2025 22:40:48 GMT  
		Size: 106.9 MB (106907688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc960cac91ac363a95bef98a38cc3fb38959fa72bc0cb7265db2189a3a2e235a`  
		Last Modified: Fri, 21 Mar 2025 18:15:44 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a79cc5df8e0c7c8e6c563687a0f78d9870101094935a115b6870b8a9492fad`  
		Last Modified: Fri, 21 Mar 2025 18:15:43 GMT  
		Size: 1.1 KB (1066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e3300230bafc1fabe41a5770baa1e47cdcc97ad21e23f5a50534401d8b14c14`  
		Last Modified: Fri, 21 Mar 2025 18:15:43 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b900f540f263cb8a381ed0994e9bf77a8d728dab20861e8b814619f0338aea`  
		Last Modified: Fri, 21 Mar 2025 18:15:43 GMT  
		Size: 69.0 KB (69007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c1547c89f815bb84fdd7658f9d9202b0e22836d7a24573fd1f925db9f1a475`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 1.0 KB (1045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7985796622cb9631672c0810504b1c1b32008b7f14be35e0434ddf49b89f329`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15788921873c8cacd33c7f356128579bb2e1692261e82123a3108d4e60fc505`  
		Last Modified: Fri, 21 Mar 2025 18:15:53 GMT  
		Size: 207.5 MB (207502652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba29098ea7f10232e0f69015f2095bff4d06221e8fb282e2e62203b5107e69f`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 4.4 MB (4421007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd15deb15c083c0b0cc3b10c5f2512d0d55c61f196dd6dc470c7b0787c7940e3`  
		Last Modified: Fri, 21 Mar 2025 18:15:42 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
