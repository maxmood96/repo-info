## `eclipse-temurin:25-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:81d12c8e15c9f1720212bb40b91e589cc47d7013f5f4d0d106f4f681c0899d29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.32230; amd64

### `eclipse-temurin:25-nanoserver-ltsc2025` - windows version 10.0.26100.32230; amd64

```console
$ docker pull eclipse-temurin@sha256:a4a8af21dfaf025c6c6870550b7e36291d01eb40ff1dd3d067041f9bd4d01c22
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.2 MB (337202005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedea746267c5add62ffa8b7b1b783f2839a92bbd224ef24f9c8bfc2f6e0e45e`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 11 Jan 2026 06:15:10 GMT
RUN Apply image 10.0.26100.32230
# Thu, 05 Feb 2026 22:40:04 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:40:05 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:40:05 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 05 Feb 2026 22:40:06 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:40:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:40:16 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:45 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Thu, 05 Feb 2026 22:40:51 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 05 Feb 2026 22:40:52 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d441ba4c6d25e3ab6a1e3ce5360fd1d1214e97975f1e40b10c0ccb55dc46ad22`  
		Last Modified: Tue, 13 Jan 2026 22:42:10 GMT  
		Size: 199.1 MB (199076547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf8eb19f89ac1b618a34285625693ac2b2b931ba02e3bf7210fc3bfb50f6591d`  
		Last Modified: Thu, 05 Feb 2026 22:40:57 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa5705fde259c85367b4564254042fb2ea6d5ceef73a0f27295d7019a5c670d`  
		Last Modified: Thu, 05 Feb 2026 22:40:57 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57d1aacdda3632ea4f298304d27e2f31c28f0d2fa3eb018fcffbe419e9a64b36`  
		Last Modified: Thu, 05 Feb 2026 22:40:57 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05f4754395f4bdd96b8f7e2ef0043b6a8965a5ae07d73bc97459c09037de3568`  
		Last Modified: Thu, 05 Feb 2026 22:40:57 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afa5ad6c704872ef8e04d3a01fb07b2a29474e90f1004291c5383928fda3b976`  
		Last Modified: Thu, 05 Feb 2026 22:40:56 GMT  
		Size: 77.6 KB (77625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da59acfd1af433f1c1e176c16cc7bcf1f2cf429060da6f8a560279c1ce35715`  
		Last Modified: Thu, 05 Feb 2026 22:40:56 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c48439fe4a39aff4fb547e4dad911403322e0b9279e970f3a51c7ffb1d84d82`  
		Last Modified: Thu, 05 Feb 2026 22:41:08 GMT  
		Size: 137.9 MB (137932013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4f1081efacbbfc550fe1036e8a0e40dd5774c477b426849dd63d9e4527ed0e`  
		Last Modified: Thu, 05 Feb 2026 22:40:56 GMT  
		Size: 109.4 KB (109443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8c389b60a4615b95044c391a138bfdf2620506c43a8ccceba68fe2752a1c1e0`  
		Last Modified: Thu, 05 Feb 2026 22:40:56 GMT  
		Size: 1.1 KB (1064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
