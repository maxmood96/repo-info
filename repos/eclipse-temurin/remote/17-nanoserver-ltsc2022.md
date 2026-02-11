## `eclipse-temurin:17-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:383073caba0e9788619d0a83449561084feb5cb817863184700817a62335aa11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4773; amd64

### `eclipse-temurin:17-nanoserver-ltsc2022` - windows version 10.0.20348.4773; amd64

```console
$ docker pull eclipse-temurin@sha256:f166a2a39d6db8d94c2d371991c1fde4a1f39ba561ff41af19ba6d8ee43626e2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314336650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8a4bbb6403ba514bc302a17d451c117478a16a5f6d1cf75a697cea3fc3dbc5f`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 06 Feb 2026 09:42:51 GMT
RUN Apply image 10.0.20348.4773
# Tue, 10 Feb 2026 23:30:56 GMT
SHELL [cmd /s /c]
# Tue, 10 Feb 2026 23:30:57 GMT
ENV JAVA_VERSION=jdk-17.0.18+8
# Tue, 10 Feb 2026 23:30:57 GMT
ENV JAVA_HOME=C:\openjdk-17
# Tue, 10 Feb 2026 23:30:58 GMT
USER ContainerAdministrator
# Tue, 10 Feb 2026 23:31:00 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Tue, 10 Feb 2026 23:31:00 GMT
USER ContainerUser
# Tue, 10 Feb 2026 23:31:08 GMT
COPY dir:fb23a79434a3e7defa51a1bec1a7ef896ff849f7ba85f2629e1913957db57a2e in C:\openjdk-17 
# Tue, 10 Feb 2026 23:31:12 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 10 Feb 2026 23:31:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ca0a97fd01c767a53a3e0856fa1db64de3eecf8d8b3f54cc7e6b032890bd7e7e`  
		Last Modified: Tue, 10 Feb 2026 19:28:47 GMT  
		Size: 126.6 MB (126645827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15b005c26b3eb53f2a73969b3045aa2b8dfbd47327ae7840b25c73a4df0798a9`  
		Last Modified: Tue, 10 Feb 2026 23:31:19 GMT  
		Size: 1.1 KB (1070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283fc896b5852fb4d57e90839e54314d16c9d1fd026fdea56d9f39269dec1b7e`  
		Last Modified: Tue, 10 Feb 2026 23:31:18 GMT  
		Size: 1.1 KB (1083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d680ea3b9b2f8c77f3be52d6691805c5b13381df085565f0e75d4782f730657`  
		Last Modified: Tue, 10 Feb 2026 23:31:18 GMT  
		Size: 1.1 KB (1075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9d92bae2d731be2e34cda36ca42b0201e901172a5e661b5653e146a868970e1`  
		Last Modified: Tue, 10 Feb 2026 23:31:18 GMT  
		Size: 1.1 KB (1068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efadadff715b53ed911df06d2017dc29e2474ae4b4b48e40dfd6e713deacbbcc`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 77.4 KB (77381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfea66346a34e2b2231506c9aa24e7f0c0e46a857c8892c692a841d68cd2d10`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009b2af3cd856165a295c3385dc422c95d89cdf0b442472cceaaab1eca0c6837`  
		Last Modified: Tue, 10 Feb 2026 23:31:29 GMT  
		Size: 187.5 MB (187486794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23809c1ed4f5806350689273478021e91c886dd004d7e46f40b28eb8f556d89`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 120.2 KB (120210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5f3a36b99dd98364b6bbd4b15261c572f279acc73889fe7610aa3796263ea9`  
		Last Modified: Tue, 10 Feb 2026 23:31:17 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
