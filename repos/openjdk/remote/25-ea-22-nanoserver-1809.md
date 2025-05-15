## `openjdk:25-ea-22-nanoserver-1809`

```console
$ docker pull openjdk@sha256:c046073958efc967f06095ed7eda1e35aadd6193d0c7db7b197e62ad5a8c39d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.7314; amd64

### `openjdk:25-ea-22-nanoserver-1809` - windows version 10.0.17763.7314; amd64

```console
$ docker pull openjdk@sha256:a3ba540e7eda561381f24b38ca17c3661b1f273e07e5bb5c7b8a5c064e206830
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.6 MB (321641319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c41127d941b6842aa268a8d29296355c1b14a5eeb8fc8485b8e101d9ce173a5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Fri, 09 May 2025 13:34:54 GMT
RUN Apply image 10.0.17763.7314
# Wed, 14 May 2025 22:10:54 GMT
SHELL [cmd /s /c]
# Wed, 14 May 2025 22:10:55 GMT
ENV JAVA_HOME=C:\openjdk-25
# Wed, 14 May 2025 22:10:55 GMT
USER ContainerAdministrator
# Wed, 14 May 2025 22:10:57 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 14 May 2025 22:10:57 GMT
USER ContainerUser
# Wed, 14 May 2025 22:10:58 GMT
ENV JAVA_VERSION=25-ea+22
# Wed, 14 May 2025 22:11:04 GMT
COPY dir:d2aeeab016ce5cfb722c90fbb6527341de5d03dac18528814b93fc4084ba77f8 in C:\openjdk-25 
# Wed, 14 May 2025 22:11:09 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 14 May 2025 22:11:09 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:67993f619eb734923df34b48b82cc62be3bba8b8a12116cccde4695b2546a3ba`  
		Last Modified: Tue, 13 May 2025 19:41:43 GMT  
		Size: 108.8 MB (108780592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a36e792622af88113228a82b02f51e00d1193caf98bf62d9dd5d430a2420f0`  
		Last Modified: Wed, 14 May 2025 22:11:16 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab254fd0082f3dfafcfcfcaff73d34bbd786362000eebd3321915f10df591c1a`  
		Last Modified: Wed, 14 May 2025 22:11:15 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:077941f894a09876eef2dfa40fa6aa80daf89c17e174a5c1a454b9a1f51df750`  
		Last Modified: Wed, 14 May 2025 22:11:15 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ad71391053ff562107e55bceb0e9cca39f70769a61641f0484cbd58ba3e7ac`  
		Last Modified: Wed, 14 May 2025 22:11:15 GMT  
		Size: 68.7 KB (68702 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3526665ebcf0433715f10ee965e479ecb4bcbd05cff56fb17c3f529376147d4`  
		Last Modified: Wed, 14 May 2025 22:11:13 GMT  
		Size: 1.0 KB (1032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2238c8170e48ccc782309833db5f05d2f8ead94087296d26751d1a3a023ebdd3`  
		Last Modified: Wed, 14 May 2025 22:11:13 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02197cf11c8ce1129d0658836bcfc3a27e0f2ef150b823d3998df2cf642f5091`  
		Last Modified: Wed, 14 May 2025 22:11:25 GMT  
		Size: 208.4 MB (208366191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7124649093354b73c5da4eb232fccd4d05789e787e67333f123207cb85d5fc7d`  
		Last Modified: Wed, 14 May 2025 22:11:14 GMT  
		Size: 4.4 MB (4419658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f7146fc7d0fc7cad5bf0c2b1311bae145c2a4ce70071634ba294ed4411936ab0`  
		Last Modified: Wed, 14 May 2025 22:11:14 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
