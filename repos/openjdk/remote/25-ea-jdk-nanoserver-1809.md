## `openjdk:25-ea-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:42dbdac7e5568118dcd98b35030f140ae8c271bbdee698c8fcdf41316c3b03dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7009; amd64

### `openjdk:25-ea-jdk-nanoserver-1809` - windows version 10.0.17763.7009; amd64

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
