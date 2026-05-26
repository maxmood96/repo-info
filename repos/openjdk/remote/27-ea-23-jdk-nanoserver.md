## `openjdk:27-ea-23-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:6ce69dcc0411b3bdd52223a343849c6b5023775f10eb09e8b29eecdc74f0b924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.26100.32860; amd64
	-	windows version 10.0.20348.5139; amd64

### `openjdk:27-ea-23-jdk-nanoserver` - windows version 10.0.26100.32860; amd64

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

### `openjdk:27-ea-23-jdk-nanoserver` - windows version 10.0.20348.5139; amd64

```console
$ docker pull openjdk@sha256:008f624c8f5616492e7453cd0211e7fc52f8a4067efc26387f4161f830506d33
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **352.1 MB (352148081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a43bcd75949007d92d82c87e942cecbddce17ee30bcb91d399288ad62f13a01`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 07 May 2026 03:34:45 GMT
RUN Apply image 10.0.20348.5139
# Tue, 26 May 2026 20:25:08 GMT
SHELL [cmd /s /c]
# Tue, 26 May 2026 20:25:10 GMT
ENV JAVA_HOME=C:\openjdk-27
# Tue, 26 May 2026 20:25:11 GMT
USER ContainerAdministrator
# Tue, 26 May 2026 20:25:27 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 26 May 2026 20:25:27 GMT
USER ContainerUser
# Tue, 26 May 2026 20:25:28 GMT
ENV JAVA_VERSION=27-ea+23
# Tue, 26 May 2026 20:26:29 GMT
COPY dir:80513245d63c2b8708d5fdd101a6acf071e02784ec2be0deabfc91a3dc9cc485 in C:\openjdk-27 
# Tue, 26 May 2026 20:26:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 26 May 2026 20:26:36 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ad8f1a10df37e4e23a0a01bc418a0257a18e7ccd287a5ca33cb10569eb83c8bf`  
		Last Modified: Tue, 12 May 2026 19:16:02 GMT  
		Size: 127.0 MB (127038785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:908ac4a55db0291ca25e71aae4a2b48deea0b528d09232443aa10a1e1a9c3533`  
		Last Modified: Tue, 26 May 2026 20:26:42 GMT  
		Size: 1.1 KB (1099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:979e85692c962b331c2f115fb46616cd8f79e0dca05913a61a02c0e523758461`  
		Last Modified: Tue, 26 May 2026 20:26:42 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5622d8a53cb2117d88db0b46a0e8af49565ae694bb7367e22b9744c9d3c0adb`  
		Last Modified: Tue, 26 May 2026 20:26:42 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06712f945c0143e1413691ef09ec382e3d9207925e81ab364297f7e7b8795cab`  
		Last Modified: Tue, 26 May 2026 20:26:42 GMT  
		Size: 72.1 KB (72113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3274d383a40a16897d996b1ad733bc105a187279eff70c1344381b6b2b4d1519`  
		Last Modified: Tue, 26 May 2026 20:26:40 GMT  
		Size: 1.0 KB (1044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0facc702fe217dc035f14fb49560e4d21c627cc38f9298a4c21fbe8c1cb87e1e`  
		Last Modified: Tue, 26 May 2026 20:26:40 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96c91fa3f5cc3b71c36f0f651740529e308ffbfd7749af775fbdb5b5af5d74aa`  
		Last Modified: Tue, 26 May 2026 20:26:55 GMT  
		Size: 224.9 MB (224912827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d449ca6bdc6bf6a5e91128a9bc9eb95a7a0789ae0a0e739087ebeb3f7068b0d5`  
		Last Modified: Tue, 26 May 2026 20:26:40 GMT  
		Size: 118.0 KB (117960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719b33e20d14824d615b4cb2772e5b2d94dc527b779353db1544bba06ea70966`  
		Last Modified: Tue, 26 May 2026 20:26:40 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
