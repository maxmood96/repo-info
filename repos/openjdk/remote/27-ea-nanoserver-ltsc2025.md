## `openjdk:27-ea-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:ee34f34a20c1b608e70ca548ff2c7dc8bccc9ba1691ed7fef01569a3a2e8cb7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32370; amd64

### `openjdk:27-ea-nanoserver-ltsc2025` - windows version 10.0.26100.32370; amd64

```console
$ docker pull openjdk@sha256:fd7603ea1e7a4234bd6fe9b2cec135c813ded684a5ad798fe6846d5121ff3b98
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.8 MB (423766316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cc8c0b8dc43917fd771e48c0fd700be979a356ae735e93ee0a9a1daa2fd815`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 22:06:41 GMT
RUN Apply image 10.0.26100.32370
# Sat, 07 Mar 2026 01:08:31 GMT
SHELL [cmd /s /c]
# Sat, 07 Mar 2026 01:08:32 GMT
ENV JAVA_HOME=C:\openjdk-27
# Sat, 07 Mar 2026 01:08:32 GMT
USER ContainerAdministrator
# Sat, 07 Mar 2026 01:08:43 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Sat, 07 Mar 2026 01:08:44 GMT
USER ContainerUser
# Sat, 07 Mar 2026 01:08:44 GMT
ENV JAVA_VERSION=27-ea+12
# Sat, 07 Mar 2026 01:09:17 GMT
COPY dir:39bc387d6f4a82116c9105a5f2b625fb020bc268f5298b0afe5a9520fad3060e in C:\openjdk-27 
# Sat, 07 Mar 2026 01:09:22 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Sat, 07 Mar 2026 01:09:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:77321bd03612cfa46920e790ae0c3b142758a5803ad759fdb406c98b6f2e4ed0`  
		Last Modified: Tue, 10 Feb 2026 22:50:26 GMT  
		Size: 199.3 MB (199251619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d81e20bae1eb3de0a07008f8cafb5dd2154fa4c97008c5502e687fe7f190e8f`  
		Last Modified: Sat, 07 Mar 2026 01:09:29 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:765dea2043f0942c7731fc57381ebbba1a68889dd65d4d4e1915b080fb1f2252`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 1.1 KB (1065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7906a4196aa868e28a84b96f9dfc8478fef755188b3a62004faf4aa2dff3253`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4a462b43f1924bb1830c86f59814c144fed443bd94b021fd60c933887cd971f`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 69.7 KB (69687 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2853fa4e94788599ca2956be40a6b791f1225ba7b143d501602e1c83b2bdc9f4`  
		Last Modified: Sat, 07 Mar 2026 01:09:27 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:640313cc78d5bee9c84262c6e56a096a20a0ce13d60db709de7996c4940846bd`  
		Last Modified: Sat, 07 Mar 2026 01:09:28 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc0bb66e532253dd75ca2d36649683084c325eeca950d490d4bff863d9bbcc10`  
		Last Modified: Sat, 07 Mar 2026 01:09:43 GMT  
		Size: 224.3 MB (224333831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0aa1dca44c70ecdc192ca0fc1749847e21c94852a53f767e97101c09ad6aad7`  
		Last Modified: Sat, 07 Mar 2026 01:09:27 GMT  
		Size: 104.7 KB (104696 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321759a62e8a965c891cfb2fefc92176248ec66484feb54526360de2995f1f3a`  
		Last Modified: Sat, 07 Mar 2026 01:09:27 GMT  
		Size: 1.1 KB (1073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
