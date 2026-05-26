## `openjdk:27-ea-23-nanoserver-ltsc2025`

```console
$ docker pull openjdk@sha256:bcf6544440e9b6db2a2b2c60f53fc8af9d34007cb56d62e31d4751ce839e6e01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32860; amd64

### `openjdk:27-ea-23-nanoserver-ltsc2025` - windows version 10.0.26100.32860; amd64

```console
$ docker pull openjdk@sha256:be579848cc405a302e02e5bd3cb19a37dd595bc1660c4c598cc26b32c95f56d3
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **424.8 MB (424842006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b92549b6533569e3bec79c8d8cb53b7aefd689c09454dd9f315e97bbe52b00`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 10 May 2026 09:46:02 GMT
RUN Apply image 10.0.26100.32860
# Tue, 26 May 2026 20:05:04 GMT
SHELL [cmd /s /c]
# Tue, 26 May 2026 20:05:07 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 26 May 2026 20:05:09 GMT
USER ContainerAdministrator
# Tue, 26 May 2026 20:05:30 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 26 May 2026 20:05:31 GMT
USER ContainerUser
# Tue, 26 May 2026 20:05:32 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 20:07:17 GMT
COPY dir:80513245d63c2b8708d5fdd101a6acf071e02784ec2be0deabfc91a3dc9cc485 in C:\openjdk-27 
# Tue, 26 May 2026 20:07:30 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 26 May 2026 20:07:31 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:34ab6476d71f2d23d05a00ac439000ba4c19d17e5c66f15efbe329ed79bba2bf`  
		Last Modified: Tue, 12 May 2026 22:29:47 GMT  
		Size: 199.7 MB (199739001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3c2e2133b157dd9b85568cd977824c3576355ac9843f37dd2346c9aed466151`  
		Last Modified: Tue, 26 May 2026 20:07:37 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb449d317ed6e50781fcd8f572c192980221a5439457479c34cf0808f44964c2`  
		Last Modified: Tue, 26 May 2026 20:07:37 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b3bc2f60dd273f612a7dec869d7cfc6b21b5a1d6737fdcf08316509b13131f3`  
		Last Modified: Tue, 26 May 2026 20:07:37 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5f4ae86bf173a39591b3ff259636853dbdc93f2d2096f2948fc8a630cfdb2bb`  
		Last Modified: Tue, 26 May 2026 20:07:37 GMT  
		Size: 70.5 KB (70470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7514f02aa805eea46edf5ad2ce0faa77d001984708a7e84382ef6bc873402f`  
		Last Modified: Tue, 26 May 2026 20:07:35 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64adcc101e17fb4765e1a4a69203e9d1a5c693d94a7bfc8a40ae411cb163dd9a`  
		Last Modified: Tue, 26 May 2026 20:07:35 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e86849a860af16cb36e91aab9da776fd57ee237c71b286d6bc1111afce5d6b5`  
		Last Modified: Tue, 26 May 2026 20:07:51 GMT  
		Size: 224.9 MB (224912979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80dd14bc068d8c8b239c39f2ed21ca4e66af486ad0c94880c3d6d7662a149230`  
		Last Modified: Tue, 26 May 2026 20:07:35 GMT  
		Size: 113.4 KB (113373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d39ac0860efcb6c84a1222d9ad9bb4fa953efc0766f16ff7c89bb62b675333cf`  
		Last Modified: Tue, 26 May 2026 20:07:35 GMT  
		Size: 1.0 KB (1012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
