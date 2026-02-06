## `eclipse-temurin:25-jdk-nanoserver-ltsc2022`

```console
$ docker pull eclipse-temurin@sha256:0b8b330cfd9bc78cbd8f5afcfd32902e9ff006eac4315c944a887732fdf40c02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.4648; amd64

### `eclipse-temurin:25-jdk-nanoserver-ltsc2022` - windows version 10.0.20348.4648; amd64

```console
$ docker pull eclipse-temurin@sha256:901032d65fb15d3dbfe3ffe0cd95c982031d24e4a2736c87cf0db745527a40d6
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **264.9 MB (264852930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dde30568702d87084faaeb24c39b6ece109c6db1115dc0e2b57f4a3b62d3ce3d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 08 Jan 2026 23:55:05 GMT
RUN Apply image 10.0.20348.4648
# Thu, 05 Feb 2026 22:39:16 GMT
SHELL [cmd /s /c]
# Thu, 05 Feb 2026 22:40:21 GMT
ENV JAVA_VERSION=jdk-25.0.2+10
# Thu, 05 Feb 2026 22:40:22 GMT
ENV JAVA_HOME=C:\openjdk-25
# Thu, 05 Feb 2026 22:40:22 GMT
USER ContainerAdministrator
# Thu, 05 Feb 2026 22:40:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Thu, 05 Feb 2026 22:40:25 GMT
USER ContainerUser
# Thu, 05 Feb 2026 22:40:59 GMT
COPY dir:ebca1fed269853ebca056470dac79e7ebf8f2b759d9752408e0c7f2313fb3842 in C:\openjdk-25 
# Thu, 05 Feb 2026 22:41:08 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 05 Feb 2026 22:41:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:45913f0a8ae18b9ed53b6fdc600f5062ad8ee62812c6d52c890cb122810ceb81`  
		Last Modified: Tue, 13 Jan 2026 20:07:11 GMT  
		Size: 126.7 MB (126696821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4c75b6a0defca9fcf399b6d239ee405e6b00e1f4ad808bd98a6eadba33d863`  
		Last Modified: Thu, 05 Feb 2026 22:39:41 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a79e52c59aebf9064280126540c591d9ef81ff9315a476cc3f1a5b9f16f8fc`  
		Last Modified: Thu, 05 Feb 2026 22:41:14 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8f511d8567ccabefbb965658c3ef8f967207a58849e7f11772ec0bd0aa5eda0`  
		Last Modified: Thu, 05 Feb 2026 22:41:14 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726850af1e26582d287ebb479fb6467de245ab6f2fd4d311622f5aac66b17812`  
		Last Modified: Thu, 05 Feb 2026 22:41:14 GMT  
		Size: 1.1 KB (1069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899fe9c26bec39677024c832cadceaf20f8ca0044ecc32907368aef3a675b51c`  
		Last Modified: Thu, 05 Feb 2026 22:41:12 GMT  
		Size: 76.4 KB (76409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:463d4222aaa323fa571003db044c6e4248833b3197b59023448f5385904059b5`  
		Last Modified: Thu, 05 Feb 2026 22:41:12 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea2cf37442749f4170a269df2779b85ae306a4580d451917c9a8a2801a9dcbe4`  
		Last Modified: Thu, 05 Feb 2026 22:41:24 GMT  
		Size: 137.9 MB (137932483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3dab2a3229f7994c7889567b034f4f3f3473f030932b52a47f4963c7e46eded`  
		Last Modified: Thu, 05 Feb 2026 22:41:12 GMT  
		Size: 140.8 KB (140845 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d5f6100670c9691975460aae971d6eefecc9f1127e9216ecd8cf087b0f2e505`  
		Last Modified: Thu, 05 Feb 2026 22:41:12 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
