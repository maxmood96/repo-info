## `eclipse-temurin:21-jdk-nanoserver-ltsc2025`

```console
$ docker pull eclipse-temurin@sha256:e326ab9fef4debb25c5c8b00b0211b9e2c7eca155c156dbce7f19863bd658f4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.26100.6905; amd64

### `eclipse-temurin:21-jdk-nanoserver-ltsc2025` - windows version 10.0.26100.6905; amd64

```console
$ docker pull eclipse-temurin@sha256:5711b1b3bd750823baf047ef520e7146ea66e87bdfaa02355650d1f62932daf1
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 MB (396006138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25019fe2eb29e8d91f8366249d54c3964b7ab6cc4611ff14aef4142df3cbe6a3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 22 Oct 2025 07:22:01 GMT
RUN Apply image 10.0.26100.6905
# Sat, 08 Nov 2025 19:18:29 GMT
SHELL [cmd /s /c]
# Sat, 08 Nov 2025 19:18:30 GMT
ENV JAVA_VERSION=jdk-21.0.9+10
# Sat, 08 Nov 2025 19:18:30 GMT
ENV JAVA_HOME=C:\openjdk-21
# Sat, 08 Nov 2025 19:18:31 GMT
USER ContainerAdministrator
# Sat, 08 Nov 2025 19:18:37 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Sat, 08 Nov 2025 19:18:37 GMT
USER ContainerUser
# Sat, 08 Nov 2025 19:19:00 GMT
COPY dir:ca3f22bac3b96b31650dd9d8b46eabc8cfc824f09a5d61f04cd758713bcc4892 in C:\openjdk-21 
# Sat, 08 Nov 2025 19:19:06 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Sat, 08 Nov 2025 19:19:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9188956580c47f583c927f17e42f8825823890544237141f21ca4ef10ea55e60`  
		Last Modified: Fri, 24 Oct 2025 11:13:56 GMT  
		Size: 194.0 MB (194029378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37408c046b83db4ae29530e52943549c64b4717ebccea3bd128a29d34f7938d1`  
		Last Modified: Sat, 08 Nov 2025 19:19:36 GMT  
		Size: 1.1 KB (1084 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7860ec14ce608862dd08c3a9f801ffa80eef03da59f24c9a25668fa08b8328d3`  
		Last Modified: Sat, 08 Nov 2025 19:19:36 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0c8e8eb03efdac25b783bfc07f07c4152d62fd348c619a39ddac1b96982ef6d`  
		Last Modified: Sat, 08 Nov 2025 19:19:37 GMT  
		Size: 1.1 KB (1081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:075ac2e61d7177ae64fa8b7553616a07052afa744e1765af9855641e45ef2778`  
		Last Modified: Sat, 08 Nov 2025 19:19:37 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e26d3eb566299e5d044556c78366d9090f43d813c350b4d0cbfd00dabf87fe04`  
		Last Modified: Sat, 08 Nov 2025 19:19:39 GMT  
		Size: 70.5 KB (70547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5599a53627283603eea459018e6e85da6f2f050cea0c4efd4441502d2b8e7b`  
		Last Modified: Sat, 08 Nov 2025 19:19:37 GMT  
		Size: 1.1 KB (1067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54c7615e4da455100367cf5b26af8978fd1d891bfea4808b9e1f93eecafe1801`  
		Last Modified: Sat, 08 Nov 2025 22:18:06 GMT  
		Size: 201.8 MB (201782475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3582fd8d1ab349380357e5207838345ac9345196df82b23eb448d253297a43ca`  
		Last Modified: Sat, 08 Nov 2025 19:19:38 GMT  
		Size: 117.3 KB (117261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbb8f203c67956dfce422775fe41069c79729112d515b9941971b91de55fef81`  
		Last Modified: Sat, 08 Nov 2025 19:19:38 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
